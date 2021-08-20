---
description: Descreve as possíveis arquiteturas de computador.
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: Constantes do computador do arquivo de imagem (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6498bcc715fe318f79b3aaa09c3cb7b19855daab2db5a0b110d756ef54fb21e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117958389"
---
# <a name="image-file-machine-constants"></a>Constantes do computador do arquivo de imagem

Descreve as possíveis arquiteturas de computador. Usado em [**GetSystemWow64Directory2,**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) e [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).

<dl> <dt>

<span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**COMPUTADOR DE \_ ARQUIVO \_ DE IMAGEM \_ DESCONHECIDO**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Unknown


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**HOST DE \_ DESTINO DO COMPUTADOR DO ARQUIVO DE \_ \_ \_ IMAGEM**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Interage com o host e não com um convidado WOW64

> [!Note]  
> Essa constante está disponível a partir do Windows 10, versão 1607 e Windows Server 2016.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ I386**
</dt> <dd> <dl> <dt>

0x014c
</dt> <dt>



Intel 386


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ R3000**
</dt> <dd> <dl> <dt>

0x0162
</dt> <dt>



MIPS little-endian, 0x160 big-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ R4000**
</dt> <dd> <dl> <dt>

0x0166
</dt> <dt>



MIPS little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ R10000**
</dt> <dd> <dl> <dt>

0x0168
</dt> <dt>



MIPS little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ WCEMIPSV2**
</dt> <dd> <dl> <dt>

0x0169
</dt> <dt>



MIPS little-endian WCE v2


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**COMPUTADOR \_ DO ARQUIVO DE IMAGEM \_ \_ ALFA**
</dt> <dd> <dl> <dt>

0x0184
</dt> <dt>



Alfa \_ AXP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**MÁQUINA DE \_ ARQUIVOS \_ DE IMAGEM \_ SH3**
</dt> <dd> <dl> <dt>

0x01a2
</dt> <dt>



SH3 little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ SH3DSP**
</dt> <dd> <dl> <dt>

0x01a3
</dt> <dt>



SH3DSP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**MÁQUINA \_ DE ARQUIVOS DE IMAGEM \_ \_ SH3E**
</dt> <dd> <dl> <dt>

0x01a4
</dt> <dt>



SH3E little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**MÁQUINA DE \_ ARQUIVOS \_ DE IMAGEM \_ SH4**
</dt> <dd> <dl> <dt>

0x01a6
</dt> <dt>



SH4 little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**MÁQUINA DE \_ ARQUIVOS \_ DE IMAGEM \_ SH5**
</dt> <dd> <dl> <dt>

0x01a8
</dt> <dt>



SH5


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**ARM DO \_ COMPUTADOR DO ARQUIVO DE \_ \_ IMAGEM**
</dt> <dd> <dl> <dt>

0x01c0
</dt> <dt>



Arm Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**MINIATURA DO \_ COMPUTADOR DO ARQUIVO DE \_ \_ IMAGEM**
</dt> <dd> <dl> <dt>

0x01c2
</dt> <dt>



Arm Thumb/Thumb-2 Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**ARMNT \_ DO COMPUTADOR DO ARQUIVO DE \_ \_ IMAGEM**
</dt> <dd> <dl> <dt>

0x01c4
</dt> <dt>



Arm Thumb-2 Little-Endian

> [!Note]  
> Essa constante está disponível a partir do Windows 7 e Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ AM33**
</dt> <dd> <dl> <dt>

0x01d3
</dt> <dt>



TAM33BD


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**COMPUTADOR \_ DO ARQUIVO DE IMAGEM \_ \_ POWERPC**
</dt> <dd> <dl> <dt>

0x01F0
</dt> <dt>



IBM PowerPC Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**COMPUTADOR \_ DO ARQUIVO DE IMAGEM \_ \_ POWERPCFP**
</dt> <dd> <dl> <dt>

0x01f1
</dt> <dt>



POWERPCFP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**MÁQUINA DE \_ ARQUIVOS \_ DE IMAGEM \_ IA64**
</dt> <dd> <dl> <dt>

0x0200
</dt> <dt>



Intel 64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**\_ \_ MIPS16 DO COMPUTADOR DO \_ ARQUIVO DE IMAGEM**
</dt> <dd> <dl> <dt>

0x0266
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ ALPHA64**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



ALPHA64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**\_ \_ \_ MIPSFPU DO COMPUTADOR DO ARQUIVO DE IMAGEM**
</dt> <dd> <dl> <dt>

0x0366
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**MÁQUINA \_ DE ARQUIVOS DE IMAGEM \_ \_ MIPSFPU16**
</dt> <dd> <dl> <dt>

0x0466
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ AXP64**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



AXP64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**TRICORE \_ DO COMPUTADOR DO ARQUIVO DE \_ \_ IMAGEM**
</dt> <dd> <dl> <dt>

0x0520
</dt> <dt>



Infineon


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**\_CEF DO \_ COMPUTADOR DO ARQUIVO \_ DE IMAGEM**
</dt> <dd> <dl> <dt>

0x0CEF
</dt> <dt>



CEF


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**MÁQUINA DE \_ ARQUIVOS \_ DE IMAGEM \_ EBC**
</dt> <dd> <dl> <dt>

0x0EBC
</dt> <dt>



Código de byte EFI


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ AMD64**
</dt> <dd> <dl> <dt>

0x8664
</dt> <dt>



AMD64 (K8)


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ M32R**
</dt> <dd> <dl> <dt>

0x9041
</dt> <dt>



M32R little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**COMPUTADOR \_ DE ARQUIVO DE IMAGEM \_ \_ ARM64**
</dt> <dd> <dl> <dt>

0xAA64
</dt> <dt>



Arm64 Little-Endian

> [!Note]  
> essa constante está disponível a partir do Windows 8.1 e do Windows Server 2012 R2.

 


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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




