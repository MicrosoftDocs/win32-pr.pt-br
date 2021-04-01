---
description: Usando fallback de fonte
ms.assetid: 952f33b6-ca52-40a2-b914-52c1c62ae0e0
title: Usando fallback de fonte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9afb073a01cc1c5b90d4a4861a973846d3ae9ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663483"
---
# <a name="using-font-fallback"></a>Usando fallback de fonte

> [!Note]  
> Neste tópico, todos os comentários sobre [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) aplicam-se igualmente a [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).

 

Seu aplicativo deve usar o fallback de fonte durante a exibição de texto se alguns caracteres em uma cadeia de caracteres não forem suportados na fonte ou se o aplicativo usar um [script complexo](uniscribe-glossary.md) sem suporte da fonte. O requisito para o fallback de fonte é detectado durante o processo de layout para texto, quando o aplicativo chama a função [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) . Para obter informações sobre a exibição de texto, consulte [exibindo texto com o Uniscribe](displaying-text-with-uniscribe.md).

## <a name="determine-the-need-for-font-fallback-for-unsupported-characters"></a>Determinar a necessidade de fallback de fonte para caracteres sem suporte

Se alguns dos caracteres em uma cadeia de caracteres não forem suportados em uma fonte solicitada, uma chamada de aplicativo para [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) terá sucesso. No entanto, o aplicativo deve verificar o buffer de saída de glifo para a presença de glifos ausentes. O índice de glifo do glifo ausente pode ser determinado para uma fonte específica chamando [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Se um glifo específico não estiver disponível, o aplicativo deverá retornar a uma fonte diferente para um glifo ou renderizar um símbolo gráfico que indica que nenhum glifo está disponível.

## <a name="determine-the-need-for-font-fallback-for-unsupported-complex-scripts"></a>Determinar a necessidade de fallback de fonte para scripts complexos sem suporte

A fonte que um aplicativo prefere para exibição pode não dar suporte a um script complexo exigido pelo texto. Nesse caso, a chamada de aplicativo para [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) falha com o código de erro E o \_ script que não está \_ \_ na \_ fonte.

## <a name="assign-a-fallback-font"></a>Atribuir uma fonte de fallback

Depois de determinar que o fallback de fonte é necessário, o aplicativo deve atribuir uma fonte de fallback. O aplicativo pode tentar as seguintes técnicas:

-   Chame [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para cada fonte em uma lista de fontes até que uma chamada tenha um retorno aceitável.
-   Chame [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) com cada fonte em uma lista até que seja possível determinar que nenhuma fonte terá sucesso. Se o código de erro for sempre E o \_ script \_ não \_ \_ estiver na fonte, não haverá suporte para um script complexo nas fontes. Processe um símbolo gráfico que indica que nenhum glifo está disponível ou especifique o script novamente como indefinido (sem processamento de script) e inicie novamente. Para definir o script como indefinido, defina o membro **eScript** da estrutura [**de \_ análise de script**](/windows/win32/api/usp10/ns-usp10-script_analysis) como script \_ undefined.
-   Chame [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) com cada fonte em uma lista até que seja possível determinar que nenhuma fonte terá sucesso. Se o código de erro indicar que alguns dos caracteres estão sendo mapeados para glifos ausentes, divida a cadeia de caracteres em intervalos menores. Diferentes fontes podem ser atribuídas a subintervalos para que mais caracteres possam ser renderizados.

## <a name="generate-glyph-information"></a>Gerar informações de glifo

Depois que o aplicativo tiver atribuído uma fonte com sucesso em chamadas para [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), ele poderá fazer chamadas para [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) para gerar a largura de avanço de glifo e informações de deslocamento bidimensionais da saída de **ScriptShape**. A fonte deve ter sucesso nessas chamadas. Uma falha de fonte em uma chamada para **ScriptPlace** após o êxito em uma chamada **ScriptShape** indica uma fonte quebrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



