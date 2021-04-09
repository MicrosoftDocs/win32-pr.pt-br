---
description: Usado pelo cliente de preenchimento automático para notificar o aplicativo sobre o texto que um usuário tem Inked no painel de entrada.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'Método ITipAutocompleteProvider:: UpdatePendingText (TipAutoComplete. h)'
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
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011820"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a>Método ITipAutocompleteProvider:: UpdatePendingText

Usado pelo cliente de preenchimento automático para notificar o aplicativo sobre o texto que um usuário tem Inked no painel de entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrPendingText* \[ no\]
</dt> <dd>

O texto de origem a ser usado para gerar a lista de preenchimento automático.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse texto não conterá o texto já inserido no campo focalizado. O provedor de preenchimento automático é responsável por levar em conta o texto do campo atual e a seleção para gerar a lista de preenchimento automático. Quando *bstrPendingText* é **nulo**, a lista de preenchimento automático é gerada com o texto atual à esquerda da seleção no campo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| parâmetro<br/>                   | <dl> <dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITipAutocompleteProvider**](itipautocompleteprovider.md)
</dt> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




