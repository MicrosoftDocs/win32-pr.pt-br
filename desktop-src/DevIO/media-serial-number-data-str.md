---
description: Contém o número de série de um dispositivo USB. Ele é usado pelo código de \_ controle do número de série do armazenamento do IOCTL \_ Get \_ Media \_ \_ .
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: Estrutura de MEDIA_SERIAL_NUMBER_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: cbb007769238f0e6a4239366e8fe9956e61f892f7d3c98f2b638dc425dc9359f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053476"
---
# <a name="media_serial_number_data-structure"></a>\_Estrutura de \_ dados do número de série da mídia \_

Contém o número de série de um dispositivo USB. Ele é usado pelo código de controle do [**número de série do armazenamento do IOCTL \_ \_ Get \_ Media \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**SerialNumberLength**
</dt> <dd>

O tamanho da cadeia de caracteres **SerialNumberData** , em bytes.

</dd> <dt>

**Resultado**
</dt> <dd>

O status da solicitação.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**SerialNumberData**
</dt> <dd>

O número de série do dispositivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum arquivo de cabeçalho está disponível para a estrutura de **dados do número de série de mídia \_ \_ \_** . Inclua a definição de estrutura na parte superior desta página em seu código-fonte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>          |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**armazenamento de IOCTL \_ \_ obter \_ número de série de mídia \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




