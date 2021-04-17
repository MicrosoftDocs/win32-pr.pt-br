---
description: Permite que o cliente chame o objeto de provedor de preenchimento automático do painel de entrada de texto do aplicativo.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Interface ITipAutocompleteClient (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808313"
---
# <a name="itipautocompleteclient-interface"></a>Interface ITipAutocompleteClient

Permite que o cliente chame o objeto de provedor de preenchimento automático do painel de entrada de texto do aplicativo.

## <a name="members"></a>Membros

A interface **ITipAutocompleteClient** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITipAutocompleteClient** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITipAutocompleteClient** tem esses métodos.



| Método                                                              | Descrição                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aconselheprovider**](itipautocompleteclient-adviseprovider.md)     | Registra o provedor com o cliente para permitir que o cliente chame o objeto de provedor de preenchimento automático do aplicativo.<br/>                                      |
| [**PreferredRects**](itipautocompleteclient-preferredrects.md)     | Permite que o cliente sugira onde posicionar a lista de preenchimento automático para evitar sobreposição do painel de entrada.<br/>                                               |
| [**RequestShowUI**](itipautocompleteclient-requestshowui.md)       | Determina se o painel de entrada está pronto para que a lista de preenchimento automático seja mostrada.<br/>                                                                             |
| [**Unaconselheprovider**](itipautocompleteclient-unadviseprovider.md) | Cancela o registro do provedor associado.<br/>                                                                                                                      |
| [**Userseleções**](itipautocompleteclient-userselection.md)       | Notifica o painel de entrada que o usuário selecionou algo na lista de preenchimento automático e para descartar todo o texto restante que ainda não foi inserido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| parâmetro<br/>                   | <dl> <dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



 

