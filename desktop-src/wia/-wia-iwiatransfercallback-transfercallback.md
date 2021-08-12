---
description: Fornece progresso e outras notificações durante uma transferência.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: Método IWiaTransferCallback::TransferCallback (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 02c24f4cb1795e233fbbbb3dc30ad1bbb3624e104d59ac72f8e310bbbd323820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440314"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a>Método IWiaTransferCallback::TransferCallback

Fornece progresso e outras notificações durante uma transferência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ Em\]
</dt> <dd>

Tipo: **LONG**

Atualmente não éusado. Deve ser definido como zero.

</dd> <dt>

*pWiaTransferParams* \[ Em\]
</dt> <dd>

Tipo: **[ **WiaTransferParams**](-wia-wiatransferparams.md)\***

Especifica um ponteiro para uma [**estrutura WiaTransferParams.**](-wia-wiatransferparams.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Quando esse método é implementado por um filtro de processamento de imagem, o minidriver WIA (Aquisição de Imagem) 2.0 do Windows chama durante a aquisição de imagem para enviar mensagens de progresso de volta para o aplicativo.

**IWiaTransferCallback::TransferCallback** de um filtro deve delegar ao método **IWiaTransferCallback::TransferCallback** do retorno de chamada do aplicativo. Normalmente, o fluxo de filtro filtra os dados passados para ele e grava os dados filtrados diretamente no fluxo fornecido pelo aplicativo. Quando o filtro de processamento de imagem armazena dados entre chamadas para seu método [IStream::Write,](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) ele também deve modificar os valores *lPercentComplete* e *ulBytesWrittenToCurrentStream* na estrutura [**WiaTransferParams.**](-wia-wiatransferparams.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
