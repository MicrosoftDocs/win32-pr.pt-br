---
title: Sobre a área de transferência
description: Esta seção aborda a área de transferência.
ms.assetid: 14c91730-a668-495b-9ec6-b835234821a5
keywords:
- área de transferência, sobre
- área de transferência, formatos
- área de transferência, comandos
- área de transferência, Windows
- área de transferência, números de sequência
- área de transferência, visualizadores
- área de transferência, janelas de visualizador
- área de transferência, formatos de exibição
- área de transferência, formatos de exibição de proprietário
- Exibir formatos da área de transferência
- exibição do proprietário exibir formatos da área de transferência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94757a95fb8c40152a0018d04cef64e8efae624
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294382"
---
# <a name="about-the-clipboard"></a>Sobre a área de transferência

A *área de transferência* é um conjunto de funções e mensagens que permitem que os aplicativos transfiram dados. Como todos os aplicativos têm acesso à área de transferência, os dados podem ser facilmente transferidos entre aplicativos ou dentro de um aplicativo.

A área de transferência é controlada pelo usuário. Uma janela deve transferir dados de ou para a área de transferência somente em resposta a um comando do usuário. Uma janela não deve usar a área de transferência para transferir dados sem o conhecimento do usuário.

Um objeto de memória na área de transferência pode estar em qualquer formato de dados, chamado de formato de área de transferência. Cada formato é identificado por um valor inteiro sem sinal. Para formatos de área de transferência padrão (predefinidos), esse valor é uma constante definida em winuser. h; para formatos de área de transferência registrados, é o valor de retorno da função [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) .

Exceto para registrar formatos de área de transferência, as janelas individuais executam a maioria das operações de área de transferência. Normalmente, um procedimento de janela transfere informações de ou para a área de transferência em resposta à mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .

Esta seção discute o seguinte:

-   [Comandos da área de transferência](#clipboard-commands)
-   [Número de sequência da área de transferência](#clipboard-sequence-number)
-   [Visualizadores da área de transferência](#clipboard-viewers)
    -   [Janelas do Visualizador de área de transferência](#clipboard-viewer-windows)
    -   [Formatos de exibição](#display-formats)
    -   [Formato de exibição do proprietário](#owner-display-format)
-   [Tópicos relacionados](#related-topics)

## <a name="clipboard-commands"></a>Comandos da área de transferência

Normalmente, um usuário realiza operações de área de transferência escolhendo comandos no menu **Editar** de um aplicativo. Veja a seguir uma breve descrição dos comandos padrão da área de transferência.



|            |                                                                                                                                                                                                                   |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Recortar**    | Coloca uma cópia da seleção atual na área de transferência e exclui a seleção do documento. O conteúdo anterior da área de transferência é destruído.                                                          |
| **Cópia**   | Coloca uma cópia da seleção atual na área de transferência. O documento permanece inalterado. O conteúdo anterior da área de transferência é destruído.                                                                      |
| **Colar**  | Substitui a seleção atual pelo conteúdo da área de transferência. O conteúdo da área de transferência não é alterado.                                                                                                    |
| **Excluir** | Exclui a seleção atual do documento. O conteúdo da área de transferência não é alterado. Esse comando não envolve a área de transferência, mas deve aparecer com os comandos da área de transferência no menu **Editar** . |



 

## <a name="clipboard-sequence-number"></a>Número de sequência da área de transferência

A área de transferência para cada estação de janela tem um número de sequência da área de transferência associado. Esse número é incrementado sempre que o conteúdo da área de transferência é alterado. Para obter o número de sequência da área de transferência, chame a função [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) .

## <a name="clipboard-viewers"></a>Visualizadores da área de transferência

Um visualizador da área de transferência é uma janela que exibe o conteúdo atual da área de transferência. A janela do Visualizador da área de transferência é uma conveniência para o usuário e não afeta as funções de transação de dados da área de transferência.

Normalmente, uma janela do Visualizador da área de transferência pode exibir pelo menos os três formatos mais comuns: **\_ texto do CF**, **\_ bitmap do CF** e **\_ METAFILEPICT do CF**. Se uma janela não disponibilizar dados em nenhum desses três formatos, ela deve fornecer dados em um formato de exibição ou usar o formato de exibição de proprietário.

Uma *cadeia do Visualizador da área de transferência* é a vinculação entre duas ou mais entidades, de modo que elas dependem umas das outras para a operação. Essa interdependência (cadeia) permite que todos os aplicativos em execução do Visualizador da área de transferência recebam as mensagens enviadas para a área de transferência atual.

Os tópicos a seguir são discutidos nesta seção.

-   [Janelas do Visualizador de área de transferência](#clipboard-viewer-windows)
-   [Formatos de exibição](#display-formats)
-   [Formato de exibição do proprietário](#owner-display-format)

### <a name="clipboard-viewer-windows"></a>Janelas do Visualizador de área de transferência

Uma janela adiciona-se à cadeia do Visualizador da área de transferência chamando a função [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) . O valor de retorno é o identificador para a próxima janela na cadeia. Para recuperar o identificador para a primeira janela na cadeia, chame a função [**GetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer) .

Cada janela do Visualizador da área de transferência deve manter o controle da próxima janela na cadeia do Visualizador da área de transferência. Quando o conteúdo da área de transferência é alterado, o sistema envia uma mensagem do [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) para a primeira janela na cadeia. Depois de atualizar sua exibição, cada janela do Visualizador da área de transferência deve passar essa mensagem para a próxima janela na cadeia.

Antes de fechar, uma janela do Visualizador da área de transferência deve se remover da cadeia do Visualizador da área de transferência chamando a função [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) . Em seguida, o sistema envia uma mensagem do [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) para a primeira janela na cadeia.

Para obter mais informações sobre como processar as mensagens do [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) e do [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) , consulte [criando uma janela do Visualizador da área de transferência](using-the-clipboard.md).

### <a name="display-formats"></a>Formatos de exibição

Um formato de exibição é um formato de área de transferência usado para exibir informações em uma janela do Visualizador da área de transferência. Um proprietário da área de transferência que usa um formato de área de transferência particular ou registrado, e nenhum dos formatos padrão mais comuns, deve fornecer dados em um formato de exibição para exibição em uma janela do Visualizador da área de transferência. Os formatos de exibição são destinados apenas para exibição e não devem ser colados em um documento.

Os quatro formatos de exibição são **: \_ CF DSPBITMAP**, **CF \_ DSPMETAFILEPICT**, **CF \_ DSPTEXT** e **CF \_ DSPENHMETAFILE**. Esses formatos de exibição são renderizados da mesma maneira que os formatos padrão, que são: o **\_ bitmap do CF**, o **\_ texto do CF**, o **CF \_ METAFILEPICT** e o **CF \_ ENHMETAFILE**.

### <a name="owner-display-format"></a>Formato de exibição do proprietário

Para um proprietário da área de transferência que não usa nenhum dos formatos de área de transferência padrão comuns, uma alternativa para fornecer um formato de exibição é usar o formato de área de transferência Owner-display (**CF \_ OWNERDISPLAY**).

Usando o formato de exibição de proprietário, um proprietário da área de transferência pode evitar a sobrecarga de renderizar dados em um formato adicional, assumindo o controle direto sobre a pintura da janela do Visualizador da área de transferência. A janela Visualizador da área de transferência envia mensagens para o proprietário da área de transferência sempre que uma parte da janela deve ser redesenhada ou quando a janela é rolada ou redimensionada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formatos de área de transferência padrão](standard-clipboard-formats.md)
</dt> </dl>

 

 