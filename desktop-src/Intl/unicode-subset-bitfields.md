---
description: Os subconjuntos Unicode bitfields (USBs) são usados nas estruturas FONTSIGNATURE e LOCALESIGNATURE.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Subconjunto Unicode bitfields
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fced251b1bf8e04dd4c0d7d7cb0dca15c8bdfa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752668"
---
# <a name="unicode-subset-bitfields"></a><span data-ttu-id="38e18-103">Subconjunto Unicode bitfields</span><span class="sxs-lookup"><span data-stu-id="38e18-103">Unicode Subset Bitfields</span></span>

<span data-ttu-id="38e18-104">Os subconjuntos Unicode bitfields (USBs) são usados nas estruturas [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) e [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .</span><span class="sxs-lookup"><span data-stu-id="38e18-104">The Unicode subset bitfields (USBs) are used in the [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) and [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) structures.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="38e18-105">bit</span><span class="sxs-lookup"><span data-stu-id="38e18-105">Bit</span></span></th>
<th><span data-ttu-id="38e18-106">Subintervalo Unicode</span><span class="sxs-lookup"><span data-stu-id="38e18-106">Unicode subrange</span></span></th>
<th><span data-ttu-id="38e18-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="38e18-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="38e18-108">0</span><span class="sxs-lookup"><span data-stu-id="38e18-108">0</span></span></td>
<td><span data-ttu-id="38e18-109">0000 - 007F</span><span class="sxs-lookup"><span data-stu-id="38e18-109">0000 - 007F</span></span></td>
<td><span data-ttu-id="38e18-110">Latim básico</span><span class="sxs-lookup"><span data-stu-id="38e18-110">Basic Latin</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-111">1</span><span class="sxs-lookup"><span data-stu-id="38e18-111">1</span></span></td>
<td><span data-ttu-id="38e18-112">0080 - 00FF</span><span class="sxs-lookup"><span data-stu-id="38e18-112">0080 - 00FF</span></span></td>
<td><span data-ttu-id="38e18-113">Suplemento latino-1</span><span class="sxs-lookup"><span data-stu-id="38e18-113">Latin-1 Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-114">2</span><span class="sxs-lookup"><span data-stu-id="38e18-114">2</span></span></td>
<td><span data-ttu-id="38e18-115">0100 - 017F</span><span class="sxs-lookup"><span data-stu-id="38e18-115">0100 - 017F</span></span></td>
<td><span data-ttu-id="38e18-116">Latim estendido-A</span><span class="sxs-lookup"><span data-stu-id="38e18-116">Latin Extended-A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-117">3</span><span class="sxs-lookup"><span data-stu-id="38e18-117">3</span></span></td>
<td><span data-ttu-id="38e18-118">0180 - 024F</span><span class="sxs-lookup"><span data-stu-id="38e18-118">0180 - 024F</span></span></td>
<td><span data-ttu-id="38e18-119">Latim estendido-B</span><span class="sxs-lookup"><span data-stu-id="38e18-119">Latin Extended-B</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="38e18-120">4 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-120">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-121">0250 - 02AF</span><span class="sxs-lookup"><span data-stu-id="38e18-121">0250 - 02AF</span></span></td>
<td><span data-ttu-id="38e18-122">Extensões IPA</span><span class="sxs-lookup"><span data-stu-id="38e18-122">IPA Extensions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-123">1D00 - 1D7F</span><span class="sxs-lookup"><span data-stu-id="38e18-123">1D00 - 1D7F</span></span></td>
<td><span data-ttu-id="38e18-124">Extensões fonéticas</span><span class="sxs-lookup"><span data-stu-id="38e18-124">Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-125">1D80 - 1DBF</span><span class="sxs-lookup"><span data-stu-id="38e18-125">1D80 - 1DBF</span></span></td>
<td><span data-ttu-id="38e18-126">Suplementos de extensões fonéticas</span><span class="sxs-lookup"><span data-stu-id="38e18-126">Phonetic Extensions Supplement</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="38e18-127">5 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-127">5${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-128">02B0 - 02FF</span><span class="sxs-lookup"><span data-stu-id="38e18-128">02B0 - 02FF</span></span></td>
<td><span data-ttu-id="38e18-129">Letras do modificador de espaçamento</span><span class="sxs-lookup"><span data-stu-id="38e18-129">Spacing Modifier Letters</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-130">A700 - A71F</span><span class="sxs-lookup"><span data-stu-id="38e18-130">A700 - A71F</span></span></td>
<td><span data-ttu-id="38e18-131">Letras de Tom modificadores</span><span class="sxs-lookup"><span data-stu-id="38e18-131">Modifier Tone Letters</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="38e18-132">6 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-132">6${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-133">0300 - 036F</span><span class="sxs-lookup"><span data-stu-id="38e18-133">0300 - 036F</span></span></td>
<td><span data-ttu-id="38e18-134">Combinando marcas de sinais diacríticos</span><span class="sxs-lookup"><span data-stu-id="38e18-134">Combining Diacritical Marks</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-135">1DC0 - 1DFF</span><span class="sxs-lookup"><span data-stu-id="38e18-135">1DC0 - 1DFF</span></span></td>
<td><span data-ttu-id="38e18-136">Complemento de sinais diacríticos combináveis</span><span class="sxs-lookup"><span data-stu-id="38e18-136">Combining Diacritical Marks Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-137">7</span><span class="sxs-lookup"><span data-stu-id="38e18-137">7</span></span></td>
<td><span data-ttu-id="38e18-138">0370 - 03FF</span><span class="sxs-lookup"><span data-stu-id="38e18-138">0370 - 03FF</span></span></td>
<td><span data-ttu-id="38e18-139">Grego e cóptico</span><span class="sxs-lookup"><span data-stu-id="38e18-139">Greek and Coptic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-140">8</span><span class="sxs-lookup"><span data-stu-id="38e18-140">8</span></span></td>
<td><span data-ttu-id="38e18-141">2C80 - 2CFF</span><span class="sxs-lookup"><span data-stu-id="38e18-141">2C80 - 2CFF</span></span></td>
<td><span data-ttu-id="38e18-142">Copta</span><span class="sxs-lookup"><span data-stu-id="38e18-142">Coptic</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="38e18-143">9 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-143">9${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-144">0400 - 04FF</span><span class="sxs-lookup"><span data-stu-id="38e18-144">0400 - 04FF</span></span></td>
<td><span data-ttu-id="38e18-145">Cirílico</span><span class="sxs-lookup"><span data-stu-id="38e18-145">Cyrillic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-146">0500 - 052F</span><span class="sxs-lookup"><span data-stu-id="38e18-146">0500 - 052F</span></span></td>
<td><span data-ttu-id="38e18-147">Suplementar cirílico</span><span class="sxs-lookup"><span data-stu-id="38e18-147">Cyrillic Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-148">2DE0 - 2DFF</span><span class="sxs-lookup"><span data-stu-id="38e18-148">2DE0 - 2DFF</span></span></td>
<td><span data-ttu-id="38e18-149">Cirílico estendido-A</span><span class="sxs-lookup"><span data-stu-id="38e18-149">Cyrillic Extended-A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-150">A640 - A69F</span><span class="sxs-lookup"><span data-stu-id="38e18-150">A640 - A69F</span></span></td>
<td><span data-ttu-id="38e18-151">Cirílico estendido-B</span><span class="sxs-lookup"><span data-stu-id="38e18-151">Cyrillic Extended-B</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-152">10</span><span class="sxs-lookup"><span data-stu-id="38e18-152">10</span></span></td>
<td><span data-ttu-id="38e18-153">0530 - 058F</span><span class="sxs-lookup"><span data-stu-id="38e18-153">0530 - 058F</span></span></td>
<td><span data-ttu-id="38e18-154">Armênia</span><span class="sxs-lookup"><span data-stu-id="38e18-154">Armenian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-155">11</span><span class="sxs-lookup"><span data-stu-id="38e18-155">11</span></span></td>
<td><span data-ttu-id="38e18-156">0590 - 05FF</span><span class="sxs-lookup"><span data-stu-id="38e18-156">0590 - 05FF</span></span></td>
<td><span data-ttu-id="38e18-157">Hebraico</span><span class="sxs-lookup"><span data-stu-id="38e18-157">Hebrew</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-158">12</span><span class="sxs-lookup"><span data-stu-id="38e18-158">12</span></span></td>
<td><span data-ttu-id="38e18-159">A500 - A63F</span><span class="sxs-lookup"><span data-stu-id="38e18-159">A500 - A63F</span></span></td>
<td><span data-ttu-id="38e18-160">Vai</span><span class="sxs-lookup"><span data-stu-id="38e18-160">Vai</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="38e18-161">13 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-161">13${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-162">0600 - 06FF</span><span class="sxs-lookup"><span data-stu-id="38e18-162">0600 - 06FF</span></span></td>
<td><span data-ttu-id="38e18-163">Árabe</span><span class="sxs-lookup"><span data-stu-id="38e18-163">Arabic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-164">0750-077F</span><span class="sxs-lookup"><span data-stu-id="38e18-164">0750 - 077F</span></span></td>
<td><span data-ttu-id="38e18-165">Suplementar árabe</span><span class="sxs-lookup"><span data-stu-id="38e18-165">Arabic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-166">14</span><span class="sxs-lookup"><span data-stu-id="38e18-166">14</span></span></td>
<td><span data-ttu-id="38e18-167">07C0 - 07FF</span><span class="sxs-lookup"><span data-stu-id="38e18-167">07C0 - 07FF</span></span></td>
<td><span data-ttu-id="38e18-168">NKo</span><span class="sxs-lookup"><span data-stu-id="38e18-168">NKo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-169">15</span><span class="sxs-lookup"><span data-stu-id="38e18-169">15</span></span></td>
<td><span data-ttu-id="38e18-170">0900 - 097F</span><span class="sxs-lookup"><span data-stu-id="38e18-170">0900 - 097F</span></span></td>
<td><span data-ttu-id="38e18-171">Devanagari</span><span class="sxs-lookup"><span data-stu-id="38e18-171">Devanagari</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-172">16</span><span class="sxs-lookup"><span data-stu-id="38e18-172">16</span></span></td>
<td><span data-ttu-id="38e18-173">0980 - 09FF</span><span class="sxs-lookup"><span data-stu-id="38e18-173">0980 - 09FF</span></span></td>
<td><span data-ttu-id="38e18-174">Bangla</span><span class="sxs-lookup"><span data-stu-id="38e18-174">Bangla</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-175">17</span><span class="sxs-lookup"><span data-stu-id="38e18-175">17</span></span></td>
<td><span data-ttu-id="38e18-176">0A00 - 0A7F</span><span class="sxs-lookup"><span data-stu-id="38e18-176">0A00 - 0A7F</span></span></td>
<td><span data-ttu-id="38e18-177">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="38e18-177">Gurmukhi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-178">18</span><span class="sxs-lookup"><span data-stu-id="38e18-178">18</span></span></td>
<td><span data-ttu-id="38e18-179">0A80 - 0AFF</span><span class="sxs-lookup"><span data-stu-id="38e18-179">0A80 - 0AFF</span></span></td>
<td><span data-ttu-id="38e18-180">Guzerate</span><span class="sxs-lookup"><span data-stu-id="38e18-180">Gujarati</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-181">19</span><span class="sxs-lookup"><span data-stu-id="38e18-181">19</span></span></td>
<td><span data-ttu-id="38e18-182">0B00 - 0B7F</span><span class="sxs-lookup"><span data-stu-id="38e18-182">0B00 - 0B7F</span></span></td>
<td><span data-ttu-id="38e18-183">Oriá</span><span class="sxs-lookup"><span data-stu-id="38e18-183">Odia</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-184">20</span><span class="sxs-lookup"><span data-stu-id="38e18-184">20</span></span></td>
<td><span data-ttu-id="38e18-185">0B80 - 0BFF</span><span class="sxs-lookup"><span data-stu-id="38e18-185">0B80 - 0BFF</span></span></td>
<td><span data-ttu-id="38e18-186">Tâmil</span><span class="sxs-lookup"><span data-stu-id="38e18-186">Tamil</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-187">21</span><span class="sxs-lookup"><span data-stu-id="38e18-187">21</span></span></td>
<td><span data-ttu-id="38e18-188">0C00 - 0C7F</span><span class="sxs-lookup"><span data-stu-id="38e18-188">0C00 - 0C7F</span></span></td>
<td><span data-ttu-id="38e18-189">Télugo</span><span class="sxs-lookup"><span data-stu-id="38e18-189">Telugu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-190">22</span><span class="sxs-lookup"><span data-stu-id="38e18-190">22</span></span></td>
<td><span data-ttu-id="38e18-191">0C80 - 0CFF</span><span class="sxs-lookup"><span data-stu-id="38e18-191">0C80 - 0CFF</span></span></td>
<td><span data-ttu-id="38e18-192">canarim</span><span class="sxs-lookup"><span data-stu-id="38e18-192">Kannada</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-193">23</span><span class="sxs-lookup"><span data-stu-id="38e18-193">23</span></span></td>
<td><span data-ttu-id="38e18-194">0D00 - 0D7F</span><span class="sxs-lookup"><span data-stu-id="38e18-194">0D00 - 0D7F</span></span></td>
<td><span data-ttu-id="38e18-195">Malaiala</span><span class="sxs-lookup"><span data-stu-id="38e18-195">Malayalam</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-196">24</span><span class="sxs-lookup"><span data-stu-id="38e18-196">24</span></span></td>
<td><span data-ttu-id="38e18-197">0E00 - 0E7F</span><span class="sxs-lookup"><span data-stu-id="38e18-197">0E00 - 0E7F</span></span></td>
<td><span data-ttu-id="38e18-198">Tailandês</span><span class="sxs-lookup"><span data-stu-id="38e18-198">Thai</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-199">25</span><span class="sxs-lookup"><span data-stu-id="38e18-199">25</span></span></td>
<td><span data-ttu-id="38e18-200">0E80 - 0EFF</span><span class="sxs-lookup"><span data-stu-id="38e18-200">0E80 - 0EFF</span></span></td>
<td><span data-ttu-id="38e18-201">Lao</span><span class="sxs-lookup"><span data-stu-id="38e18-201">Lao</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="38e18-202">26 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-202">26${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-203">10A0 - 10FF</span><span class="sxs-lookup"><span data-stu-id="38e18-203">10A0 - 10FF</span></span></td>
<td><span data-ttu-id="38e18-204">Georgiano</span><span class="sxs-lookup"><span data-stu-id="38e18-204">Georgian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-205">2D00 - 2D2F</span><span class="sxs-lookup"><span data-stu-id="38e18-205">2D00 - 2D2F</span></span></td>
<td><span data-ttu-id="38e18-206">Suplemento georgiano</span><span class="sxs-lookup"><span data-stu-id="38e18-206">Georgian Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-207">27</span><span class="sxs-lookup"><span data-stu-id="38e18-207">27</span></span></td>
<td><span data-ttu-id="38e18-208">1B00 - 1B7F</span><span class="sxs-lookup"><span data-stu-id="38e18-208">1B00 - 1B7F</span></span></td>
<td><span data-ttu-id="38e18-209">Balinês</span><span class="sxs-lookup"><span data-stu-id="38e18-209">Balinese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-210">28</span><span class="sxs-lookup"><span data-stu-id="38e18-210">28</span></span></td>
<td><span data-ttu-id="38e18-211">1100 - 11FF</span><span class="sxs-lookup"><span data-stu-id="38e18-211">1100 - 11FF</span></span></td>
<td><span data-ttu-id="38e18-212">Jamo Hangul</span><span class="sxs-lookup"><span data-stu-id="38e18-212">Hangul Jamo</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="38e18-213">29 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-213">29${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-214">1E00 - 1EFF</span><span class="sxs-lookup"><span data-stu-id="38e18-214">1E00 - 1EFF</span></span></td>
<td><span data-ttu-id="38e18-215">Latim estendido adicional</span><span class="sxs-lookup"><span data-stu-id="38e18-215">Latin Extended Additional</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-216">2C60 - 2C7F</span><span class="sxs-lookup"><span data-stu-id="38e18-216">2C60 - 2C7F</span></span></td>
<td><span data-ttu-id="38e18-217">Latim estendido-C</span><span class="sxs-lookup"><span data-stu-id="38e18-217">Latin Extended-C</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-218">A720 - A7FF</span><span class="sxs-lookup"><span data-stu-id="38e18-218">A720 - A7FF</span></span></td>
<td><span data-ttu-id="38e18-219">Latim estendido-D</span><span class="sxs-lookup"><span data-stu-id="38e18-219">Latin Extended-D</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-220">30</span><span class="sxs-lookup"><span data-stu-id="38e18-220">30</span></span></td>
<td><span data-ttu-id="38e18-221">1F00 - 1FFF</span><span class="sxs-lookup"><span data-stu-id="38e18-221">1F00 - 1FFF</span></span></td>
<td><span data-ttu-id="38e18-222">Grego estendido</span><span class="sxs-lookup"><span data-stu-id="38e18-222">Greek Extended</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="38e18-223">31 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-223">31${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-224">2000 - 206F</span><span class="sxs-lookup"><span data-stu-id="38e18-224">2000 - 206F</span></span></td>
<td><span data-ttu-id="38e18-225">Pontuação geral</span><span class="sxs-lookup"><span data-stu-id="38e18-225">General Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-226">2E00 - 2E7F</span><span class="sxs-lookup"><span data-stu-id="38e18-226">2E00 - 2E7F</span></span></td>
<td><span data-ttu-id="38e18-227">Pontuação suplementar</span><span class="sxs-lookup"><span data-stu-id="38e18-227">Supplemental Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-228">32</span><span class="sxs-lookup"><span data-stu-id="38e18-228">32</span></span></td>
<td><span data-ttu-id="38e18-229">2070 - 209F</span><span class="sxs-lookup"><span data-stu-id="38e18-229">2070 - 209F</span></span></td>
<td><span data-ttu-id="38e18-230">Sobrescritos e subscritos</span><span class="sxs-lookup"><span data-stu-id="38e18-230">Superscripts And Subscripts</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-231">33</span><span class="sxs-lookup"><span data-stu-id="38e18-231">33</span></span></td>
<td><span data-ttu-id="38e18-232">20A0 - 20CF</span><span class="sxs-lookup"><span data-stu-id="38e18-232">20A0 - 20CF</span></span></td>
<td><span data-ttu-id="38e18-233">Símbolos de moeda</span><span class="sxs-lookup"><span data-stu-id="38e18-233">Currency Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-234">34</span><span class="sxs-lookup"><span data-stu-id="38e18-234">34</span></span></td>
<td><span data-ttu-id="38e18-235">20D0 - 20FF</span><span class="sxs-lookup"><span data-stu-id="38e18-235">20D0 - 20FF</span></span></td>
<td><span data-ttu-id="38e18-236">Combinando marcas de sinais diacríticos para símbolos</span><span class="sxs-lookup"><span data-stu-id="38e18-236">Combining Diacritical Marks For Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-237">35</span><span class="sxs-lookup"><span data-stu-id="38e18-237">35</span></span></td>
<td><span data-ttu-id="38e18-238">2100 - 214F</span><span class="sxs-lookup"><span data-stu-id="38e18-238">2100 - 214F</span></span></td>
<td><span data-ttu-id="38e18-239">Símbolos Letterlike</span><span class="sxs-lookup"><span data-stu-id="38e18-239">Letterlike Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-240">36</span><span class="sxs-lookup"><span data-stu-id="38e18-240">36</span></span></td>
<td><span data-ttu-id="38e18-241">2150 - 218F</span><span class="sxs-lookup"><span data-stu-id="38e18-241">2150 - 218F</span></span></td>
<td><span data-ttu-id="38e18-242">Formulários de número</span><span class="sxs-lookup"><span data-stu-id="38e18-242">Number Forms</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="38e18-243">37 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-243">37${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-244">2190 - 21FF</span><span class="sxs-lookup"><span data-stu-id="38e18-244">2190 - 21FF</span></span></td>
<td><span data-ttu-id="38e18-245">Setas</span><span class="sxs-lookup"><span data-stu-id="38e18-245">Arrows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-246">27F0 - 27FF</span><span class="sxs-lookup"><span data-stu-id="38e18-246">27F0 - 27FF</span></span></td>
<td><span data-ttu-id="38e18-247">Setas suplementares-A</span><span class="sxs-lookup"><span data-stu-id="38e18-247">Supplemental Arrows-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-248">2900 - 297F</span><span class="sxs-lookup"><span data-stu-id="38e18-248">2900 - 297F</span></span></td>
<td><span data-ttu-id="38e18-249">Setas suplementares-B</span><span class="sxs-lookup"><span data-stu-id="38e18-249">Supplemental Arrows-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-250">2B00 - 2BFF</span><span class="sxs-lookup"><span data-stu-id="38e18-250">2B00 - 2BFF</span></span></td>
<td><span data-ttu-id="38e18-251">Símbolos e setas diversos</span><span class="sxs-lookup"><span data-stu-id="38e18-251">Miscellaneous Symbols and Arrows</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="38e18-252">38 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-252">38${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-253">2200 - 22FF</span><span class="sxs-lookup"><span data-stu-id="38e18-253">2200 - 22FF</span></span></td>
<td><span data-ttu-id="38e18-254">Operadores matemáticos</span><span class="sxs-lookup"><span data-stu-id="38e18-254">Mathematical Operators</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-255">27C0 - 27EF</span><span class="sxs-lookup"><span data-stu-id="38e18-255">27C0 - 27EF</span></span></td>
<td><span data-ttu-id="38e18-256">Símbolos matemáticos diversos-A</span><span class="sxs-lookup"><span data-stu-id="38e18-256">Miscellaneous Mathematical Symbols-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-257">2980 - 29FF</span><span class="sxs-lookup"><span data-stu-id="38e18-257">2980 - 29FF</span></span></td>
<td><span data-ttu-id="38e18-258">Símbolos matemáticos diversos-B</span><span class="sxs-lookup"><span data-stu-id="38e18-258">Miscellaneous Mathematical Symbols-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-259">2A00 - 2AFF</span><span class="sxs-lookup"><span data-stu-id="38e18-259">2A00 - 2AFF</span></span></td>
<td><span data-ttu-id="38e18-260">Operadores matemáticos complementares</span><span class="sxs-lookup"><span data-stu-id="38e18-260">Supplemental Mathematical Operators</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-261">39</span><span class="sxs-lookup"><span data-stu-id="38e18-261">39</span></span></td>
<td><span data-ttu-id="38e18-262">2300 - 23FF</span><span class="sxs-lookup"><span data-stu-id="38e18-262">2300 - 23FF</span></span></td>
<td><span data-ttu-id="38e18-263">Técnicos diversos</span><span class="sxs-lookup"><span data-stu-id="38e18-263">Miscellaneous Technical</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-264">40</span><span class="sxs-lookup"><span data-stu-id="38e18-264">40</span></span></td>
<td><span data-ttu-id="38e18-265">2400 - 243F</span><span class="sxs-lookup"><span data-stu-id="38e18-265">2400 - 243F</span></span></td>
<td><span data-ttu-id="38e18-266">Imagens de controle</span><span class="sxs-lookup"><span data-stu-id="38e18-266">Control Pictures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-267">41</span><span class="sxs-lookup"><span data-stu-id="38e18-267">41</span></span></td>
<td><span data-ttu-id="38e18-268">2440 - 245F</span><span class="sxs-lookup"><span data-stu-id="38e18-268">2440 - 245F</span></span></td>
<td><span data-ttu-id="38e18-269">Reconhecimento óptico de caracteres</span><span class="sxs-lookup"><span data-stu-id="38e18-269">Optical Character Recognition</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-270">42</span><span class="sxs-lookup"><span data-stu-id="38e18-270">42</span></span></td>
<td><span data-ttu-id="38e18-271">2460 - 24FF</span><span class="sxs-lookup"><span data-stu-id="38e18-271">2460 - 24FF</span></span></td>
<td><span data-ttu-id="38e18-272">Alfanuméricos embutidos</span><span class="sxs-lookup"><span data-stu-id="38e18-272">Enclosed Alphanumerics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-273">43</span><span class="sxs-lookup"><span data-stu-id="38e18-273">43</span></span></td>
<td><span data-ttu-id="38e18-274">2500 - 257F</span><span class="sxs-lookup"><span data-stu-id="38e18-274">2500 - 257F</span></span></td>
<td><span data-ttu-id="38e18-275">Desenho de caixa</span><span class="sxs-lookup"><span data-stu-id="38e18-275">Box Drawing</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-276">44</span><span class="sxs-lookup"><span data-stu-id="38e18-276">44</span></span></td>
<td><span data-ttu-id="38e18-277">2580 - 259F</span><span class="sxs-lookup"><span data-stu-id="38e18-277">2580 - 259F</span></span></td>
<td><span data-ttu-id="38e18-278">Elementos de bloco</span><span class="sxs-lookup"><span data-stu-id="38e18-278">Block Elements</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-279">45</span><span class="sxs-lookup"><span data-stu-id="38e18-279">45</span></span></td>
<td><span data-ttu-id="38e18-280">25A0 - 25FF</span><span class="sxs-lookup"><span data-stu-id="38e18-280">25A0 - 25FF</span></span></td>
<td><span data-ttu-id="38e18-281">Formas geométricas</span><span class="sxs-lookup"><span data-stu-id="38e18-281">Geometric Shapes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-282">46</span><span class="sxs-lookup"><span data-stu-id="38e18-282">46</span></span></td>
<td><span data-ttu-id="38e18-283">2600 - 26FF</span><span class="sxs-lookup"><span data-stu-id="38e18-283">2600 - 26FF</span></span></td>
<td><span data-ttu-id="38e18-284">Símbolos diversos</span><span class="sxs-lookup"><span data-stu-id="38e18-284">Miscellaneous Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-285">47</span><span class="sxs-lookup"><span data-stu-id="38e18-285">47</span></span></td>
<td><span data-ttu-id="38e18-286">2700 - 27BF</span><span class="sxs-lookup"><span data-stu-id="38e18-286">2700 - 27BF</span></span></td>
<td><span data-ttu-id="38e18-287">Dingbats</span><span class="sxs-lookup"><span data-stu-id="38e18-287">Dingbats</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-288">48</span><span class="sxs-lookup"><span data-stu-id="38e18-288">48</span></span></td>
<td><span data-ttu-id="38e18-289">3000 - 303F</span><span class="sxs-lookup"><span data-stu-id="38e18-289">3000 - 303F</span></span></td>
<td><span data-ttu-id="38e18-290">Símbolos CJK e Pontuação</span><span class="sxs-lookup"><span data-stu-id="38e18-290">CJK Symbols And Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-291">49</span><span class="sxs-lookup"><span data-stu-id="38e18-291">49</span></span></td>
<td><span data-ttu-id="38e18-292">3040 - 309F</span><span class="sxs-lookup"><span data-stu-id="38e18-292">3040 - 309F</span></span></td>
<td><span data-ttu-id="38e18-293">Hiragana</span><span class="sxs-lookup"><span data-stu-id="38e18-293">Hiragana</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="38e18-294">50 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-294">50${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-295">30A0 - 30FF</span><span class="sxs-lookup"><span data-stu-id="38e18-295">30A0 - 30FF</span></span></td>
<td><span data-ttu-id="38e18-296">Katakana</span><span class="sxs-lookup"><span data-stu-id="38e18-296">Katakana</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-297">31F0 - 31FF</span><span class="sxs-lookup"><span data-stu-id="38e18-297">31F0 - 31FF</span></span></td>
<td><span data-ttu-id="38e18-298">Extensões fonéticas em katakana</span><span class="sxs-lookup"><span data-stu-id="38e18-298">Katakana Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="38e18-299">51 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-299">51${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-300">3100 - 312F</span><span class="sxs-lookup"><span data-stu-id="38e18-300">3100 - 312F</span></span></td>
<td><span data-ttu-id="38e18-301">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="38e18-301">Bopomofo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-302">31A0 - 31BF</span><span class="sxs-lookup"><span data-stu-id="38e18-302">31A0 - 31BF</span></span></td>
<td><span data-ttu-id="38e18-303">Bopomofo estendido</span><span class="sxs-lookup"><span data-stu-id="38e18-303">Bopomofo Extended</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-304">52</span><span class="sxs-lookup"><span data-stu-id="38e18-304">52</span></span></td>
<td><span data-ttu-id="38e18-305">3130 - 318F</span><span class="sxs-lookup"><span data-stu-id="38e18-305">3130 - 318F</span></span></td>
<td><span data-ttu-id="38e18-306">Hangul de compatibilidade com Jamo</span><span class="sxs-lookup"><span data-stu-id="38e18-306">Hangul Compatibility Jamo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-307">53</span><span class="sxs-lookup"><span data-stu-id="38e18-307">53</span></span></td>
<td><span data-ttu-id="38e18-308">A840 - A87F</span><span class="sxs-lookup"><span data-stu-id="38e18-308">A840 - A87F</span></span></td>
<td><span data-ttu-id="38e18-309">Phags-Pa</span><span class="sxs-lookup"><span data-stu-id="38e18-309">Phags-pa</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-310">54</span><span class="sxs-lookup"><span data-stu-id="38e18-310">54</span></span></td>
<td><span data-ttu-id="38e18-311">3200 - 32FF</span><span class="sxs-lookup"><span data-stu-id="38e18-311">3200 - 32FF</span></span></td>
<td><span data-ttu-id="38e18-312">Letras e meses CJK incluídos</span><span class="sxs-lookup"><span data-stu-id="38e18-312">Enclosed CJK Letters And Months</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-313">55</span><span class="sxs-lookup"><span data-stu-id="38e18-313">55</span></span></td>
<td><span data-ttu-id="38e18-314">3300 - 33FF</span><span class="sxs-lookup"><span data-stu-id="38e18-314">3300 - 33FF</span></span></td>
<td><span data-ttu-id="38e18-315">Compatibilidade com CJK</span><span class="sxs-lookup"><span data-stu-id="38e18-315">CJK Compatibility</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-316">56</span><span class="sxs-lookup"><span data-stu-id="38e18-316">56</span></span></td>
<td><span data-ttu-id="38e18-317">AC00 - D7AF</span><span class="sxs-lookup"><span data-stu-id="38e18-317">AC00 - D7AF</span></span></td>
<td><span data-ttu-id="38e18-318">Sílabas Hangul</span><span class="sxs-lookup"><span data-stu-id="38e18-318">Hangul Syllables</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-319">57</span><span class="sxs-lookup"><span data-stu-id="38e18-319">57</span></span></td>
<td><span data-ttu-id="38e18-320">D800-DFFF</span><span class="sxs-lookup"><span data-stu-id="38e18-320">D800 - DFFF</span></span></td>
<td><span data-ttu-id="38e18-321">Não plano 0.</span><span class="sxs-lookup"><span data-stu-id="38e18-321">Non-Plane 0.</span></span> <span data-ttu-id="38e18-322">Observe que a configuração desse bit implica que há pelo menos um ponto de código suplementar além do BMP (plano multilíngue) básico que é suportado por essa fonte.</span><span class="sxs-lookup"><span data-stu-id="38e18-322">Note that setting this bit implies that there is at least one supplementary code point beyond the Basic Multilingual Plane (BMP) that is supported by this font.</span></span> <span data-ttu-id="38e18-323">Consulte <a href="surrogates-and-supplementary-characters.md">substitutos e caracteres suplementares</a>.</span><span class="sxs-lookup"><span data-stu-id="38e18-323">See <a href="surrogates-and-supplementary-characters.md">Surrogates and Supplementary Characters</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-324">58</span><span class="sxs-lookup"><span data-stu-id="38e18-324">58</span></span></td>
<td><span data-ttu-id="38e18-325">10900-1091F</span><span class="sxs-lookup"><span data-stu-id="38e18-325">10900 - 1091F</span></span></td>
<td><span data-ttu-id="38e18-326">Fenícia</span><span class="sxs-lookup"><span data-stu-id="38e18-326">Phoenician</span></span></td>
</tr>
<tr class="even">
<td rowspan="7"><span data-ttu-id="38e18-327">59 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-327">59${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-328">2E80 - 2EFF</span><span class="sxs-lookup"><span data-stu-id="38e18-328">2E80 - 2EFF</span></span></td>
<td><span data-ttu-id="38e18-329">Suplemento de radicais CJK</span><span class="sxs-lookup"><span data-stu-id="38e18-329">CJK Radicals Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-330">2F00 - 2FDF</span><span class="sxs-lookup"><span data-stu-id="38e18-330">2F00 - 2FDF</span></span></td>
<td><span data-ttu-id="38e18-331">Radicais da Kangxi</span><span class="sxs-lookup"><span data-stu-id="38e18-331">Kangxi Radicals</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-332">2FF0 - 2FFF</span><span class="sxs-lookup"><span data-stu-id="38e18-332">2FF0 - 2FFF</span></span></td>
<td><span data-ttu-id="38e18-333">Caracteres de descrição ideográfica</span><span class="sxs-lookup"><span data-stu-id="38e18-333">Ideographic Description Characters</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-334">3190 - 319F</span><span class="sxs-lookup"><span data-stu-id="38e18-334">3190 - 319F</span></span></td>
<td><span data-ttu-id="38e18-335">Kanbun</span><span class="sxs-lookup"><span data-stu-id="38e18-335">Kanbun</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-336">3400 - 4DBF</span><span class="sxs-lookup"><span data-stu-id="38e18-336">3400 - 4DBF</span></span></td>
<td><span data-ttu-id="38e18-337">Extensão A de ideogramas unificadas CJK</span><span class="sxs-lookup"><span data-stu-id="38e18-337">CJK Unified Ideographs Extension A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-338">4E00 - 9FFF</span><span class="sxs-lookup"><span data-stu-id="38e18-338">4E00 - 9FFF</span></span></td>
<td><span data-ttu-id="38e18-339">Ideogramas unificadas CJK</span><span class="sxs-lookup"><span data-stu-id="38e18-339">CJK Unified Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-340">20000-2A6DF</span><span class="sxs-lookup"><span data-stu-id="38e18-340">20000 - 2A6DF</span></span></td>
<td><span data-ttu-id="38e18-341">Extensão de ideogramas unificadas CJK B</span><span class="sxs-lookup"><span data-stu-id="38e18-341">CJK Unified Ideographs Extension B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-342">60</span><span class="sxs-lookup"><span data-stu-id="38e18-342">60</span></span></td>
<td><span data-ttu-id="38e18-343">E000 - F8FF</span><span class="sxs-lookup"><span data-stu-id="38e18-343">E000 - F8FF</span></span></td>
<td><span data-ttu-id="38e18-344">Área de uso particular</span><span class="sxs-lookup"><span data-stu-id="38e18-344">Private Use Area</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="38e18-345">61 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-345">61${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-346">31C0 - 31EF</span><span class="sxs-lookup"><span data-stu-id="38e18-346">31C0 - 31EF</span></span></td>
<td><span data-ttu-id="38e18-347">Traços CJK</span><span class="sxs-lookup"><span data-stu-id="38e18-347">CJK Strokes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-348">F900 - FAFF</span><span class="sxs-lookup"><span data-stu-id="38e18-348">F900 - FAFF</span></span></td>
<td><span data-ttu-id="38e18-349">Ideogramas de compatibilidade CJK</span><span class="sxs-lookup"><span data-stu-id="38e18-349">CJK Compatibility Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-350">2F800 - 2FA1F</span><span class="sxs-lookup"><span data-stu-id="38e18-350">2F800 - 2FA1F</span></span></td>
<td><span data-ttu-id="38e18-351">Suplementos de ideogramas de compatibilidade CJK</span><span class="sxs-lookup"><span data-stu-id="38e18-351">CJK Compatibility Ideographs Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-352">62</span><span class="sxs-lookup"><span data-stu-id="38e18-352">62</span></span></td>
<td><span data-ttu-id="38e18-353">FB00 - FB4F</span><span class="sxs-lookup"><span data-stu-id="38e18-353">FB00 - FB4F</span></span></td>
<td><span data-ttu-id="38e18-354">Formulários de apresentação alfabética</span><span class="sxs-lookup"><span data-stu-id="38e18-354">Alphabetic Presentation Forms</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-355">63</span><span class="sxs-lookup"><span data-stu-id="38e18-355">63</span></span></td>
<td><span data-ttu-id="38e18-356">FB50 - FDFF</span><span class="sxs-lookup"><span data-stu-id="38e18-356">FB50 - FDFF</span></span></td>
<td><span data-ttu-id="38e18-357">Formulários de apresentação em árabe – A</span><span class="sxs-lookup"><span data-stu-id="38e18-357">Arabic Presentation Forms-A</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-358">64</span><span class="sxs-lookup"><span data-stu-id="38e18-358">64</span></span></td>
<td><span data-ttu-id="38e18-359">FE20 - FE2F</span><span class="sxs-lookup"><span data-stu-id="38e18-359">FE20 - FE2F</span></span></td>
<td><span data-ttu-id="38e18-360">Combinando metades das marcas</span><span class="sxs-lookup"><span data-stu-id="38e18-360">Combining Half Marks</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="38e18-361">65 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-361">65${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-362">FE10 - FE1F</span><span class="sxs-lookup"><span data-stu-id="38e18-362">FE10 - FE1F</span></span></td>
<td><span data-ttu-id="38e18-363">Formulários verticais</span><span class="sxs-lookup"><span data-stu-id="38e18-363">Vertical Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-364">FE30 - FE4F</span><span class="sxs-lookup"><span data-stu-id="38e18-364">FE30 - FE4F</span></span></td>
<td><span data-ttu-id="38e18-365">Formulários de compatibilidade CJK</span><span class="sxs-lookup"><span data-stu-id="38e18-365">CJK Compatibility Forms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-366">66</span><span class="sxs-lookup"><span data-stu-id="38e18-366">66</span></span></td>
<td><span data-ttu-id="38e18-367">FE50 - FE6F</span><span class="sxs-lookup"><span data-stu-id="38e18-367">FE50 - FE6F</span></span></td>
<td><span data-ttu-id="38e18-368">Variantes de forma pequena</span><span class="sxs-lookup"><span data-stu-id="38e18-368">Small Form Variants</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-369">67</span><span class="sxs-lookup"><span data-stu-id="38e18-369">67</span></span></td>
<td><span data-ttu-id="38e18-370">FE70 - FEFF</span><span class="sxs-lookup"><span data-stu-id="38e18-370">FE70 - FEFF</span></span></td>
<td><span data-ttu-id="38e18-371">Formulários de apresentação em árabe-B</span><span class="sxs-lookup"><span data-stu-id="38e18-371">Arabic Presentation Forms-B</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-372">68</span><span class="sxs-lookup"><span data-stu-id="38e18-372">68</span></span></td>
<td><span data-ttu-id="38e18-373">FF00 - FFEF</span><span class="sxs-lookup"><span data-stu-id="38e18-373">FF00 - FFEF</span></span></td>
<td><span data-ttu-id="38e18-374">Formas de largura e largura total</span><span class="sxs-lookup"><span data-stu-id="38e18-374">Halfwidth And Fullwidth Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-375">69</span><span class="sxs-lookup"><span data-stu-id="38e18-375">69</span></span></td>
<td><span data-ttu-id="38e18-376">FFF0 - FFFF</span><span class="sxs-lookup"><span data-stu-id="38e18-376">FFF0 - FFFF</span></span></td>
<td><span data-ttu-id="38e18-377">Especialidades</span><span class="sxs-lookup"><span data-stu-id="38e18-377">Specials</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-378">70</span><span class="sxs-lookup"><span data-stu-id="38e18-378">70</span></span></td>
<td><span data-ttu-id="38e18-379">0F00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="38e18-379">0F00 - 0FFF</span></span></td>
<td><span data-ttu-id="38e18-380">Tibetano</span><span class="sxs-lookup"><span data-stu-id="38e18-380">Tibetan</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-381">71</span><span class="sxs-lookup"><span data-stu-id="38e18-381">71</span></span></td>
<td><span data-ttu-id="38e18-382">0700 - 074F</span><span class="sxs-lookup"><span data-stu-id="38e18-382">0700 - 074F</span></span></td>
<td><span data-ttu-id="38e18-383">Siríaco</span><span class="sxs-lookup"><span data-stu-id="38e18-383">Syriac</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-384">72</span><span class="sxs-lookup"><span data-stu-id="38e18-384">72</span></span></td>
<td><span data-ttu-id="38e18-385">0780 - 07BF</span><span class="sxs-lookup"><span data-stu-id="38e18-385">0780 - 07BF</span></span></td>
<td><span data-ttu-id="38e18-386">Thaana</span><span class="sxs-lookup"><span data-stu-id="38e18-386">Thaana</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-387">73</span><span class="sxs-lookup"><span data-stu-id="38e18-387">73</span></span></td>
<td><span data-ttu-id="38e18-388">0D80 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="38e18-388">0D80 - 0DFF</span></span></td>
<td><span data-ttu-id="38e18-389">Sinhala</span><span class="sxs-lookup"><span data-stu-id="38e18-389">Sinhala</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-390">74</span><span class="sxs-lookup"><span data-stu-id="38e18-390">74</span></span></td>
<td><span data-ttu-id="38e18-391">1000 - 109F</span><span class="sxs-lookup"><span data-stu-id="38e18-391">1000 - 109F</span></span></td>
<td><span data-ttu-id="38e18-392">Myanmar</span><span class="sxs-lookup"><span data-stu-id="38e18-392">Myanmar</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="38e18-393">75 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-393">75${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-394">1200 - 137F</span><span class="sxs-lookup"><span data-stu-id="38e18-394">1200 - 137F</span></span></td>
<td><span data-ttu-id="38e18-395">Etíope</span><span class="sxs-lookup"><span data-stu-id="38e18-395">Ethiopic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-396">1380-139F</span><span class="sxs-lookup"><span data-stu-id="38e18-396">1380 - 139F</span></span></td>
<td><span data-ttu-id="38e18-397">Suplemento Etíope</span><span class="sxs-lookup"><span data-stu-id="38e18-397">Ethiopic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-398">2D80 - 2DDF</span><span class="sxs-lookup"><span data-stu-id="38e18-398">2D80 - 2DDF</span></span></td>
<td><span data-ttu-id="38e18-399">Etíope estendido</span><span class="sxs-lookup"><span data-stu-id="38e18-399">Ethiopic Extended</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-400">76</span><span class="sxs-lookup"><span data-stu-id="38e18-400">76</span></span></td>
<td><span data-ttu-id="38e18-401">13A0 - 13FF</span><span class="sxs-lookup"><span data-stu-id="38e18-401">13A0 - 13FF</span></span></td>
<td><span data-ttu-id="38e18-402">Cherokee</span><span class="sxs-lookup"><span data-stu-id="38e18-402">Cherokee</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-403">77</span><span class="sxs-lookup"><span data-stu-id="38e18-403">77</span></span></td>
<td><span data-ttu-id="38e18-404">1400 - 167F</span><span class="sxs-lookup"><span data-stu-id="38e18-404">1400 - 167F</span></span></td>
<td><span data-ttu-id="38e18-405">Silábico Aboriginal canadense unificado</span><span class="sxs-lookup"><span data-stu-id="38e18-405">Unified Canadian Aboriginal Syllabics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-406">78</span><span class="sxs-lookup"><span data-stu-id="38e18-406">78</span></span></td>
<td><span data-ttu-id="38e18-407">1680 - 169F</span><span class="sxs-lookup"><span data-stu-id="38e18-407">1680 - 169F</span></span></td>
<td><span data-ttu-id="38e18-408">Ogham</span><span class="sxs-lookup"><span data-stu-id="38e18-408">Ogham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-409">79</span><span class="sxs-lookup"><span data-stu-id="38e18-409">79</span></span></td>
<td><span data-ttu-id="38e18-410">16A0 - 16FF</span><span class="sxs-lookup"><span data-stu-id="38e18-410">16A0 - 16FF</span></span></td>
<td><span data-ttu-id="38e18-411">Rúnica</span><span class="sxs-lookup"><span data-stu-id="38e18-411">Runic</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="38e18-412">80 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-412">80${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-413">1780 - 17FF</span><span class="sxs-lookup"><span data-stu-id="38e18-413">1780 - 17FF</span></span></td>
<td><span data-ttu-id="38e18-414">Khmer</span><span class="sxs-lookup"><span data-stu-id="38e18-414">Khmer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-415">19E0 - 19FF</span><span class="sxs-lookup"><span data-stu-id="38e18-415">19E0 - 19FF</span></span></td>
<td><span data-ttu-id="38e18-416">Símbolos Khmer</span><span class="sxs-lookup"><span data-stu-id="38e18-416">Khmer Symbols</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-417">81</span><span class="sxs-lookup"><span data-stu-id="38e18-417">81</span></span></td>
<td><span data-ttu-id="38e18-418">1800 - 18AF</span><span class="sxs-lookup"><span data-stu-id="38e18-418">1800 - 18AF</span></span></td>
<td><span data-ttu-id="38e18-419">Mongol</span><span class="sxs-lookup"><span data-stu-id="38e18-419">Mongolian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-420">82</span><span class="sxs-lookup"><span data-stu-id="38e18-420">82</span></span></td>
<td><span data-ttu-id="38e18-421">2800 - 28FF</span><span class="sxs-lookup"><span data-stu-id="38e18-421">2800 - 28FF</span></span></td>
<td><span data-ttu-id="38e18-422">Padrões de braille</span><span class="sxs-lookup"><span data-stu-id="38e18-422">Braille Patterns</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="38e18-423">83 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-423">83${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-424">A000 - A48F</span><span class="sxs-lookup"><span data-stu-id="38e18-424">A000 - A48F</span></span></td>
<td><span data-ttu-id="38e18-425">Sílabas Yi</span><span class="sxs-lookup"><span data-stu-id="38e18-425">Yi Syllables</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-426">A490 - A4CF</span><span class="sxs-lookup"><span data-stu-id="38e18-426">A490 - A4CF</span></span></td>
<td><span data-ttu-id="38e18-427">Radicais Yi</span><span class="sxs-lookup"><span data-stu-id="38e18-427">Yi Radicals</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="38e18-428">84 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-428">84${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-429">1700 - 171F</span><span class="sxs-lookup"><span data-stu-id="38e18-429">1700 - 171F</span></span></td>
<td><span data-ttu-id="38e18-430">Tagalo</span><span class="sxs-lookup"><span data-stu-id="38e18-430">Tagalog</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-431">1720 - 173F</span><span class="sxs-lookup"><span data-stu-id="38e18-431">1720 - 173F</span></span></td>
<td><span data-ttu-id="38e18-432">Hanunoo</span><span class="sxs-lookup"><span data-stu-id="38e18-432">Hanunoo</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-433">1740 - 175F</span><span class="sxs-lookup"><span data-stu-id="38e18-433">1740 - 175F</span></span></td>
<td><span data-ttu-id="38e18-434">Buhid</span><span class="sxs-lookup"><span data-stu-id="38e18-434">Buhid</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-435">1760 - 177F</span><span class="sxs-lookup"><span data-stu-id="38e18-435">1760 - 177F</span></span></td>
<td><span data-ttu-id="38e18-436">Tagbanwa</span><span class="sxs-lookup"><span data-stu-id="38e18-436">Tagbanwa</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-437">85</span><span class="sxs-lookup"><span data-stu-id="38e18-437">85</span></span></td>
<td><span data-ttu-id="38e18-438">10300-1032F</span><span class="sxs-lookup"><span data-stu-id="38e18-438">10300 - 1032F</span></span></td>
<td><span data-ttu-id="38e18-439">Itálico antigo</span><span class="sxs-lookup"><span data-stu-id="38e18-439">Old Italic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-440">86</span><span class="sxs-lookup"><span data-stu-id="38e18-440">86</span></span></td>
<td><span data-ttu-id="38e18-441">10330-1034F</span><span class="sxs-lookup"><span data-stu-id="38e18-441">10330 - 1034F</span></span></td>
<td><span data-ttu-id="38e18-442">Gothic</span><span class="sxs-lookup"><span data-stu-id="38e18-442">Gothic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-443">87</span><span class="sxs-lookup"><span data-stu-id="38e18-443">87</span></span></td>
<td><span data-ttu-id="38e18-444">10400-1044F</span><span class="sxs-lookup"><span data-stu-id="38e18-444">10400 - 1044F</span></span></td>
<td><span data-ttu-id="38e18-445">Deseret</span><span class="sxs-lookup"><span data-stu-id="38e18-445">Deseret</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="38e18-446">88 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-446">88${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-447">1D000 - 1D0FF</span><span class="sxs-lookup"><span data-stu-id="38e18-447">1D000 - 1D0FF</span></span></td>
<td><span data-ttu-id="38e18-448">Símbolos símbolos musicais</span><span class="sxs-lookup"><span data-stu-id="38e18-448">Byzantine Musical Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-449">1D100 - 1D1FF</span><span class="sxs-lookup"><span data-stu-id="38e18-449">1D100 - 1D1FF</span></span></td>
<td><span data-ttu-id="38e18-450">Símbolos musicais</span><span class="sxs-lookup"><span data-stu-id="38e18-450">Musical Symbols</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-451">1D200 - 1D24F</span><span class="sxs-lookup"><span data-stu-id="38e18-451">1D200 - 1D24F</span></span></td>
<td><span data-ttu-id="38e18-452">Notação musical grega antiga</span><span class="sxs-lookup"><span data-stu-id="38e18-452">Ancient Greek Musical Notation</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-453">89</span><span class="sxs-lookup"><span data-stu-id="38e18-453">89</span></span></td>
<td><span data-ttu-id="38e18-454">1D400 - 1D7FF</span><span class="sxs-lookup"><span data-stu-id="38e18-454">1D400 - 1D7FF</span></span></td>
<td><span data-ttu-id="38e18-455">Símbolos alfanuméricos matemáticos</span><span class="sxs-lookup"><span data-stu-id="38e18-455">Mathematical Alphanumeric Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="38e18-456">90 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-456">90${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-457">FF000-FFFF</span><span class="sxs-lookup"><span data-stu-id="38e18-457">FF000 - FFFFD</span></span></td>
<td><span data-ttu-id="38e18-458">Uso privado (plano 15)</span><span class="sxs-lookup"><span data-stu-id="38e18-458">Private Use (plane 15)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-459">100000-10FFFD</span><span class="sxs-lookup"><span data-stu-id="38e18-459">100000 - 10FFFD</span></span></td>
<td><span data-ttu-id="38e18-460">Uso privado (plano 16)</span><span class="sxs-lookup"><span data-stu-id="38e18-460">Private Use (plane 16)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="38e18-461">91 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-461">91${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-462">FE00 - FE0F</span><span class="sxs-lookup"><span data-stu-id="38e18-462">FE00 - FE0F</span></span></td>
<td><span data-ttu-id="38e18-463">Seletores de variação</span><span class="sxs-lookup"><span data-stu-id="38e18-463">Variation Selectors</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-464">E0100 - E01EF</span><span class="sxs-lookup"><span data-stu-id="38e18-464">E0100 - E01EF</span></span></td>
<td><span data-ttu-id="38e18-465">Suplemento seletores de variação</span><span class="sxs-lookup"><span data-stu-id="38e18-465">Variation Selectors Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-466">92</span><span class="sxs-lookup"><span data-stu-id="38e18-466">92</span></span></td>
<td><span data-ttu-id="38e18-467">E0000 - E007F</span><span class="sxs-lookup"><span data-stu-id="38e18-467">E0000 - E007F</span></span></td>
<td><span data-ttu-id="38e18-468">Marcações</span><span class="sxs-lookup"><span data-stu-id="38e18-468">Tags</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-469">93</span><span class="sxs-lookup"><span data-stu-id="38e18-469">93</span></span></td>
<td><span data-ttu-id="38e18-470">1900 - 194F</span><span class="sxs-lookup"><span data-stu-id="38e18-470">1900 - 194F</span></span></td>
<td><span data-ttu-id="38e18-471">Limbu</span><span class="sxs-lookup"><span data-stu-id="38e18-471">Limbu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-472">94</span><span class="sxs-lookup"><span data-stu-id="38e18-472">94</span></span></td>
<td><span data-ttu-id="38e18-473">1950 - 197F</span><span class="sxs-lookup"><span data-stu-id="38e18-473">1950 - 197F</span></span></td>
<td><span data-ttu-id="38e18-474">Tai Le</span><span class="sxs-lookup"><span data-stu-id="38e18-474">Tai Le</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-475">95</span><span class="sxs-lookup"><span data-stu-id="38e18-475">95</span></span></td>
<td><span data-ttu-id="38e18-476">1980-19DF</span><span class="sxs-lookup"><span data-stu-id="38e18-476">1980 - 19DF</span></span></td>
<td><span data-ttu-id="38e18-477">Tai Lue Novo</span><span class="sxs-lookup"><span data-stu-id="38e18-477">New Tai Lue</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-478">96</span><span class="sxs-lookup"><span data-stu-id="38e18-478">96</span></span></td>
<td><span data-ttu-id="38e18-479">1A00 - 1A1F</span><span class="sxs-lookup"><span data-stu-id="38e18-479">1A00 - 1A1F</span></span></td>
<td><span data-ttu-id="38e18-480">Bugi</span><span class="sxs-lookup"><span data-stu-id="38e18-480">Buginese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-481">97</span><span class="sxs-lookup"><span data-stu-id="38e18-481">97</span></span></td>
<td><span data-ttu-id="38e18-482">2C00 - 2C5F</span><span class="sxs-lookup"><span data-stu-id="38e18-482">2C00 - 2C5F</span></span></td>
<td><span data-ttu-id="38e18-483">Letra</span><span class="sxs-lookup"><span data-stu-id="38e18-483">Glagolitic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-484">98</span><span class="sxs-lookup"><span data-stu-id="38e18-484">98</span></span></td>
<td><span data-ttu-id="38e18-485">2D30 - 2D7F</span><span class="sxs-lookup"><span data-stu-id="38e18-485">2D30 - 2D7F</span></span></td>
<td><span data-ttu-id="38e18-486">Tifinagh</span><span class="sxs-lookup"><span data-stu-id="38e18-486">Tifinagh</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-487">99</span><span class="sxs-lookup"><span data-stu-id="38e18-487">99</span></span></td>
<td><span data-ttu-id="38e18-488">4DC0 - 4DFF</span><span class="sxs-lookup"><span data-stu-id="38e18-488">4DC0 - 4DFF</span></span></td>
<td><span data-ttu-id="38e18-489">Símbolos de Hexagrama do Yijing</span><span class="sxs-lookup"><span data-stu-id="38e18-489">Yijing Hexagram Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-490">100</span><span class="sxs-lookup"><span data-stu-id="38e18-490">100</span></span></td>
<td><span data-ttu-id="38e18-491">A800 - A82F</span><span class="sxs-lookup"><span data-stu-id="38e18-491">A800 - A82F</span></span></td>
<td><span data-ttu-id="38e18-492">Syloti Nagri</span><span class="sxs-lookup"><span data-stu-id="38e18-492">Syloti Nagri</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="38e18-493">101 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-493">101${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-494">10000-1007F</span><span class="sxs-lookup"><span data-stu-id="38e18-494">10000 - 1007F</span></span></td>
<td><span data-ttu-id="38e18-495">Syllabary linear B</span><span class="sxs-lookup"><span data-stu-id="38e18-495">Linear B Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-496">10080-100FF</span><span class="sxs-lookup"><span data-stu-id="38e18-496">10080 - 100FF</span></span></td>
<td><span data-ttu-id="38e18-497">Ideograms linear B</span><span class="sxs-lookup"><span data-stu-id="38e18-497">Linear B Ideograms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-498">10100-1013F</span><span class="sxs-lookup"><span data-stu-id="38e18-498">10100 - 1013F</span></span></td>
<td><span data-ttu-id="38e18-499">Números de Aegean</span><span class="sxs-lookup"><span data-stu-id="38e18-499">Aegean Numbers</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-500">102</span><span class="sxs-lookup"><span data-stu-id="38e18-500">102</span></span></td>
<td><span data-ttu-id="38e18-501">10140-1018F</span><span class="sxs-lookup"><span data-stu-id="38e18-501">10140 - 1018F</span></span></td>
<td><span data-ttu-id="38e18-502">Números gregos antigo</span><span class="sxs-lookup"><span data-stu-id="38e18-502">Ancient Greek Numbers</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-503">103</span><span class="sxs-lookup"><span data-stu-id="38e18-503">103</span></span></td>
<td><span data-ttu-id="38e18-504">10380-1039F</span><span class="sxs-lookup"><span data-stu-id="38e18-504">10380 - 1039F</span></span></td>
<td><span data-ttu-id="38e18-505">Ugarítico</span><span class="sxs-lookup"><span data-stu-id="38e18-505">Ugaritic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-506">104</span><span class="sxs-lookup"><span data-stu-id="38e18-506">104</span></span></td>
<td><span data-ttu-id="38e18-507">103A0 - 103DF</span><span class="sxs-lookup"><span data-stu-id="38e18-507">103A0 - 103DF</span></span></td>
<td><span data-ttu-id="38e18-508">Persa antigo</span><span class="sxs-lookup"><span data-stu-id="38e18-508">Old Persian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-509">105</span><span class="sxs-lookup"><span data-stu-id="38e18-509">105</span></span></td>
<td><span data-ttu-id="38e18-510">10450-1047F</span><span class="sxs-lookup"><span data-stu-id="38e18-510">10450 - 1047F</span></span></td>
<td><span data-ttu-id="38e18-511">Shavian</span><span class="sxs-lookup"><span data-stu-id="38e18-511">Shavian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-512">106</span><span class="sxs-lookup"><span data-stu-id="38e18-512">106</span></span></td>
<td><span data-ttu-id="38e18-513">10480-104AF</span><span class="sxs-lookup"><span data-stu-id="38e18-513">10480 - 104AF</span></span></td>
<td><span data-ttu-id="38e18-514">Osmanya</span><span class="sxs-lookup"><span data-stu-id="38e18-514">Osmanya</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-515">107</span><span class="sxs-lookup"><span data-stu-id="38e18-515">107</span></span></td>
<td><span data-ttu-id="38e18-516">10800-1083F</span><span class="sxs-lookup"><span data-stu-id="38e18-516">10800 - 1083F</span></span></td>
<td><span data-ttu-id="38e18-517">Cypriot Syllabary</span><span class="sxs-lookup"><span data-stu-id="38e18-517">Cypriot Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-518">108</span><span class="sxs-lookup"><span data-stu-id="38e18-518">108</span></span></td>
<td><span data-ttu-id="38e18-519">10A00 - 10A5F</span><span class="sxs-lookup"><span data-stu-id="38e18-519">10A00 - 10A5F</span></span></td>
<td><span data-ttu-id="38e18-520">Kharoshthi</span><span class="sxs-lookup"><span data-stu-id="38e18-520">Kharoshthi</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-521">109</span><span class="sxs-lookup"><span data-stu-id="38e18-521">109</span></span></td>
<td><span data-ttu-id="38e18-522">1D300 - 1D35F</span><span class="sxs-lookup"><span data-stu-id="38e18-522">1D300 - 1D35F</span></span></td>
<td><span data-ttu-id="38e18-523">Símbolos Jing de Xuan Tai</span><span class="sxs-lookup"><span data-stu-id="38e18-523">Tai Xuan Jing Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="38e18-524">110 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-524">110${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-525">12000-123FF</span><span class="sxs-lookup"><span data-stu-id="38e18-525">12000 - 123FF</span></span></td>
<td><span data-ttu-id="38e18-526">Cuneiform</span><span class="sxs-lookup"><span data-stu-id="38e18-526">Cuneiform</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-527">12400-1247F</span><span class="sxs-lookup"><span data-stu-id="38e18-527">12400 - 1247F</span></span></td>
<td><span data-ttu-id="38e18-528">Cuneiform números e Pontuação</span><span class="sxs-lookup"><span data-stu-id="38e18-528">Cuneiform Numbers and Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-529">111</span><span class="sxs-lookup"><span data-stu-id="38e18-529">111</span></span></td>
<td><span data-ttu-id="38e18-530">1D360 - 1D37F</span><span class="sxs-lookup"><span data-stu-id="38e18-530">1D360 - 1D37F</span></span></td>
<td><span data-ttu-id="38e18-531">Numeração de metros de contagem</span><span class="sxs-lookup"><span data-stu-id="38e18-531">Counting Rod Numerals</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-532">112</span><span class="sxs-lookup"><span data-stu-id="38e18-532">112</span></span></td>
<td><span data-ttu-id="38e18-533">1B80 - 1BBF</span><span class="sxs-lookup"><span data-stu-id="38e18-533">1B80 - 1BBF</span></span></td>
<td><span data-ttu-id="38e18-534">Sundanês</span><span class="sxs-lookup"><span data-stu-id="38e18-534">Sundanese</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-535">113</span><span class="sxs-lookup"><span data-stu-id="38e18-535">113</span></span></td>
<td><span data-ttu-id="38e18-536">1C00 - 1C4F</span><span class="sxs-lookup"><span data-stu-id="38e18-536">1C00 - 1C4F</span></span></td>
<td><span data-ttu-id="38e18-537">Lepcha</span><span class="sxs-lookup"><span data-stu-id="38e18-537">Lepcha</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-538">114</span><span class="sxs-lookup"><span data-stu-id="38e18-538">114</span></span></td>
<td><span data-ttu-id="38e18-539">1C50 - 1C7F</span><span class="sxs-lookup"><span data-stu-id="38e18-539">1C50 - 1C7F</span></span></td>
<td><span data-ttu-id="38e18-540">Ol Chiki</span><span class="sxs-lookup"><span data-stu-id="38e18-540">Ol Chiki</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-541">115</span><span class="sxs-lookup"><span data-stu-id="38e18-541">115</span></span></td>
<td><span data-ttu-id="38e18-542">A880 - A8DF</span><span class="sxs-lookup"><span data-stu-id="38e18-542">A880 - A8DF</span></span></td>
<td><span data-ttu-id="38e18-543">Saurashtra</span><span class="sxs-lookup"><span data-stu-id="38e18-543">Saurashtra</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-544">116</span><span class="sxs-lookup"><span data-stu-id="38e18-544">116</span></span></td>
<td><span data-ttu-id="38e18-545">A900 - A92F</span><span class="sxs-lookup"><span data-stu-id="38e18-545">A900 - A92F</span></span></td>
<td><span data-ttu-id="38e18-546">Kayah Li</span><span class="sxs-lookup"><span data-stu-id="38e18-546">Kayah Li</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-547">117</span><span class="sxs-lookup"><span data-stu-id="38e18-547">117</span></span></td>
<td><span data-ttu-id="38e18-548">A930 - A95F</span><span class="sxs-lookup"><span data-stu-id="38e18-548">A930 - A95F</span></span></td>
<td><span data-ttu-id="38e18-549">Rejang</span><span class="sxs-lookup"><span data-stu-id="38e18-549">Rejang</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-550">118</span><span class="sxs-lookup"><span data-stu-id="38e18-550">118</span></span></td>
<td><span data-ttu-id="38e18-551">AA00 - AA5F</span><span class="sxs-lookup"><span data-stu-id="38e18-551">AA00 - AA5F</span></span></td>
<td><span data-ttu-id="38e18-552">Cham</span><span class="sxs-lookup"><span data-stu-id="38e18-552">Cham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-553">119</span><span class="sxs-lookup"><span data-stu-id="38e18-553">119</span></span></td>
<td><span data-ttu-id="38e18-554">10190-101CF</span><span class="sxs-lookup"><span data-stu-id="38e18-554">10190 - 101CF</span></span></td>
<td><span data-ttu-id="38e18-555">Símbolos antigo</span><span class="sxs-lookup"><span data-stu-id="38e18-555">Ancient Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-556">120</span><span class="sxs-lookup"><span data-stu-id="38e18-556">120</span></span></td>
<td><span data-ttu-id="38e18-557">101D0 - 101FF</span><span class="sxs-lookup"><span data-stu-id="38e18-557">101D0 - 101FF</span></span></td>
<td><span data-ttu-id="38e18-558">Disco Phaistos</span><span class="sxs-lookup"><span data-stu-id="38e18-558">Phaistos Disc</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="38e18-559">121 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-559">121${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-560">10280-1029F</span><span class="sxs-lookup"><span data-stu-id="38e18-560">10280 - 1029F</span></span></td>
<td><span data-ttu-id="38e18-561">Lício</span><span class="sxs-lookup"><span data-stu-id="38e18-561">Lycian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-562">102A0 - 102DF</span><span class="sxs-lookup"><span data-stu-id="38e18-562">102A0 - 102DF</span></span></td>
<td><span data-ttu-id="38e18-563">Cariano</span><span class="sxs-lookup"><span data-stu-id="38e18-563">Carian</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-564">10920-1093F</span><span class="sxs-lookup"><span data-stu-id="38e18-564">10920 - 1093F</span></span></td>
<td><span data-ttu-id="38e18-565">Lídio</span><span class="sxs-lookup"><span data-stu-id="38e18-565">Lydian</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="38e18-566">122 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="38e18-566">122${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="38e18-567">1F000 - 1F02F</span><span class="sxs-lookup"><span data-stu-id="38e18-567">1F000 - 1F02F</span></span></td>
<td><span data-ttu-id="38e18-568">Blocos do mahjong</span><span class="sxs-lookup"><span data-stu-id="38e18-568">Mahjong Tiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-569">1F030 - 1F09F</span><span class="sxs-lookup"><span data-stu-id="38e18-569">1F030 - 1F09F</span></span></td>
<td><span data-ttu-id="38e18-570">Blocos do Domino</span><span class="sxs-lookup"><span data-stu-id="38e18-570">Domino Tiles</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38e18-571">123</span><span class="sxs-lookup"><span data-stu-id="38e18-571">123</span></span></td>

<td><span data-ttu-id="38e18-572"><strong>Windows 2000 e posterior:</strong> Progresso do layout, horizontal da direita para a esquerda</span><span class="sxs-lookup"><span data-stu-id="38e18-572"><strong>Windows 2000 and later:</strong> Layout progress, horizontal from right to left</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-573">124</span><span class="sxs-lookup"><span data-stu-id="38e18-573">124</span></span></td>

<td><span data-ttu-id="38e18-574"><strong>Windows 2000 e posterior:</strong> Progresso do layout, vertical antes da horizontal</span><span class="sxs-lookup"><span data-stu-id="38e18-574"><strong>Windows 2000 and later:</strong> Layout progress, vertical before horizontal</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38e18-575">125</span><span class="sxs-lookup"><span data-stu-id="38e18-575">125</span></span></td>

<td><span data-ttu-id="38e18-576"><strong>Windows 2000 e posterior:</strong> Progresso do layout, vertical inferior ao início</span><span class="sxs-lookup"><span data-stu-id="38e18-576"><strong>Windows 2000 and later:</strong> Layout progress, vertical bottom to top</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38e18-577">126-127</span><span class="sxs-lookup"><span data-stu-id="38e18-577">126-127</span></span></td>

<td><span data-ttu-id="38e18-578">Reservado para o uso interno de processo</span><span class="sxs-lookup"><span data-stu-id="38e18-578">Reserved for process-internal usage</span></span></td>
</tr>
</tbody>
</table>



 

 

 



