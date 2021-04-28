---
description: Estrutura de STORAGE_HW_FIRMWARE_INFO_QUERY-essa estrutura contém informações sobre o firmware do dispositivo.
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: Estrutura de STORAGE_HW_FIRMWARE_INFO_QUERY (Winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: ffda37d918406a696a29a9bf2903424523c3b830
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119394"
---
# <a name="storage_hw_firmware_info_query-structure"></a>\_Estrutura de \_ consulta de informações de firmware de hardware de \_ armazenamento \_

Essa estrutura contém informações sobre o firmware do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a>Membros

<dl> <dt>

**Versão**
</dt> <dd>

A versão desta estrutura. Isso deve ser definido como sizeof (consulta de informações de firmware de hardware de armazenamento \_ \_ \_ \_ )

</dd> <dt>

**Tamanho**
</dt> <dd>

O tamanho dessa estrutura como um buffer.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Os sinalizadores associados à consulta. Os seguintes são sinalizadores que podem ser definidos neste membro.



| Sinalizador                                             | Descrição                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| \_controlador de \_ \_ sinalizador de solicitação de firmware HW \_ de \_ armazenamento | Indica que o destino da solicitação não é o próprio dispositivo ou o próprio objeto. |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Winioctl. h. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

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

[**\_informações de \_ slot de firmware de hardware de armazenamento \_ \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




