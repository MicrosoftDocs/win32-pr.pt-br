---
title: Propriedade BackColor (recursos de ambiente herdado do Windows)
description: Propriedade BackColor
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644188"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a><span data-ttu-id="efad9-103">Propriedade BackColor (recursos de ambiente herdado do Windows)</span><span class="sxs-lookup"><span data-stu-id="efad9-103">BackColor Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="efad9-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="efad9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="efad9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="efad9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="efad9-106">Retorna a cor do plano de fundo atualmente exibida na janela de balão do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="efad9-106">Returns the background color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="efad9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="efad9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="efad9-108">\*agente \***. Caracteres ("**_characterid_*_"). Balloon. BackColor_*</span><span class="sxs-lookup"><span data-stu-id="efad9-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.BackColor_\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efad9-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="efad9-109">Remarks</span></span>

<span data-ttu-id="efad9-110">O intervalo válido para uma cor RGB normal é de 0 a 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="efad9-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="efad9-111">O byte alto de um número neste intervalo é igual a 0; os 3 bytes inferiores, do menos ao byte mais significativo, determinam a quantidade de vermelho, verde e azul, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="efad9-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="efad9-112">Cada um dos componentes vermelho, verde e azul é representado por um número entre 0 e 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="efad9-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




