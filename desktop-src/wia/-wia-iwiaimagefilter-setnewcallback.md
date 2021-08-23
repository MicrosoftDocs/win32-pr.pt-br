---
description: Define um novo retorno de chamada de aplicativo para o filtro de processamento de imagem a ser usado para chamadas de encaminhamento.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'Método IWiaImageFilter:: SetNewCallback (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: abb279faba1c5174fc39ebdfe30a4a8cde8cabf86e8b86599f8d3ab9cc3247cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450486"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a>Método IWiaImageFilter:: SetNewCallback

Define um novo retorno de chamada de aplicativo para o filtro de processamento de imagem a ser usado para chamadas de encaminhamento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWiaTransferCallback* \[ no\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**

Especifica um ponteiro para a interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) do aplicativo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Não chame esse método diretamente do seu aplicativo.

O filtro de processamento de imagem é necessário para liberar a interface de retorno de chamada de aplicativo armazenada anteriormente antes de definir o novo retorno de chamada.

Se *pWiaTransferCallback* for **NULL**, o filtro de processamento de imagem deverá simplesmente liberar o retorno de chamada do aplicativo antigo e retornar os S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




