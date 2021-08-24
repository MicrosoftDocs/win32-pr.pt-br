---
description: Esta seção descreve as funções para tipografia e para processamento de script complexo.
ms.assetid: 876e36f5-a91c-490b-87bd-b7cb4993f8c4
title: Funções uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547bdd2179e734120fe07c2ae774c8a066d9fd5d9db2be1262e67b505cbb04ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582186"
---
# <a name="uniscribe-functions"></a>Funções uniscribe

Esta seção descreve as funções para tipografia e para processamento de script complexo.



| Função                                                               | Descrição                                                                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution)   | Aplica as configurações de substituição de dígito especificadas às estruturas de estado de script e controle de script especificadas.                                                                    |
| [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)             | Leva uma matriz de larguras de avanço para uma executar e gera uma matriz de larguras de glifos de avanço ajustadas.                                                                               |
| [**Scriptbreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)                                     | Recupera informações para determinar quebras de linha.                                                                                                                                |
| [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)                   | Recupera a altura da fonte armazenada em cache no momento.                                                                                                                                |
| [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)                                     | Gera o deslocamento x da extremidade esquerda ou da borda à esquerda de uma corrida para a borda à esquerda ou à direita de um cluster de caracteres lógicos.                                          |
| [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache)                             | Libera um cache de script.                                                                                                                                                             |
| [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)                                 | Recupera os índices de glifo dos caracteres Unicode em uma cadeia de caracteres de acordo com a tabela cmap TrueType ou a tabela cmap padrão implementada para fontes de estilo antigo.         |
| [**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)   | Recupera uma lista de glifos alternativos para um caractere especificado que pode ser acessado por meio de um recurso OpenType especificado.                                                         |
| [**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)           | Recupera uma lista de recursos tipográficos para o sistema de escrita definido para processamento OpenType.                                                                                  |
| [**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)         | Recupera uma lista de marcas de idioma que estão disponíveis para o item especificado e têm suporte por uma marca de script especificada para processamento OpenType.                                  |
| [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)             | Recupera informações do cache de fonte nos glifos especiais usados por uma fonte.                                                                                                   |
| [**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)             | Recupera uma lista de scripts disponíveis na fonte para processamento OpenType.                                                                                                        |
| [**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth)               | Recupera a largura ABC de um determinado glifo.                                                                                                                                         |
| [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)               | Converte as larguras de avanço de glifo para uma fonte específica em larguras lógicas.                                                                                                        |
| [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties)                     | Recupera informações sobre os scripts atuais.                                                                                                                                  |
| [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex)                             | Determina se uma cadeia de caracteres Unicode requer processamento de script complexo.                                                                                                           |
| [**Scriptitemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)                                 | Divide uma cadeia de caracteres Unicode em itens formatados individualmente.                                                                                                                        |
| [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)                 | Divide uma cadeia de caracteres Unicode em itens formatados individualmente e fornece uma matriz de marcas de recurso para cada item moldável para processamento OpenType.                                  |
| [**Scriptjustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)                                 | Cria uma tabela de larguras avançadas para permitir a justificativa de texto quando passada para a [**função ScriptTextOut.**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                                   |
| [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout)                                   | Converte uma matriz de níveis de incorporação de executar em um mapa de posição visual para lógica e/ou posição lógica para visual.                                                               |
| [**Scriptplace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)                                     | Gera largura de avanço de glifo e informações de deslocamento bidimensional da saída de [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).                                                       |
| [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)                     | Gera glifos e atributos visuais para uma executar Unicode com informações de OpenType da saída de [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).                         |
| [**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)         | Posiciona um único glifo com um único ajuste usando um recurso especificado fornecido na fonte para processamento openType.                                                         |
| [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) | Lê as configurações de substituição de dígitos e dígitos nativos do NLS (National Language Support) e as registra em uma [**estrutura SCRIPT \_ DIGITSUBSTITUTE.**](/windows/win32/api/usp10/ns-usp10-script_digitsubstitute) |
| [**Scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                     | Gera glifos e atributos visuais para uma executar Unicode.                                                                                                                         |
| [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                     | Gera glifos e atributos visuais para uma executar Unicode com informações de OpenType.                                                                                               |
| [**Scriptstringanalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)                     | Analisa uma cadeia de caracteres de texto sem-texto.                                                                                                                                                     |
| [**ScriptStringCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox)                         | Recupera a coordenada x para a borda à esquerda ou à direita de uma posição de caractere.                                                                                              |
| [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)                           | Libera uma estrutura [**SCRIPT \_ STRING \_ ANALYSIS.**](script-string-analysis.md)                                                                                                     |
| [**ScriptStringGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths)   | Converte larguras visuais em larguras lógicas.                                                                                                                                       |
| [**ScriptStringGetOrder**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder)                   | Cria uma matriz que mapeia uma posição de caractere original para uma posição de glifo.                                                                                                    |
| [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)                             | Exibe uma cadeia de caracteres gerada por uma chamada anterior para [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) e, opcionalmente, adiciona realçamento.                                               |
| [**ScriptString \_ pcOutChars**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars)            | Retorna um ponteiro para o comprimento de uma cadeia de caracteres após o recorte.                                                                                                                       |
| [**ScriptString \_ pLogAttr**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr)                | Retorna um ponteiro para um buffer de atributos lógicos para uma cadeia de caracteres analisada.                                                                                                          |
| [**ScriptString \_ pSize**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize)                      | Retorna um ponteiro para uma estrutura [**SIZE**](/previous-versions//dd145106(v=vs.85)) para uma cadeia de caracteres analisada.                                                                                                     |
| [**ScriptStringValidate**](/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate)                   | Verifica uma estrutura [**SCRIPT \_ STRING \_ ANALYSIS**](script-string-analysis.md) em busca de sequências inválidas.                                                                              |
| [**ScriptStringXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp)                         | Converte uma coordenada x em uma posição de caractere.                                                                                                                                 |
| [**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)     | Habilita a substituição de um único glifo por uma forma alternativa do mesmo glifo para processamento OpenType.                                                                         |
| [**Scripttextout**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                 | Exibe o texto para as informações de colocação e forma de script especificadas.                                                                                                               |
| [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)                                     | Gera a borda à esquerda ou à direita de um cluster de caracteres lógicos do deslocamento x de uma sequência.                                                                                 |



 

 

 
