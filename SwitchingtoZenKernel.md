---


---

<h1 id="how-to-switch-to-the-zen-kernel">How to Switch to the Zen Kernel</h1>
<p>If you are here, you are trying to switch to the Zen Kernel on</p>
<p>AcreetionOS. You first need to install the packages required to use</p>
<p>the Zen Kernel.</p>
<p>Installation command:</p>
<pre><code>
sudo pacman -Sy linux-zen linux-zen-headers --noconfirm

</code></pre>
<p>From here on you need to follow one of two sections. If you are using the default of AcreetionOS, grub, follow the first section. If you converted to systemd-boot, follow the second section.</p>
<p>GRUB Instructions:</p>
<p>Make sure you have installed the Zen Kernel. Afterward follow these instructions.</p>
<p>You will open /boot/grub/grub.cfg with your desired text editor. If you are new to Linux and are using AcreetionOS as your first distro, use Gedit to open it. If you are advanced, you know what you are doing, so follow below:</p>
<p>You will search within the grub.cfg file for <em>initrd</em>. The lines above should say “title” and “linux”. You will change “/vmlinuz-linux” to be “/vmlinuz-linux-zen” and “/initramfs-linux.img” to “/initramfs-linux-zen.img”. Afterward you will save the file and close the editor.</p>
<p>You will now need to open up a terminal emulator for the next part. You will open it and type <em>“sudo mkinitcpio -P &amp;&amp; sudo grub-mkconfig -o /boot/grub/grub.cfg”</em> This will update your initramfs and grub configuration. Afterward, reboot and you should boot into the OS, using the Zen Kernel. In the instance this does not work for whatever reason, feel free to email us at <a href="mailto:acreetionos@gmail.com">acreetionos@gmail.com</a> if you need support.</p>

<h2> Systemd-boot Instructions:</h2>
<p>In the case os systemd-boot, you will need to install the packages as before and then open /boot/loader/entries/[insert name of configuration file.conf]. You will need to edit the “linux” and “initrd” lines. You will change “/vmlinuz-linux” to “/vmlinuz-linux-zen” and “/initramfs-linux.img” and “/initramfs-linux-zen.img”. You will then simply save the file and reboot.</p>
<p>Note: If you end up not being able to boot, use the fallback image.</p>

