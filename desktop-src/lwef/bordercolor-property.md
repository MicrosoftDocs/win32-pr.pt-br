---
title: Propriedade BorderColor
description: Propriedade BorderColor
ms.assetid: 7592db02-c157-45f4-bbcf-e6d5bd99e8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981d3ac280669f64219961b74d05c6ba73f1008
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453587"
---
# <a name="bordercolor-property"></a><span data-ttu-id="c99d1-103">Propriedade BorderColor</span><span class="sxs-lookup"><span data-stu-id="c99d1-103">BorderColor Property</span></span>

<span data-ttu-id="c99d1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c99d1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c99d1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="c99d1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c99d1-106">Retorna a cor de borda atualmente exibida para a janela de balão do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="c99d1-106">Returns the border color currently displayed for the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="c99d1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="c99d1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c99d1-108">\* Agente ***. Caracteres ("*** characterid \***").** Balloon. BorderColor</span><span class="sxs-lookup"><span data-stu-id="c99d1-108">*agent ***.Characters ("*** CharacterID\*\*\*").*\* Balloon.BorderColor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c99d1-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c99d1-109">Remarks</span></span>

<span data-ttu-id="c99d1-110">O intervalo válido para uma cor RGB normal é de 0 a 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="c99d1-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="c99d1-111">O byte alto de um número neste intervalo é igual a 0; os 3 bytes inferiores, do menos ao byte mais significativo, determinam a quantidade de vermelho, verde e azul, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c99d1-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="c99d1-112">Cada um dos componentes vermelho, verde e azul é representado por um número entre 0 e 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="c99d1-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




