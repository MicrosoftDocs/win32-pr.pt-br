---
description: Gerencia o lado do aplicativo da integração de preenchimento automático do painel de entrada de texto.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Interface ITipAutocompleteProvider (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 3c300e2724ccabbc8388ef647f8f0145531cfc8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772511"
---
# <a name="itipautocompleteprovider-interface"></a>Interface ITipAutocompleteProvider

Gerencia o lado do aplicativo da integração de preenchimento automático do painel de entrada de texto.

## <a name="members"></a>Membros

A interface **ITipAutocompleteProvider** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITipAutocompleteProvider** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITipAutocompleteProvider** tem esses métodos.



| Método                                                                  | Descrição                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**programa**](itipautocompleteprovider-show.md)                           | Exibe ou oculta a lista de preenchimento automático.<br/>                                                                 |
| [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md) | Usado pelo cliente de preenchimento automático para notificar o aplicativo sobre o texto que um usuário tem Inked no painel de entrada.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| parâmetro<br/>                   | <dl> <dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> <dt>

[**Interface ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> </dl>

 

