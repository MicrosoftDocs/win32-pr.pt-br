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
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647482"
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

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Não chame esse método diretamente do seu aplicativo.

O filtro de processamento de imagem é necessário para liberar a interface de retorno de chamada de aplicativo armazenada anteriormente antes de definir o novo retorno de chamada.

Se *pWiaTransferCallback* for **NULL**, o filtro de processamento de imagem deverá simplesmente liberar o retorno de chamada do aplicativo antigo e retornar os S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




