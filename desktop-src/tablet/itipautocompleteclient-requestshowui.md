---
description: Determina se o painel de entrada está pronto para que a lista de preenchimento automático seja mostrada.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'Método ITipAutocompleteClient:: RequestShowUI (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 4288a506e14ae8096db9be051e3282bb2ebd62522988d75574f3e56070419fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449789"
---
# <a name="itipautocompleteclientrequestshowui-method"></a>Método ITipAutocompleteClient:: RequestShowUI

Determina se o painel de entrada está pronto para que a lista de preenchimento automático seja mostrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hWndACList* \[ no\]
</dt> <dd>

Identificador de janela da interface do usuário da lista de preenchimento automático.

</dd> <dt>

*pfAllowShowing* \[ fora\]
</dt> <dd>

**False** se o cliente recomendar não mostrar a interface de usuário da lista de preenchimento automático. **True** se o provedor de preenchimento automático puder mostrar a interface do usuário da lista.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é chamado pelo provedor de preenchimento automático quando está prestes a mostrar a interface do usuário de preenchimento automático. Se o estado interno do cliente não permitir que o provedor mostre a interface do usuário, *pfAllowShowing* será definido como **false**. Por exemplo, quando o texto é enviado para o campo da capa de manuscrito no painel de entrada do Tablet PC e o usuário inicia imediatamente a tinta, o cliente recomendará não mostrar a interface do usuário de preenchimento automático, para evitar a destruição da tinta do usuário, definindo *pfAllowShowing* como **false**.

Chame **RequestShowUI** para definir o identificador de janela de lista de preenchimento automático de pop-up antes de chamar o [**método ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md). A falha em fazer isso causará um erro **E \_ INVALIDARG** ao chamar **PreferredRects**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| Cabeçalho<br/>                   | <dl> <dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[**ITipAutocompleteClient: método referredRects de:P**](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




