---
title: ElementIsChildOfParentMulipleTimes
description: ElementIsChildOfParentMulipleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27c66027f7948dfa794c85dace015565d636c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160506"
---
# <a name="elementischildofparentmulipletimes"></a>ElementIsChildOfParentMulipleTimes

## <a name="text"></a>Texto

AccParent do elemento é ( {0} ), mas o elemento original é um {1} período filho

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Quando [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) é chamado no elemento de destino, ele relata ser filho do mesmo pai várias vezes.

Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a passagem de elementos pode ser irregular e imprevisível.

## <a name="possible-causes"></a>Possíveis causas

Uma implementação de MSAA incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




