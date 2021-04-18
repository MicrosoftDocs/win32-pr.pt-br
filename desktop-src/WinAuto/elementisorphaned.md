---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789326"
---
# <a name="elementisorphaned"></a>ElementIsOrphaned

## <a name="text"></a>Texto

O elemento é um IAccessible órfão na árvore

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

O endereço da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do objeto obtido para as coordenadas fornecidas é uma referência a um elemento órfão na árvore de elementos.

Esse problema é um problema para as pessoas que contam com um leitor de tela e um teclado para navegação porque os elementos serão tratados como invisíveis e não serão anunciados para o usuário.

## <a name="possible-causes"></a>Possíveis causas

-   A interação do usuário durante a verificação, como a movimentação do foco para um HWND não-alvo, interfere no processo de verificação.
-   Uma implementação de MSAA incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Navegação por meio de teste de clique e local da tela](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




