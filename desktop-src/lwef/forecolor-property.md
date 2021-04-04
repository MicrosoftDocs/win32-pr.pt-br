---
title: Propriedade ForeColor
description: Propriedade ForeColor
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef05c9f51e040326c75f142e4649a8dbd0cfdbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822376"
---
# <a name="forecolor-property"></a><span data-ttu-id="42590-103">Propriedade ForeColor</span><span class="sxs-lookup"><span data-stu-id="42590-103">ForeColor Property</span></span>

<span data-ttu-id="42590-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="42590-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="42590-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="42590-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="42590-106">Retorna a cor de primeiro plano exibida atualmente na janela de balão do texto para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="42590-106">Returns the foreground color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="42590-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="42590-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="42590-108">*agente do ***. Caracteres ("*** characterid \* \* *"). Balloon. ForeColor**</span><span class="sxs-lookup"><span data-stu-id="42590-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.ForeColor*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42590-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="42590-109">Remarks</span></span>

<span data-ttu-id="42590-110">A propriedade **ForeColor** retorna um valor que especifica a cor do texto na palavra balão.</span><span class="sxs-lookup"><span data-stu-id="42590-110">The **ForeColor** property returns a value that specifies the color of text in the word balloon.</span></span> <span data-ttu-id="42590-111">O intervalo válido para uma cor RGB normal é de 0 a 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="42590-111">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="42590-112">O byte alto de um número neste intervalo é igual a 0; os 3 bytes inferiores, do menos ao byte mais significativo, determinam a quantidade de vermelho, verde e azul, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="42590-112">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="42590-113">Cada um dos componentes vermelho, verde e azul é representado por um número entre 0 e 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="42590-113">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




