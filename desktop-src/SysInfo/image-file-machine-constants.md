---
description: Descreve possíveis arquiteturas de computador.
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: Constantes de máquina de arquivo de imagem (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c43767ce0d86edf2285241772ea060573efc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501966"
---
# <a name="image-file-machine-constants"></a>Constantes de máquina de arquivo de imagem

Descreve possíveis arquiteturas de computador. Usado em [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) e [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).

<dl> <dt>

<span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**computador de arquivo de imagem \_ \_ \_ desconhecido**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Unknown


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**\_host de \_ destino da máquina do arquivo de imagem \_ \_**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Interage com o host e não com um convidado do WOW64

> [!Note]  
> Essa constante está disponível a partir do Windows 10, versão 1607 e Windows Server 2016.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**Arquivo de imagem/ \_ \_ computador \_ i386**
</dt> <dd> <dl> <dt>

0x014c
</dt> <dt>



Intel 386


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**\_R3000 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x0162
</dt> <dt>



MIPS little-endian, 0x160 big-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**\_R4000 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x0166
</dt> <dt>



MIPS little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**\_R10000 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x0168
</dt> <dt>



MIPS little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**\_WCEMIPSV2 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x0169
</dt> <dt>



MIPS little-endian Stone v2


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**computador de arquivo de imagem \_ \_ \_ Alpha**
</dt> <dd> <dl> <dt>

0x0184
</dt> <dt>



Alpha \_ AXP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**\_SH3 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x01a2
</dt> <dt>



SH3 little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**\_SH3DSP da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x01a3
</dt> <dt>



SH3DSP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**\_SH3E da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x01a4
</dt> <dt>



SH3E little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**\_Sh4 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x01a6
</dt> <dt>



SH4 little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**\_SH5 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x01a8
</dt> <dt>



SH5


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**\_ARM de \_ máquina de arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x01c0
</dt> <dt>



Little-Endian ARM


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**\_miniatura do \_ computador do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x01c2
</dt> <dt>



Little-Endian ARM Thumb/Thumb-2


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**\_ARMNT da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x01c4
</dt> <dt>



ARM Thumb-2 Little-Endian

> [!Note]  
> Essa constante está disponível a partir do Windows 7 e do Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**\_AM33 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x01d3
</dt> <dt>



TAM33BD


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**\_POWERPC de \_ máquina de arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x01F0
</dt> <dt>



IBM PowerPC Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**\_POWERPCFP da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x01f1
</dt> <dt>



POWERPCFP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**Computador de arquivo de imagem \_ \_ \_ IA64**
</dt> <dd> <dl> <dt>

0x0200
</dt> <dt>



Intel 64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**\_MIPS16 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x0266
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**\_ALPHA64 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



ALPHA64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**\_MIPSFPU da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x0366
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**\_MIPSFPU16 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x0466
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**\_AXP64 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



AXP64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**computador de arquivo de imagem \_ \_ \_ Tricore**
</dt> <dd> <dl> <dt>

0x0520
</dt> <dt>



Infineon


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**máquina de arquivo de imagem \_ \_ \_ CEF**
</dt> <dd> <dl> <dt>

0x0CEF
</dt> <dt>



CEF


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**computador de arquivo de imagem \_ \_ \_ EBC**
</dt> <dd> <dl> <dt>

0x0EBC
</dt> <dt>



Código de byte EFI


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**Máquina de arquivo de imagem \_ \_ \_ AMD64**
</dt> <dd> <dl> <dt>

0x8664
</dt> <dt>



AMD64 (K8)


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**\_M32R da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0x9041
</dt> <dt>



M32R little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**\_ARM64 da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0xAA64
</dt> <dt>



Little-Endian ARM64

> [!Note]  
> Essa constante está disponível a partir do Windows 8.1 e do Windows Server 2012 R2.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**\_CEE da \_ máquina do arquivo de imagem \_**
</dt> <dd> <dl> <dt>

0xC0EE
</dt> <dt>



CEE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




