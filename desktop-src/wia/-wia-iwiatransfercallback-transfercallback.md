---
description: Fornece o progresso e outras notificações durante uma transferência.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'Método IWiaTransferCallback:: TransferCallback (WIA. h)'
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
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783750"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a>Método IWiaTransferCallback:: TransferCallback

Fornece o progresso e outras notificações durante uma transferência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Atualmente não utilizado. Deve ser definido como zero.

</dd> <dt>

*pWiaTransferParams* \[ no\]
</dt> <dd>

Tipo: **[**WiaTransferParams**](-wia-wiatransferparams.md) \** _

Especifica um ponteiro para uma estrutura [_ *WiaTransferParams* *](-wia-wiatransferparams.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Quando esse método é implementado por um filtro de processamento de imagem, a minidriver de aquisição de imagens do Windows (WIA) 2,0 o chama durante a aquisição da imagem para enviar mensagens de progresso de volta ao aplicativo.

**IWiaTransferCallback:: TransferCallback** de um filtro deve delegar ao método **IWiaTransferCallback:: TransferCallback** do retorno de chamada do aplicativo. Normalmente, o fluxo de filtro filtra os dados passados para ele e grava os dados filtrados diretamente no fluxo fornecido pelo aplicativo. Quando o filtro de processamento de imagens armazena dados entre chamadas para seu método [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , ele também deve modificar os valores *lPercentComplete* e *ulBytesWrittenToCurrentStream* na estrutura [**WiaTransferParams**](-wia-wiatransferparams.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
