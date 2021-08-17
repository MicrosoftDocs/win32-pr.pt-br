---
description: Usado pelo cliente de conclusão automática para notificar o aplicativo do texto que um usuário usou no Painel de Entrada.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: Método ITipAutocompleteProvider::UpdatePendingText (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 99fc67b5ba6495e2bdfb8a54de2412ca01cbdd37475d08d20d227b203f2da1bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716426"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a>Método ITipAutocompleteProvider::UpdatePendingText

Usado pelo cliente de conclusão automática para notificar o aplicativo do texto que um usuário usou no Painel de Entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrPendingText* \[ Em\]
</dt> <dd>

Texto de origem a ser usado para gerar a lista de conclusão automática.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse texto não conterá o texto já inserido no campo focalizado. O provedor de conclusão automática é responsável por levar em conta o texto do campo atual e a seleção para gerar a lista de conclusão automática. Quando *bstrPendingText* é **NULL,** a lista de conclusão automática é gerada com o texto atual à esquerda da seleção no campo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| Cabeçalho<br/>                   | <dl> <dt>TipAutoComplete.h (também requer Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITipAutocompleteProvider Interface**](itipautocompleteprovider.md)
</dt> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




