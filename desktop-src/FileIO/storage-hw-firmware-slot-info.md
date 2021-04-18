---
description: Essa estrutura contém informações sobre um slot em um dispositivo.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: Estrutura de STORAGE_HW_FIRMWARE_SLOT_INFO (Winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767654"
---
# <a name="storage_hw_firmware_slot_info-structure"></a>\_Estrutura de \_ informações do slot do firmware de hardware de \_ armazenamento \_

Essa estrutura contém informações sobre um slot em um dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Versão**
</dt> <dd>

A versão desta estrutura. Isso deve ser definido como sizeof (informações de slot de firmware de hardware de armazenamento \_ \_ \_ \_ )

</dd> <dt>

**Tamanho**
</dt> <dd>

O tamanho desta estrutura.

</dd> <dt>

**SlotNumber**
</dt> <dd>

O número do slot deste slot.

</dd> <dt>

**ReadOnly (somente-leitura)**
</dt> <dd>

Indica se este slot é somente leitura ou não.

</dd> <dt>

**Reserved0**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**Revisão**
</dt> <dd>

A revisão do firmware neste slot.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Winioctl. h. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ativação do \_ firmware de armazenamento do IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**\_ativação do \_ firmware de HW de armazenamento \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**\_download do \_ firmware de armazenamento do IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**\_download de \_ firmware de hardware de armazenamento \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**\_informações de \_ obtenção do firmware de armazenamento do IOCTL \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**\_informações de \_ firmware de hardware de armazenamento \_**](storage-hw-firmware-info.md)
</dt> <dt>

[**\_consulta de \_ informações de firmware de hardware de armazenamento \_ \_**](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




