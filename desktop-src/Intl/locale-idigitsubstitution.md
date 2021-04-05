---
description: IDIGITSUBSTITUTION de localidade \_
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089855"
---
# <a name="locale_idigitsubstitution"></a><span data-ttu-id="7df08-103">IDIGITSUBSTITUTION de localidade \_</span><span class="sxs-lookup"><span data-stu-id="7df08-103">LOCALE\_IDIGITSUBSTITUTION</span></span>

<span data-ttu-id="7df08-104">**Windows 2000:** A forma de dígitos.</span><span class="sxs-lookup"><span data-stu-id="7df08-104">**Windows 2000:** The shape of digits.</span></span> <span data-ttu-id="7df08-105">Por exemplo, os dígitos arábico, tailandês e Índico têm formas clássicas diferentes dos dígitos europeus.</span><span class="sxs-lookup"><span data-stu-id="7df08-105">For example, Arabic, Thai, and Indic digits have classical shapes different from European digits.</span></span> <span data-ttu-id="7df08-106">Para localidades com [ \_ SNATIVEDIGITS de localidade](locale-snative-constants.md) especificadas como valores diferentes de ASCII 0-9, esse valor especifica se a preferência deve ser dada a esses outros dígitos para fins de exibição.</span><span class="sxs-lookup"><span data-stu-id="7df08-106">For locales with [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) specified as values other than ASCII 0-9, this value specifies whether preference should be given to those other digits for display purposes.</span></span> <span data-ttu-id="7df08-107">Por exemplo, se um valor de 2 for escolhido, os dígitos especificados pela localidade \_ SNATIVEDIGITS sempre serão usados.</span><span class="sxs-lookup"><span data-stu-id="7df08-107">For example, if a value of 2 is chosen, the digits specified by LOCALE\_SNATIVEDIGITS are always used.</span></span> <span data-ttu-id="7df08-108">Se um 1 for escolhido, os dígitos ASCII 0-9 serão sempre usados.</span><span class="sxs-lookup"><span data-stu-id="7df08-108">If a 1 is chosen, the ASCII 0-9 digits are always used.</span></span> <span data-ttu-id="7df08-109">Se um 0 for escolhido, o ASCII será usado em algumas circunstâncias e os dígitos especificados por \_ SNATIVEDIGITS de localidade serão usados em outros, dependendo do contexto.</span><span class="sxs-lookup"><span data-stu-id="7df08-109">If a 0 is chosen, ASCII is used in some circumstances and the digits specified by LOCALE\_SNATIVEDIGITS are used in others, depending on the context.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7df08-110">Valor</span><span class="sxs-lookup"><span data-stu-id="7df08-110">Value</span></span></th>
<th><span data-ttu-id="7df08-111">Significado</span><span class="sxs-lookup"><span data-stu-id="7df08-111">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7df08-112">0</span><span class="sxs-lookup"><span data-stu-id="7df08-112">0</span></span></td>
<td><span data-ttu-id="7df08-113">Substituição baseada em contexto.</span><span class="sxs-lookup"><span data-stu-id="7df08-113">Context-based substitution.</span></span> <span data-ttu-id="7df08-114">Os dígitos são exibidos com base no texto anterior na mesma saída.</span><span class="sxs-lookup"><span data-stu-id="7df08-114">Digits are displayed based on the previous text in the same output.</span></span> <span data-ttu-id="7df08-115">Os dígitos europeus seguem scripts latinos, Arabic-Indic dígitos seguem texto em árabe e outros dígitos nacionais seguem texto escrito em vários outros scripts.</span><span class="sxs-lookup"><span data-stu-id="7df08-115">European digits follow Latin scripts, Arabic-Indic digits follow Arabic text, and other national digits follow text written in various other scripts.</span></span> <span data-ttu-id="7df08-116">Quando não há texto anterior, a localidade e a ordem de leitura exibida determinam a substituição de dígitos, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7df08-116">When there is no preceding text, the locale and the displayed reading order determine digit substitution, as shown in the following table.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7df08-117">Locale</span><span class="sxs-lookup"><span data-stu-id="7df08-117">Locale</span></span></th>
<th><span data-ttu-id="7df08-118">Sentido de leitura</span><span class="sxs-lookup"><span data-stu-id="7df08-118">Reading order</span></span></th>
<th><span data-ttu-id="7df08-119">Dígitos usados</span><span class="sxs-lookup"><span data-stu-id="7df08-119">Digits used</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7df08-120">Árabe</span><span class="sxs-lookup"><span data-stu-id="7df08-120">Arabic</span></span></td>
<td><span data-ttu-id="7df08-121">Da direita para a esquerda</span><span class="sxs-lookup"><span data-stu-id="7df08-121">Right-to-left</span></span></td>
<td><span data-ttu-id="7df08-122">Indo-arábico</span><span class="sxs-lookup"><span data-stu-id="7df08-122">Arabic-Indic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7df08-123">Tailandês</span><span class="sxs-lookup"><span data-stu-id="7df08-123">Thai</span></span></td>
<td><span data-ttu-id="7df08-124">Da esquerda para a direita</span><span class="sxs-lookup"><span data-stu-id="7df08-124">Left-to-right</span></span></td>
<td><span data-ttu-id="7df08-125">Dígitos tailandeses</span><span class="sxs-lookup"><span data-stu-id="7df08-125">Thai digits</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7df08-126">Todos os outros</span><span class="sxs-lookup"><span data-stu-id="7df08-126">All others</span></span></td>
<td><span data-ttu-id="7df08-127">Qualquer</span><span class="sxs-lookup"><span data-stu-id="7df08-127">Any</span></span></td>
<td><span data-ttu-id="7df08-128">Nenhuma substituição usada</span><span class="sxs-lookup"><span data-stu-id="7df08-128">No substitution used</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7df08-129">1</span><span class="sxs-lookup"><span data-stu-id="7df08-129">1</span></span></td>
<td><span data-ttu-id="7df08-130">Nenhuma substituição foi usada.</span><span class="sxs-lookup"><span data-stu-id="7df08-130">No substitution used.</span></span> <span data-ttu-id="7df08-131">Compatibilidade total com Unicode.</span><span class="sxs-lookup"><span data-stu-id="7df08-131">Full Unicode compatibility.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7df08-132">2</span><span class="sxs-lookup"><span data-stu-id="7df08-132">2</span></span></td>
<td><span data-ttu-id="7df08-133">Substituição de dígito nativo.</span><span class="sxs-lookup"><span data-stu-id="7df08-133">Native digit substitution.</span></span> <span data-ttu-id="7df08-134">As formas nacionais são exibidas de acordo com LOCALE_SNATIVEDIGITS.</span><span class="sxs-lookup"><span data-stu-id="7df08-134">National shapes are displayed according to LOCALE_SNATIVEDIGITS.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



