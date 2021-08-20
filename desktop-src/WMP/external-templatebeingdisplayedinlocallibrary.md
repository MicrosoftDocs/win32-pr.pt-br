---
title: External.templateBeingDisplayedInLocalLibrary
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External.templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- External.templateBeingDisplayedInLocalLibrary Windows Media Player
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8292e2527fe14ec00a2bf7169b4e2ea2ca4c8229672625712ed3ad3a10e421e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648266"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a>External.templateBeingDisplayedInLocalLibrary

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A **propriedade templateBeingDisplayedInLocalLibrary** indica se o feed representado pela página de descoberta atual está sendo exibido no controle de exibição de árvore da biblioteca local.

## <a name="syntax"></a>Syntax

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um booliana **somente leitura.** **TRUE** indica que o feed está sendo exibido no controle de exibição de árvore da biblioteca local.

## <a name="remarks"></a>Comentários

Uma página de descoberta que representa um feed para uma playlist dinâmica pode exibir um botão que permite ao usuário "salvar" o feed em sua biblioteca local. Salvar o feed, nesse contexto, significa que alguns metadados são salvos no computador do usuário e o feed é listado no nó **Playlists** no controle de exibição de árvore da biblioteca local. O script na página de descoberta pode inspecionar a propriedade **templateBeingDisplayedInLocalLibrary** para determinar se o usuário já salvou o feed na biblioteca local. Se o usuário já tiver salvo o feed, a página de descoberta não deverá exibir o botão Salvar.

Uma página de descoberta que representa um feed de rádio deve inspecionar a **propriedade templateBeingDisplayedInLocalLibrary** pelo mesmo motivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para lojas online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





