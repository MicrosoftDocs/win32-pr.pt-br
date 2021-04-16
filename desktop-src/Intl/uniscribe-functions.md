---
description: Esta seção descreve as funções de tipografia e de processamento de script complexo.
ms.assetid: 876e36f5-a91c-490b-87bd-b7cb4993f8c4
title: Funções do Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f623c8da04f985f88d091f8e9e2b4cb724c0801
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750629"
---
# <a name="uniscribe-functions"></a>Funções do Uniscribe

Esta seção descreve as funções de tipografia e de processamento de script complexo.



| Função                                                               | Descrição                                                                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution)   | Aplica as configurações de substituição de dígito especificadas ao controle de script especificado e às estruturas de estado do script.                                                                    |
| [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)             | Usa uma matriz de larguras avançadas para uma execução e gera uma matriz de larguras de glifos ajustadas.                                                                               |
| [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)                                     | Recupera informações para determinar as quebras de linha.                                                                                                                                |
| [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)                   | Recupera a altura da fonte atualmente armazenada em cache.                                                                                                                                |
| [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)                                     | Gera o deslocamento x da extremidade esquerda ou borda esquerda de uma execução para a borda à esquerda ou à direita de um cluster de caracteres lógicos.                                          |
| [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache)                             | Libera um cache de script.                                                                                                                                                             |
| [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)                                 | Recupera os índices de glifos dos caracteres Unicode em uma cadeia de caracteres de acordo com a tabela de CMap TrueType ou a tabela de mapa de texto padrão implementada para fontes de estilo antigo.         |
| [**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)   | Recupera uma lista de glifos alternativos para um caractere especificado que pode ser acessado por meio de um recurso de OpenType especificado.                                                         |
| [**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)           | Recupera uma lista de recursos tipográficos para o sistema de escrita definido para o processamento de OpenType.                                                                                  |
| [**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)         | Recupera uma lista de marcas de idioma que estão disponíveis para o item especificado e têm suporte de uma marca de script especificada para o processamento de OpenType.                                  |
| [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)             | Recupera informações do cache de fontes nos glifos especiais usados por uma fonte.                                                                                                   |
| [**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)             | Recupera uma lista de scripts disponíveis na fonte para processamento de OpenType.                                                                                                        |
| [**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth)               | Recupera a largura ABC de um determinado glifo.                                                                                                                                         |
| [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)               | Converte as larguras de avanço de glifo para uma fonte específica em larguras lógicas.                                                                                                        |
| [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties)                     | Recupera informações sobre os scripts atuais.                                                                                                                                  |
| [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex)                             | Determina se uma cadeia de caracteres Unicode requer processamento de script complexo.                                                                                                           |
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)                                 | Quebra uma cadeia de caracteres Unicode em itens formais individualmente.                                                                                                                        |
| [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)                 | Quebra uma cadeia de caracteres Unicode em itens formais individualmente e fornece uma matriz de marcas de recurso para cada item moldado para processamento de OpenType.                                  |
| [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)                                 | Cria uma tabela de larguras avançadas para permitir a justificação de texto quando passada para a função [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) .                                                   |
| [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout)                                   | Converte uma matriz de níveis de inserção de execução em um mapa de posição de Visual para lógico e/ou posição lógica para Visual.                                                               |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)                                     | Gera uma largura de avanço de glifo e informações de deslocamento bidimensionais da saída de [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).                                                       |
| [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)                     | Gera glifos e atributos visuais para um Unicode executado com informações de OpenType da saída de [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).                         |
| [**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)         | Posiciona um único glifo com um único ajuste usando um recurso especificado fornecido na fonte para processamento de OpenType.                                                         |
| [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) | Lê as configurações de substituição de dígitos e dígito nativo do NLS (suporte ao idioma nacional) e os registra em uma estrutura de [**\_ DIGITSUBSTITUTE de script**](/windows/win32/api/usp10/ns-usp10-script_digitsubstitute) . |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                     | Gera glifos e atributos visuais para uma execução Unicode.                                                                                                                         |
| [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                     | Gera glifos e atributos visuais para um Unicode executado com informações de OpenType.                                                                                               |
| [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)                     | Analisa uma cadeia de caracteres de texto sem formatação.                                                                                                                                                     |
| [**ScriptStringCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox)                         | Recupera a coordenada x para a borda à esquerda ou à direita de uma posição de caractere.                                                                                              |
| [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)                           | Libera uma estrutura [**de \_ \_ análise de cadeia de caracteres de script**](script-string-analysis.md) .                                                                                                     |
| [**ScriptStringGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths)   | Converte larguras visuais em larguras lógicas.                                                                                                                                       |
| [**ScriptStringGetOrder**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder)                   | Cria uma matriz que mapeia uma posição de caractere original para uma posição de glifo.                                                                                                    |
| [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)                             | Exibe uma cadeia de caracteres gerada por uma chamada anterior para [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) e, opcionalmente, adiciona o realce.                                               |
| [**PcOutChars ScriptString \_**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars)            | Retorna um ponteiro para o comprimento de uma cadeia de caracteres após o recorte.                                                                                                                       |
| [**PLogAttr ScriptString \_**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr)                | Retorna um ponteiro para um buffer de atributos lógicos para uma cadeia de caracteres analisada.                                                                                                          |
| [**PSize ScriptString \_**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize)                      | Retorna um ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) para uma cadeia de caracteres analisada.                                                                                                     |
| [**ScriptStringValidate**](/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate)                   | Verifica se há sequências inválidas na estrutura de [**\_ \_ análise de cadeia de script**](script-string-analysis.md) .                                                                              |
| [**ScriptStringXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp)                         | Converte uma coordenada x em uma posição de caractere.                                                                                                                                 |
| [**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)     | Habilita a substituição de um único glifo com uma forma alternativa do mesmo glifo para o processamento de OpenType.                                                                         |
| [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                 | Exibe o texto para a forma de script especificado e coloca as informações.                                                                                                               |
| [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)                                     | Gera a borda à esquerda ou à direita de um cluster de caracteres lógicos a partir do deslocamento x de uma execução.                                                                                 |



 

 

 
