---
description: Tipos de partição válidos usados por drivers de disco.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Tipos de partição de disco (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756777"
---
# <a name="disk-partition-types"></a>Tipos de partição de disco

A tabela a seguir identifica os tipos de partição válidos que são usados por drivers de disco.



| Constante/valor                                                                                                                                                                                                                                      | Descrição                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <dt>**Partição \_ do ENTRADA \_ não utilizada**</dt> <dt>0x00</dt> </dl> | Uma partição de entrada não utilizada.<br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <dt>**Partição \_ do 0x05 ESTENDIdo**</dt> <dt></dt> </dl>              | Uma partição estendida.<br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <dt>**Partição \_ do FAT \_ 12**</dt> <dt>0x01</dt> </dl>                   | Uma partição do sistema de arquivos FAT12.<br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <dt>**Partição \_ do FAT \_ 16**</dt> <dt>0x04</dt> </dl>                   | Uma partição do sistema de arquivos FAT16.<br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <dt>**Partição \_ do**</dt> <dt>0X0B</dt> de FAT32 </dl>                       | Uma partição do sistema de arquivos FAT32.<br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <dt>**Partição \_ do**</dt> <dt>0x07</dt> IFS </dl>                             | Uma partição IFS.<br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <dt>**Partição \_ do**</dt> <dt>0x42</dt> LDM </dl>                             | Uma partição LDM (Gerenciador de discos lógicos).<br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <dt>**Partição \_ do NTFT**</dt> <dt>0x80</dt> </dl>                          | Uma partição NTFT.<br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <dt>**Válido \_ NTFT**</dt> <dt>0xC0</dt> </dl>                                      | Uma partição NTFT válida.<br/> O alto bit de um código de tipo de partição indica que uma partição faz parte de um espelho NTFT ou uma matriz distribuída.<br/> |



## <a name="remarks"></a>Comentários

Há várias macros que podem ajudá-lo a detectar o tipo de partição: **IsContainerPartition**, **IsFTPartition** e **IsRecognizedPartition**. Para obter mais informações, consulte WinIoCtl. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>WinIoCtl. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**informações de partição \_ \_ ex**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[**informações de partição \_ \_ MBR**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[**DEFINIR \_ informações de partição \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




