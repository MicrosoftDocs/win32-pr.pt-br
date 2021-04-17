---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate \_ ReturnedElementWithIncorrectParent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559452"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a>AccNavigate \_ ReturnedElementWithIncorrectParent

## <a name="text"></a>Texto

Chamar accNavigate ((Live Search), 0, NAVDIR \_ FIRSTCHILD) que retornou (x-gadget:///gadget.html) retornou o pai incorreto ( \[ NULL \] ) e não (Live Search)

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Quando [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) é chamado no elemento filho retornado por [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (usando as \_ constantes de navegação NAVDIR FIRSTCHILD ou NAVDIR \_ LASTCHILD), o elemento pai retornado não corresponde ao elemento pai especificado na chamada **accNavigate** .

![exemplo de uma implementação de MSAA inválida que retorna um elemento pai incorreto.](images/accchecker-invalid-msaa-parent.png)

Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a passagem de elementos pode ser irregular e imprevisível.

## <a name="possible-causes"></a>Possíveis causas

Uma implementação de MSAA incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible:: obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




