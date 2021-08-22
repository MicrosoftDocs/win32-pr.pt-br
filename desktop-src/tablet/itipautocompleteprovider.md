---
description: Gerencia a integração automática do lado do aplicativo do Painel de Entrada de Texto.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Interface ITipAutocompleteProvider (TipAutoComplete.h)
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
ms.openlocfilehash: 66c1e38c419e7eb37745864b447249d55b384b6c832293bd3fab4d0cc171e0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031864"
---
# <a name="itipautocompleteprovider-interface"></a>Interface ITipAutocompleteProvider

Gerencia a integração automática do lado do aplicativo do Painel de Entrada de Texto.

## <a name="members"></a>Membros

A interface **ITipAutocompleteProvider** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITipAutocompleteProvider** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITipAutocompleteProvider** tem esses métodos.



| Método                                                                  | Descrição                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**programa**](itipautocompleteprovider-show.md)                           | Exibe ou oculta a lista de conclusão automática.<br/>                                                                 |
| [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md) | Usado pelo cliente de conclusão automática para notificar o aplicativo do texto que um usuário usou no Painel de Entrada.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| Cabeçalho<br/>                   | <dl> <dt>TipAutoComplete.h (também requer Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> <dt>

[**ITipAutocompleteClient Interface**](itipautocompleteclient.md)
</dt> </dl>

 

