---
description: Permite que o cliente chame o objeto de provedor de conclusão automática do Painel de Entrada de Texto do aplicativo.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Interface ITipAutocompleteClient (TipAutoComplete.h)
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
ms.openlocfilehash: dac9b1a6c581be8a8fb19df4f812a5866403d949d19739bb8ae99a0fffbe5e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590286"
---
# <a name="itipautocompleteclient-interface"></a>Interface ITipAutocompleteClient

Permite que o cliente chame o objeto de provedor de conclusão automática do Painel de Entrada de Texto do aplicativo.

## <a name="members"></a>Membros

A interface **ITipAutocompleteClient** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITipAutocompleteClient** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITipAutocompleteClient** tem esses métodos.



| Método                                                              | Descrição                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdviseProvider**](itipautocompleteclient-adviseprovider.md)     | Registra o provedor com o cliente para permitir que o cliente chame o objeto de provedor de conclusão automática do aplicativo.<br/>                                      |
| [**PreferredRects**](itipautocompleteclient-preferredrects.md)     | Permite que o cliente sugira onde posicionar a lista de conclusão automática para evitar a sobreposição do Painel de Entrada.<br/>                                               |
| [**RequestShowUI**](itipautocompleteclient-requestshowui.md)       | Determina se o Painel de Entrada está pronto para ter a lista de conclusão automática mostrada.<br/>                                                                             |
| [**UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) | Não registrou o provedor associado.<br/>                                                                                                                      |
| [**UserSelection**](itipautocompleteclient-userselection.md)       | Notifica o Painel de Entrada de que o usuário selecionou algo na lista de conclusão automática e para descartar todo o texto restante que ainda não foi inserido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| Cabeçalho<br/>                   | <dl> <dt>TipAutoComplete.h (também requer Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



 

