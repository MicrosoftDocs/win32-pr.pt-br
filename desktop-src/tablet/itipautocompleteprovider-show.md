---
description: Exibe ou oculta a lista de preenchimento automático.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'Método ITipAutocompleteProvider:: show (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 950358ae28d1cb68af803ed6b7f520f1bbad8c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663260"
---
# <a name="itipautocompleteprovidershow-method"></a>Método ITipAutocompleteProvider:: show

Exibe ou oculta a lista de preenchimento automático.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fshow* \[ no\]
</dt> <dd>

**True** para mostrar a interface do usuário de preenchimento automático, **false** para ocultar a interface do usuário da lista de preenchimento automático.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é chamado pelo cliente para mostrar ou ocultar a lista de preenchimento automático. Se a lista de preenchimento automático não for exibida e *fshow* for **false**, esse método não fará nada. Se a lista de preenchimento automático for exibida e *fshow* for **true**, esse método não fará nada.

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

 

 




