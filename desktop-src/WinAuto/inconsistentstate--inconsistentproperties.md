---
title: Inconsistent, inconsistent
description: Inconsistent, inconsistent
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635311"
---
# <a name="inconsistentstate-inconsistentproperties"></a>Inconsistent, inconsistent

## <a name="text"></a>Texto

Um controle tem Estados/propriedades que são inconsistentes {0} e {1}

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Um elemento está relatando Estados de MSAA inconsistentes ou conflitantes ou propriedades de automação de interface do usuário. Por exemplo, quando o método [**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) retorna qualquer uma das combinações a seguir.

-   \_Sistema \_ de estado expandido e sistema de estado \_ \_ recolhido
-   \_Sistema \_ de estado selecionado e não \_ sistema de estado \_ selecionável
-   Estado do sistema com foco \_ \_ e não estado do \_ sistema \_

Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque um estado de elemento incorreto pode ser relatado ao usuário.

## <a name="possible-causes"></a>Possíveis causas

O elemento ou seu pai tem um estado de MSAA definido incorretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Constantes de estado do objeto**](object-state-constants.md)
</dt> <dt>

[Estados e propriedades](uiauto-msaa.md)
</dt> </dl>

 

 




