---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate \_ ReturnedElementWithIncorrectParent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd040cda80e9dcb19543c8ee5134271693546dfdb8af76053b5a281340080765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122457"
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

 

 




