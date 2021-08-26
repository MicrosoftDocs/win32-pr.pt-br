---
description: STORAGE_HW_FIRMWARE_INFO estrutura - essa estrutura contém informações sobre o firmware do dispositivo.
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: STORAGE_HW_FIRMWARE_INFO (Winioctl.h)
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
ms.openlocfilehash: 1b9aa008e108f1282f8f61aaeacdce11eba7016632fa9643ae3db5550efb1e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047906"
---
# <a name="storage_hw_firmware_info-structure"></a>Estrutura STORAGE \_ HW \_ FIRMWARE \_ INFO

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

A versão dessa estrutura. Isso deve ser definido como sizeof(STORAGE \_ HW \_ FIRMWARE \_ INFO)

</dd> <dt>

**Tamanho**
</dt> <dd>

O tamanho dessa estrutura como um buffer, incluindo slot.

</dd> <dt>

**SupportUpgrade**
</dt> <dd>

Indica que esse firmware dá suporte a uma atualização.

</dd> <dt>

**Reservado0**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**SlotCount**
</dt> <dd>

O número de slots de firmware no dispositivo. Essa é a dimensão da matriz slot.

> [!Note]  
> Alguns dispositivos podem armazenar mais de uma imagem de firmware, se eles têm mais de 1 slot de firmware.

 

</dd> <dt>

**ActiveSlot**
</dt> <dd>

O slot de firmware que contém a imagem de firmware ativa/em execução no momento.

</dd> <dt>

**PendingActivateSlot**
</dt> <dd>

O slot de firmware que está pendente de ativação.

</dd> <dt>

**FirmwareShared**
</dt> <dd>

Indica que o firmware se aplica ao dispositivo e ao controlador/adaptador, por exemplo, NVMe SSD.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**ImagePayloadAlignment**
</dt> <dd>

O alinhamento da carga da imagem, em número de bytes. O máximo é TAMANHO DA \_ PÁGINA. O tamanho da transferência é uma mutlíptica desse tamanho. Alguns protocolos exigem pelo menos o tamanho do setor. Quando esse valor é definido como 0, isso significa que esse valor é inválido.

</dd> <dt>

**ImagePayloadMaxSize**
</dt> <dd>

O tamanho máximo do payload da imagem, que é usado para um único comando.

</dd> <dt>

**Slot**
</dt> <dd>

Contém as informações de slot para cada slot no dispositivo, do tipo [**STORAGE \_ HW \_ FIRMWARE SLOT \_ \_ INFO**](storage-hw-firmware-slot-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                                 |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Winioctl.h.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOCTL \_ STORAGE \_ FIRMWARE \_ ACTIVATE**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**ATIVAÇÃO \_ DO FIRMWARE HW \_ DE \_ ARMAZENAMENTO**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**DOWNLOAD DO FIRMWARE DE ARMAZENAMENTO IOCTL \_ \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**DOWNLOAD \_ DO FIRMWARE DO HW DE \_ \_ ARMAZENAMENTO**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**OBTER INFORMAÇÕES SOBRE O \_ FIRMWARE DE \_ ARMAZENAMENTO \_ IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**CONSULTA DE \_ INFORMAÇÕES DE FIRMWARE HW DE \_ \_ \_ ARMAZENAMENTO**](storage-hw-firmware-info-query.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO SLOT DE FIRMWARE HW DE \_ \_ \_ ARMAZENAMENTO**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




