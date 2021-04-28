---
description: Estrutura de STORAGE_HW_FIRMWARE_INFO-essa estrutura contém informações sobre o firmware do dispositivo.
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: Estrutura de STORAGE_HW_FIRMWARE_INFO (Winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: e7aa3d33f744b00fc742a2862add83149cb265b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090954"
---
# <a name="storage_hw_firmware_info-structure"></a>\_Estrutura de \_ informações de firmware de hardware de armazenamento \_

Essa estrutura contém informações sobre o firmware do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Versão**
</dt> <dd>

A versão desta estrutura. Isso deve ser definido como sizeof (informações de firmware de hardware de armazenamento \_ \_ \_ )

</dd> <dt>

**Tamanho**
</dt> <dd>

O tamanho dessa estrutura como um buffer, incluindo o slot.

</dd> <dt>

**SupportUpgrade**
</dt> <dd>

Indica que este firmware dá suporte a uma atualização.

</dd> <dt>

**Reserved0**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**SlotCount**
</dt> <dd>

O número de Slots de firmware no dispositivo. Esta é a dimensão da matriz de Slots.

> [!Note]  
> Alguns dispositivos podem armazenar mais de 1 imagem de firmware, se tiverem mais de 1 slot de firmware.

 

</dd> <dt>

**ActiveSlot**
</dt> <dd>

O slot de firmware que contém a imagem de firmware ativa/em execução no momento.

</dd> <dt>

**PendingActivateSlot**
</dt> <dd>

O slot de firmware que está com a ativação pendente.

</dd> <dt>

**FirmwareShared**
</dt> <dd>

Indica que o firmware se aplica ao dispositivo e ao controlador/adaptador, por exemplo, SSD de NVMe.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**ImagePayloadAlignment**
</dt> <dd>

O alinhamento da carga da imagem, em número de bytes. O máximo é o \_ tamanho da página. O tamanho da transferência é um vários desse tamanho. Alguns protocolos exigem pelo menos o tamanho do setor. Quando esse valor é definido como 0, isso significa que esse valor é inválido.

</dd> <dt>

**ImagePayloadMaxSize**
</dt> <dd>

O tamanho máximo da carga da imagem, que é usado para um único comando.

</dd> <dt>

**Slot**
</dt> <dd>

Contém as informações de slot para cada slot no dispositivo, do tipo [**\_ informações de \_ \_ slot \_ de firmware de HW de armazenamento**](storage-hw-firmware-slot-info.md).

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

[**\_consulta de \_ informações de firmware de hardware de armazenamento \_ \_**](storage-hw-firmware-info-query.md)
</dt> <dt>

[**\_informações de \_ slot de firmware de hardware de armazenamento \_ \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




