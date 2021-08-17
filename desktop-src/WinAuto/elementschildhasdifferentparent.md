---
title: ElementsChildHasDifferentParent
description: ElementsChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 885a5d930892d6e202764de8e58371f02690edee6715155f34533aaa110d7080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829176"
---
# <a name="elementschildhasdifferentparent"></a>ElementsChildHasDifferentParent

## <a name="text"></a>Texto

O filho do elemento ( {0} ) tem um elemento pai ( {1} ) diferente

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro indica que, quando [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) é chamado nos filhos do elemento Target, os filhos não relatam um pai consistente.

![um exemplo dos filhos de um elemento que relata um pai inconsistente](images/accchecker-inconsistent-parent.png)

Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a passagem de elementos pode ser irregular e imprevisível.

## <a name="possible-causes"></a>Possíveis causas

Uma implementação de MSAA incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




