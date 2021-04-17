---
description: Notifica o painel de entrada que o usuário selecionou algo na lista de preenchimento automático e para descartar todo o texto restante que ainda não foi inserido.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: 'Método ITipAutocompleteClient:: userseleções (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1894db9da3b8e3a36e59eb45150b27facfe0291f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812070"
---
# <a name="itipautocompleteclientuserselection-method"></a>Método ITipAutocompleteClient:: userseleções

Notifica o painel de entrada que o usuário selecionou algo na lista de preenchimento automático e para descartar todo o texto restante que ainda não foi inserido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é chamado do provedor para notificar o cliente de que uma seleção foi feita pelo usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| parâmetro<br/>                   | <dl> <dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




