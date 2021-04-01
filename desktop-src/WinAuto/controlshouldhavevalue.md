---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159976"
---
# <a name="controlshouldhavevalue"></a>ControlShouldHaveValue

## <a name="text"></a>Texto

Um controle com a função de {0} deve ter um valor, mas get \_ accValue não está implementado

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Um elemento não fornece um valor conforme esperado com base na função de MSAA atribuída, implicando que o elemento não tem o método [**Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) implementado. Por exemplo, as seguintes funções de MSAA devem fornecer um valor.

-   \_ComboBox do sistema de funções \_
-   \_IPAddress do sistema de função \_
-   \_link do sistema de funções \_
-   \_OUTLINEITEM do sistema de função \_
-   \_PROGRESSBAR do sistema de funções \_
-   \_controle deslizante do sistema de funções \_
-   \_SPINBUTTON do sistema de funções \_
-   \_barra de rolagem do sistema de funções \_
-   \_texto do sistema de função \_

Esse problema é um problema para as pessoas que contam com um leitor de tela e um teclado para navegação porque um elemento que tem um valor intrínseco deve ser capaz de relatar esse valor a um usuário.

## <a name="possible-causes"></a>Possíveis causas

O elemento ou seu pai tem uma função de MSAA definida incorretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Funções de objeto**](object-roles.md)
</dt> </dl>

 

 




