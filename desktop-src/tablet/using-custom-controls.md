---
description: Descrição do uso de controles de cliente para o Tablet PC.
ms.assetid: 43d78acd-1f02-417d-97be-1682e90a81a2
title: Usando controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70699a141f0319f917953e25363db0e0cd38eb21ecc06345c581b55526ad6bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119551876"
---
# <a name="using-custom-controls"></a>Usando controles personalizados

Você pode personalizar os controles padrão usando o desenho de proprietário para alterar a aparência do controle e estabelecer uma superclasse ou subclasse para alterar o comportamento do controle. Em cada caso, o código do sistema subjacente para o tipo de controle padrão lida com funções de controle básicas. A maioria desses controles poderá ser acessível se você usá-los corretamente.

Um controle desenhado pelo proprietário baseado em um controle padrão aparece como o controle padrão para auxiliares de acessibilidade e dá suporte a Microsoft Active Accessibility; no entanto, ele tem uma aparência personalizada. Alguns aplicativos usam controles personalizados para alterar a aparência de um controle, mas os controles desenhados pelo proprietário são uma solução mais acessível. Para obter mais informações sobre como definir menus desenhados pelo proprietário e expor controles desenhados pelo proprietário, consulte [Acessibilidade](../accessibility/accessibility.md).

Estabelecer uma superclasse ou subclasse é uma técnica para personalizar o comportamento dos controles existentes. Dependendo do novo comportamento do controle, pode ser necessário complementar as informações de acessibilidade que ele expõe. Por exemplo, um aplicativo pode usar um controle desenhado pelo proprietário para exibir um X em uma caixa de seleção selecionada, em vez de uma marca de seleção, ou rotular um botão de comando com uma imagem em vez de uma palavra.

Ao usar controles desenhados pelo proprietário que são uma superclasse ou uma subclasse:

-   Forneça rótulos para todos os controles, mesmo quando os rótulos não estão visíveis na tela. Se você personalizar um controle para que a legenda padrão não fique visível (por exemplo, um botão com uma face gráfica) e deixe a legenda como uma cadeia de caracteres em branco, o auxiliar de acessibilidade não poderá obter a legenda e usá-la para identificar o controle.
-   Verifique se [**há suporte para WM \_ GETTEXT.**](../winmsg/wm-gettext.md)
-   Verifique se há suporte para todas as mensagens específicas da classe. É especialmente importante dar suporte a mensagens de recuperação de texto, como [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) e [**LB \_ GETTEXT.**](../controls/lb-gettext.md) De definir os bits de estilo apropriados, como **CBS \_ HASSTRINGS** e **LBS \_ HASSTRINGS,** para indicar que o controle dá suporte a essas mensagens.

 

 
