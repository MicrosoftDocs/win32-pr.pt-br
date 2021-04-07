---
description: Descrição do uso de controles de cliente para o Tablet PC.
ms.assetid: 43d78acd-1f02-417d-97be-1682e90a81a2
title: Usando controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c713d2b3912d2bbe4a689c7d8d05d4d977a6eb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827077"
---
# <a name="using-custom-controls"></a>Usando controles personalizados

Você pode personalizar controles padrão usando o desenho de proprietário para alterar a aparência do controle e estabelecer uma superclasse ou subclasse para alterar o comportamento do controle. Em cada caso, o código do sistema subjacente para o tipo de controle padrão manipula funções de controle básicas. A maioria desses controles pode ser acessível se você usá-los corretamente.

Um controle desenhado pelo proprietário baseado em um controle padrão é exibido como o controle padrão para auxílios de acessibilidade e dá suporte ao Microsoft Acessibilidade Ativa; no entanto, ele tem uma aparência personalizada. Alguns aplicativos usam controles personalizados para alterar a aparência de um controle, mas os controles desenhados pelo proprietário são uma solução mais acessível. Para obter mais informações sobre como definir os menus desenhados pelo proprietário e expor controles desenhados pelo proprietário, consulte [acessibilidade](../accessibility/accessibility.md).

Estabelecer uma superclasse ou subclasse é uma técnica para personalizar o comportamento de controles existentes. Dependendo do novo comportamento do controle, pode ser necessário complementar as informações de acessibilidade que ele expõe. Por exemplo, um aplicativo pode usar um controle desenhado pelo proprietário para exibir um X em uma caixa de seleção selecionada, em vez de uma marca de seleção, ou rotular um botão de comando com uma imagem em vez de uma palavra.

Ao usar controles desenhados pelo proprietário que são uma superclasse ou uma subclasse:

-   Forneça rótulos para todos os controles, mesmo quando os rótulos não estiverem visíveis na tela. Se você personalizar um controle para que a legenda padrão não seja visível (por exemplo, um botão com uma face gráfica) e deixe a legenda como uma cadeia de caracteres em branco, o auxílio de acessibilidade não poderá obter a legenda e usá-la para identificar o controle.
-   Verifique se o [**WM \_ gettext**](../winmsg/wm-gettext.md) tem suporte.
-   Certifique-se de que todas as mensagens específicas de classe têm suporte. É especialmente importante dar suporte a mensagens de recuperação de texto, como [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) e [**lb \_ gettext**](../controls/lb-gettext.md). Defina os bits de estilo apropriados, como **CBS \_ HASSTRINGS** e **lbs \_ HASSTRINGS**, para indicar que o controle oferece suporte a essas mensagens.

 

 
