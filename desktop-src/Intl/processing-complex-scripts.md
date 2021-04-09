---
description: Para fornecer uma justificativa de texto, um aplicativo pode usar um dos dois métodos.
ms.assetid: 1190baed-5959-4f7a-8946-ac3b3da85821
title: Processando scripts complexos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bea5b75e87afc4177b03c03f4263ba2592a0e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010451"
---
# <a name="processing-complex-scripts"></a>Processando scripts complexos

Para fornecer uma justificativa de texto, um aplicativo pode usar um dos dois métodos. Para uma implementação simples de justificativa multilíngue, o aplicativo deve chamar [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify). Ele gera a matriz do Delta DX considerando kashida, depois espaçamento entre palavras e espaçamento entre caracteres. Para uma justificativa mais sofisticada, o aplicativo pode gerar uma matriz de DX Delta atualizada usando seu próprio conhecimento de linguagem e as informações recuperadas pelo [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) na matriz [**\_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr) .

O espaço de justificativa ou kashida deve ser inserido onde identificado pelo membro **uJustification** do [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr). Ao executar a justificação entre caracteres, o aplicativo deve inserir espaço extra somente após os glifos marcados com o \_ caractere de justificação do script \_ .

O aplicativo faz o posicionamento do cursor e o teste de clique usando [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) e [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox). Para obter mais informações, consulte [Gerenciamento de posicionamento de cursor e teste de clique](managing-caret-placement-and-hit-testing.md).

Para obter larguras de maneira independente de fonte, o aplicativo chama [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths). Ao passar as larguras lógicas para [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth), um bloco de texto pode ser exibido novamente nos mesmos limites com perda aceitável de qualidade, mesmo quando a fonte original não está disponível. Ele gera uma matriz de larguras de glifo ([larguras avançadas](uniscribe-glossary.md)) adequada para passar para [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout). A gravação e a reaplicação de informações de largura avançadas de maneira independente de fonte podem ser úteis em situações como a Metacriação em um formato definido pelo aplicativo.

> [!Note]  
> Os metaarquivos não oferecem suporte a índices de glifos. Para gravar em um metarquivo avançado, o aplicativo deve usar [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) e gravar os caracteres lógicos diretamente. Usando esse mecanismo, a geração de glifos e o posicionamento não ocorrem até que o texto seja reproduzido.

 

Para recuperar os glifos específicos que são usados para o padrão, espaços em branco, kashida e assim por diante, para a fonte atual, o aplicativo deve chamar [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Para determinar quais caracteres em uma execução têm suporte na fonte selecionada, o aplicativo chama [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap). Os caracteres que não estão disponíveis têm o glifo padrão no buffer de glifo. Observe que esse método falhará se uma fonte renderizar um caractere usando uma combinação de glifos em vez de um único glifo. Por exemplo, 00C9; Letra latina maiúscula e com acento agudo podem ser renderizadas usando um glifo e um glifo maiúsculo. Para determinar o suporte de fonte para uma cadeia de caracteres que contém esses tipos de pontos de código, o aplicativo pode chamar [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape). Para obter mais informações, consulte [usando mecanismos de shaping](using-shaping-engines.md).

A função [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight) retorna a altura da fonte do cache de fontes. O [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) fornece informações sobre o processamento especial necessário para todos os scripts, indexados por script. Por exemplo, ele inclui o idioma principal associado ao script, dados indicando se o script é numérico e dados indicando se o script é complexo.

[**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth) retorna a [largura ABC](uniscribe-glossary.md) de um determinado glifo, que pode ser útil para desenhar gráficos de glifos. No entanto, ele não deve ser usado para formatação de texto de script complexo normal.

## <a name="related-topics"></a>Tópicos relacionados

[Usando o Uniscribe](using-uniscribe.md)


 

 
