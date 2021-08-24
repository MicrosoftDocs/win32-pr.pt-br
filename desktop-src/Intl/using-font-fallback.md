---
description: Usando fallback de fonte
ms.assetid: 952f33b6-ca52-40a2-b914-52c1c62ae0e0
title: Usando fallback de fonte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9a4e9b329e2c3257ae9fad02f1fb4774a63dc1d4b4e804c0dca8e690cbf4d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787866"
---
# <a name="using-font-fallback"></a>Usando fallback de fonte

> [!Note]  
> Neste tópico, todos os comentários sobre [**ScriptShape se**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) aplicam igualmente a [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).

 

Seu aplicativo deve usar fallback de fonte durante a exibição de texto se não há suporte para alguns caracteres em uma cadeia de caracteres na fonte ou se o aplicativo usa um [script](uniscribe-glossary.md) complexo sem suporte da fonte. O requisito de fallback de fonte é detectado durante o processo de layout para texto, quando o aplicativo chama a [**função ScriptShape.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) Para obter informações sobre exibição de texto, [consulte Exibindo texto com Uniscribe](displaying-text-with-uniscribe.md).

## <a name="determine-the-need-for-font-fallback-for-unsupported-characters"></a>Determinar a necessidade de fallback de fonte para caracteres sem suporte

Se alguns dos caracteres em uma cadeia de caracteres não são suportados em uma fonte solicitada, uma chamada de aplicativo para [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) é bem-sucedida. No entanto, o aplicativo deve verificar o buffer de saída de glifo quanto à presença de glifos ausentes. O índice de glifo do glifo ausente pode ser determinado para uma fonte específica chamando [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Se um glifo específico não estiver disponível, o aplicativo deverá voltar para uma fonte diferente para um glifo ou renderizar um símbolo gráfico que indica que nenhum glifo está disponível.

## <a name="determine-the-need-for-font-fallback-for-unsupported-complex-scripts"></a>Determinar a necessidade de fallback de fonte para scripts complexos sem suporte

A fonte que um aplicativo prefere para exibição pode não dar suporte a um script complexo exigido pelo texto. Nesse caso, a chamada do aplicativo para [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) falha com o código de erro E \_ SCRIPT NOT IN \_ \_ \_ FONT.

## <a name="assign-a-fallback-font"></a>Atribuir uma fonte de fallback

Depois de determinar que o fallback de fonte é necessário, o aplicativo deve atribuir uma fonte de fallback. O aplicativo pode experimentar as seguintes técnicas:

-   Chame [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para cada fonte em uma lista de fontes até que uma chamada tenha um retorno aceitável.
-   Chame [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) com cada fonte em uma lista até que possa ser determinado que nenhuma fonte terá êxito. Se o código de erro for sempre E SCRIPT NOT IN FONT, não há suporte para \_ um script complexo nas \_ \_ \_ fontes. Renderizar um símbolo gráfico que indica que nenhum glifo está disponível ou especificar novamente o script como indefinido (sem processamento de script) e iniciar novamente. Para definir o script como indefinido, defina o membro **eScript** da estrutura [**SCRIPT \_ ANALYSIS**](/windows/win32/api/usp10/ns-usp10-script_analysis) como SCRIPT \_ UNDEFINED.
-   Chame [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) com cada fonte em uma lista até que possa ser determinado que nenhuma fonte terá êxito. Se o código de erro indicar que alguns dos caracteres estão mapeando para glifos ausentes, quebre a cadeia de caracteres em intervalos menores. Fontes diferentes podem ser atribuídas a subranges para que mais caracteres possam ser renderizados.

## <a name="generate-glyph-information"></a>Gerar informações de glifo

Depois que o aplicativo atribui uma fonte que é bem-sucedida em chamadas para [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), ele pode fazer chamadas para [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) para gerar largura de avanço de glifo e informações de deslocamento bidimensional da saída de **ScriptShape**. A fonte deve ter êxito nessas chamadas. Uma falha de fonte em uma chamada para **ScriptPlace após** o sucesso em **uma chamada ScriptShape** indica uma fonte interrompida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



