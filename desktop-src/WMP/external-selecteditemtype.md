---
title: External. selectedItemtype
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. selectedItemtype
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- External. selectedItemtype Windows Media Player
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811102"
---
# <a name="externalselecteditemtype"></a>External. selectedItemtype

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **selecteditemtype** recupera o tipo do item de mídia selecionado no momento no Windows Media Player.

## <a name="syntax"></a>Syntax

janela. external. selectedItemtype ()

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma **cadeia de caracteres** somente leitura que contém uma das [constantes de localização da biblioteca](library-location-constants.md).

## <a name="remarks"></a>Comentários

Essa propriedade é usada em combinação com a propriedade **external. selecteditemid** . Por exemplo, se **selecteditemtype** for igual a CPTrackID, **selecteditemid** será a ID da faixa selecionada. Para obter mais informações sobre como o Windows Media Player caracteriza exibições de conteúdo da loja online, consulte [local e item selecionado](location-and-selected-item.md).

Determinadas exibições no Windows Media Player têm um item de mídia específico selecionado. Por exemplo, suponha que a exibição atual represente um álbum. Um álbum é um contêiner de faixas, portanto **selecteditemtype** é igual a CPTrackID e **selecteditemid** é a ID da faixa selecionada. Outras exibições não têm um item de mídia selecionado. Por exemplo, se o usuário clicar no nó raiz do armazenamento online no controle de exibição de árvore, o Windows Media Player exibirá uma página de descoberta fornecida pela loja online. O Player não exibe nenhum contêiner de itens de mídia na interface do usuário do Player. Nesse caso, **selecteditemtype** é igual a UnknownLocation e **selecteditemid** é igual à cadeia de caracteres vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. selectedItemid**](external-selecteditemid.md)
</dt> <dt>

[**Local e item selecionado**](location-and-selected-item.md)
</dt> </dl>

 

 





