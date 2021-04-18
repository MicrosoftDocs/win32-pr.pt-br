---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793936"
---
# <a name="invalidrole"></a>InvalidRole

## <a name="text"></a>Texto

O int retornado de get \_ accRole não é uma constante de função válida, sistema de função do IE \_\_\*

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Um elemento está relatando uma função de MSAA inválida. Por exemplo, o método [**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) retorna um valor inteiro que não é mapeado para uma constante de função de objeto válida (como \_ ListItem de sistema de função \_ ).

Esse problema causa problemas para as pessoas que dependem de um leitor de tela e teclado para navegação porque os elementos podem ser identificados incorretamente para o usuário.

## <a name="possible-causes"></a>Possíveis causas

O elemento ou seu pai tem uma função de MSAA definida incorretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Funções de objeto**](object-roles.md)
</dt> </dl>

 

 




