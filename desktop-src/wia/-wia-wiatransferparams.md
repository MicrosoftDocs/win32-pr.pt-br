---
description: 'O WiaTransferParams é transmitido para um aplicativo durante uma transferência de dados pelo sistema de tempo de execução da aquisição de imagens do Windows (WIA) para o método IWiaTransferCallback:: TransferCallback.'
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Estrutura WiaTransferParams (WIA. h)
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
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783724"
---
# <a name="wiatransferparams-structure"></a>Estrutura WiaTransferParams

O **WiaTransferParams** é transmitido para um aplicativo durante uma transferência de dados pelo sistema de tempo de execução da aquisição de imagens do Windows (WIA) para o método [**IWiaTransferCallback:: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .

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

Tipo: **longo**

</dd> <dd>

Indica o status da transferência de dados.

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**\_status da \_ mensagem de transferência WIA \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ fim \_ do fluxo de mensagens de transferência WIA \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ fim \_ da mensagem de \_ transferência WIA**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**\_status do \_ dispositivo de mensagens de transferência WIA \_ \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**\_ \_ \_ nova página de mensagens de transferência WIA \_**


</dt> <dd></dd> </dl> </dd> <dt>

**lPercentComplete**
</dt> <dd>

Tipo: **longo**

</dd> <dd>

Indica o progresso da transferência de dados como uma porcentagem.

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

O status ou o estado de erro do dispositivo definido pelo driver; por exemplo, "aquecendo".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 




