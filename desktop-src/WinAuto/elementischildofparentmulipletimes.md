---
title: ElementIsChildOfParentMulipleTimes
description: ElementIsChildOfParentMulipleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfed0716423d8b1fef182be7cb0cb8ef122cf70cff6a574069fe40b63549f744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829545"
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

 

 




