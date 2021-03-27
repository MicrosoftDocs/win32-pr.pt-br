---
description: Você pode usar a função GetGlyphOutline para recuperar o contorno de um glifo de uma fonte TrueType.
ms.assetid: 9b255dfa-3c1d-4707-927d-a2d5f4117f6a
title: Recuperando contornos de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 638193632d4992dfb53f29a3dfe66a858b3e1fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967591"
---
# <a name="retrieving-character-outlines"></a>Recuperando contornos de caracteres

Você pode usar a função [GetGlyphOutline](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea) para recuperar o contorno de um glifo de uma fonte TrueType. O contorno de glifo retornado pela função [**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) é para um glifo ajustado à grade. (Um glifo ajustado para grade foi modificado de forma que sua imagem de bitmap esteja de acordo com o máximo possível para o design original do glifo.) Se seu aplicativo requer um contorno de glifo não modificado, solicite o contorno de glifo para um caractere em uma fonte cujo tamanho seja igual às unidades em em. (Para criar uma fonte com esse tamanho, defina o membro **lfHeight** da estrutura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) como o negativo do valor do membro **ntmSizeEM** da estrutura [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .)

[**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) retorna a estrutura de tópicos como um bitmap ou uma série de polilinhas e linhas. Quando um aplicativo recupera um contorno de glifo como uma série de polilinhas e linhas, as informações são retornadas em uma estrutura [TTPOLYGONHEADER](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) seguida por tantas estruturas [TTPOLYCURVE](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) quantas forem necessárias para descrever o glifo. Todos os pontos são retornados como estruturas [POINTFX](/windows/win32/api/wingdi/ns-wingdi-pointfx) e representam posições absolutas, não movimentações relativas. O ponto de partida especificado pelo membro **pfxStart** da estrutura [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) é o ponto em que o contorno de uma delimitação começa. As estruturas [**TTPOLYCURVE**](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) que seguem podem ser registros de polilinha ou registros de spline.

Para renderizar um contorno de caractere TrueType, você deve usar os registros Polyline e spline. O sistema pode renderizar as polilinhas e as próprias linhas facilmente. Cada registro de polilinha e spline contém o máximo de pontos sequenciais possível, para minimizar o número de registros retornados.

O ponto de partida especificado na estrutura [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) está sempre no contorno do glifo. O ponto especificado serve como os pontos inicial e final da delimitação.

Esta seção fornece informações sobre os tópicos a seguir.

-   [Registros de polilinha](polyline-records.md)
-   [Registros de spline](spline-records.md)

 

 
