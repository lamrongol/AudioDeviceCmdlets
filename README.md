Basic audio device control from Powershell including Nuget Package Manager Console.

## Install.

1. New-Item "$profile\Modules\AudioDeviceCmdlets" -Type directory -Force
1. Copy CoreAudioApi.dll, AudioDeviceCmdlets.dll and AudioDeviceCmdlets.dll-Help.xml
1. Import the binary module. This can go into your profile.
        
		Import-Module AudioDeviceCmdlets

1. You may need to set the execution policy.

        Set-ExecutionPolicy -ExecutionPolicy RemoteSigned

## Suggested Aliases. I may set these in the module in the future.
    New-Alias -Name mute -Value Set-DefaultAudioDeviceMute
    New-Alias -Name vol -Value set-DefaultAudioDeviceVolume

## Exposed Cmdlets
* Get-DefaultAudioDevice
* Get-AudioDeviceList
* Set-DefaultAudioDevice [-Index] &lt;Int&gt;
* Set-DefaultAudioDevice [-Name] &lt;String&gt;
* Set-DefaultAudioDevice [-InputObject] &lt;AudioDevice&gt;
* Set-DefaultAudioDeviceVolume -Volume &lt;float&gt;
* Set-DefaultAudioDeviceMute
* Write-DefaultAudioDeviceValue

## Attribution
Based on work done by Ray M. <a href="http://www.codeproject.com/Articles/18520/Vista-Core-Audio-API-Master-Volume-Control">hosted</a> on The Code Project