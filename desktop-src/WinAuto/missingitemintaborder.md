---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641154"
---
# <a name="missingitemintaborder"></a>MissingItemInTabOrder

## <a name="text"></a>Texto

Esse elemento parece ser tabulado, mas não está na ordem de tabulação.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Um elemento que pode ser focalizado não é acessível usando a navegação de teclado padrão (TAB ou Shift + Tab). Por exemplo, o elemento não foi marcado como uma parada de tabulação ou um índice de tabulação foi atribuído. Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque:

-   O elemento não é detectável.
-   Se o elemento for um filho de um controle de lista personalizado, as indicações indicando que o elemento filho pode ser navegado usando as teclas de seta ou de página podem estar ausentes.

## <a name="possible-causes"></a>Possíveis causas

-   A função MSAA do elemento ou seu pai não está definido corretamente. Por exemplo, se todos os itens de lista em um controle de exibição de lista não forem expostos por meio de MSAA como uma ListItem de sistema de função \_ \_ , a verificação falhará porque os itens de lista não estão acessíveis usando a tecla Tab.
-   O elemento ou seu pai é um controle personalizado que não implementa a Tabulação corretamente. Por exemplo, a propriedade de estado MSAA nunca é configurada para o estado do \_ sistema em \_ foco.
-   Um elemento que atua como um contêiner para outros elementos foi selecionado para verificação, mas não dá suporte à navegação de teclado em si. Por exemplo, uma barra de ferramentas e seus elementos filho não podem ser acessados usando a tecla TAB.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes para design de interface de usuário de teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 