---
title: External. templateBeingDisplayedInLocalLibrary
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- Windows Media Player externo. templateBeingDisplayedInLocalLibrary
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
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758200"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a>External. templateBeingDisplayedInLocalLibrary

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **templateBeingDisplayedInLocalLibrary** indica se o feed representado pela página de descoberta atual está sendo exibido no controle de exibição de árvore de biblioteca local.

## <a name="syntax"></a>Syntax

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **booliano** somente leitura. **Verdadeiro** indica que o feed está sendo exibido no controle de exibição de árvore de biblioteca local.

## <a name="remarks"></a>Comentários

Uma página de descoberta que representa um feed para uma lista de reprodução dinâmica pode exibir um botão que permite ao usuário "salvar" o feed em sua biblioteca local. Salvar o feed, neste contexto, significa que alguns metadados são salvos no computador do usuário e o feed é listado no nó **playlists** no controle de exibição de árvore de biblioteca local. O script na página descoberta pode inspecionar a propriedade **templateBeingDisplayedInLocalLibrary** para determinar se o usuário já salvou o feed na biblioteca local. Se o usuário já tiver salvo o feed, a página de descoberta não deverá exibir o botão salvar.

Uma página de descoberta que representa um feed de rádio deve inspecionar a propriedade **templateBeingDisplayedInLocalLibrary** pelo mesmo motivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





