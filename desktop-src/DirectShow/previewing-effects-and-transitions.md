---
description: Visualização de efeitos e transições
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Visualização de efeitos e transições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baa5f35511ca9b01990e1c3e0562a3a564204a52026c08e2e2827c154b166b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748296"
---
# <a name="previewing-effects-and-transitions"></a>Visualização de efeitos e transições

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Alguns efeitos e transições levam um tempo relativamente longo para serem renderizados. Durante a visualização, isso pode fazer com que o vídeo se torne instável ou fora de sincronia com o áudio. Você pode aumentar a velocidade de visualização desabilitando efeitos ou transições:

-   Para desabilitar todos os efeitos, chame [**IAMTimeline:: EnableEffects**](iamtimeline-enableeffects.md).
-   Para desabilitar todas as transições, chame [**IAMTimeline:: EnableTransitions**](iamtimeline-enabletransitions.md).
-   Para desabilitar uma transição específica, chame [**IAMTimelineTrans:: SetCutsOnly**](iamtimelinetrans-setcutsonly.md).

Quando os efeitos são desabilitados, eles não são renderizados durante a visualização. Quando uma transição é desabilitada, ela é renderizada como um corte de salto. O transição entre faixas ainda ocorre, mas o efeito visual não é renderizado.

Se um efeito ou uma transição não puder ser renderizado, o mecanismo de renderização substituirá um efeito ou uma transição padrão. Chame o método [**IAMTimeline:: SetDefaultEffect**](iamtimeline-setdefaulteffect.md) para definir o efeito padrão e o método [**IAMTimeline:: SetDefaultTransition**](iamtimeline-setdefaulttransition.md) para definir a transição padrão. Se você não especificar um padrão, ou se aquele que você especificar também causar um erro, o DES usará seu próprio padrão.

> [!Note]  
> Você também pode melhorar a qualidade da visualização aumentando a quantidade de buffers de quadros. Consulte [**IAMTimelineGroup:: SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com efeitos e transições](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



