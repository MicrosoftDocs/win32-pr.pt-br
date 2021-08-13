---
description: O WiaTransferParams é transmitido para um aplicativo durante uma transferência de dados pelo sistema de tempo de run-time wia (aquisição de imagem) do Windows para o método IWiaTransferCallback::TransferCallback.
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Estrutura WiaTransferParams (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 7d128a39ff5d9d29bf0766273adaace7eae86b10c9556284c1f5b6f1c9285d30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449897"
---
# <a name="wiatransferparams-structure"></a>Estrutura WiaTransferParams

O **WiaTransferParams** é transmitido para um aplicativo durante uma transferência de dados pelo sistema de tempo de run-time wia (aquisição de imagem) do Windows para o [**método IWiaTransferCallback::TransferCallback.**](-wia-iwiatransfercallback-transfercallback.md)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a>Membros

<dl> <dt>

**lMessage**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Indica o status da transferência de dados.

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**STATUS DO \_ WIA TRANSFER \_ MSG \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA \_ TRANSFER \_ MSG \_ END \_ OF \_ STREAM**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA \_ TRANSFER \_ MSG \_ END \_ OF \_ TRANSFER**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**STATUS DO \_ DISPOSITIVO WIA TRANSFER \_ MSG \_ \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**NOVA PÁGINA DO \_ WIA TRANSFER \_ MSG \_ \_**


</dt> <dd></dd> </dl> </dd> <dt>

**lPercentComplete**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Indica o progresso da transferência de dados como um percentual.

</dd> <dt>

**ulTransferredBytes**
</dt> <dd>

Tipo: **ULONG64**

</dd> <dd>

Indica a quantidade de dados transferidos.

</dd> <dt>

**hrErrorStatus**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

O status ou o estado de erro do dispositivo definido pelo driver; por exemplo, "aquecimento".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 




