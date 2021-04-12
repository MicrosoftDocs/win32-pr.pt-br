---
description: Para obter informações sobre atributos de controle, consulte o link para o controle específico que você precisa criar em controles, bem como os links para determinados atributos de controle nas listas a seguir.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Atributos de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d026e84dadefa67ce9d6e00146c6e1c2017cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297207"
---
# <a name="control-attributes"></a><span data-ttu-id="1b217-103">Atributos de controle</span><span class="sxs-lookup"><span data-stu-id="1b217-103">Control Attributes</span></span>

<span data-ttu-id="1b217-104">Para obter informações sobre atributos de controle, consulte o link para o controle específico que você precisa criar em [controles](controls.md) , bem como os links para determinados atributos de controle nas listas a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b217-104">For information on control attributes, see the link to the particular control that you need to create in [Controls](controls.md) as well as the links to particular control attributes in the following lists.</span></span>

<span data-ttu-id="1b217-105">Os métodos a seguir são usados para especificar os atributos de um controle:</span><span class="sxs-lookup"><span data-stu-id="1b217-105">The following methods are used for specifying the attributes of a control:</span></span>

-   <span data-ttu-id="1b217-106">Use a [tabela ControlCondition](controlcondition-table.md) para desabilitar, habilitar, ocultar ou mostrar um controle de acordo com o valor de uma propriedade ou instrução condicional.</span><span class="sxs-lookup"><span data-stu-id="1b217-106">Use the [ControlCondition table](controlcondition-table.md) to disable, enable, hide, or show a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="1b217-107">Você também pode usar essa tabela para substituir o controle padrão especificado na [tabela de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="1b217-107">You can also use this table to override the default control specified in the [Dialog table](dialog-table.md).</span></span>
-   <span data-ttu-id="1b217-108">Assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="1b217-108">Subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="1b217-109">Insira o identificador do atributo na coluna de atributo e o identificador do ControlEvent, na coluna evento desta tabela.</span><span class="sxs-lookup"><span data-stu-id="1b217-109">Enter the attribute's identifier in the Attribute column and the ControlEvent's identifier in the Event column of this table.</span></span>
-   <span data-ttu-id="1b217-110">Defina os sinalizadores de bit de atributo de controle para o controle na coluna atributo da [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="1b217-110">Set the control attribute bit flags for the control in the Attribute column of the [Control table](control-table.md).</span></span> <span data-ttu-id="1b217-111">Isso define os atributos na criação do controle.</span><span class="sxs-lookup"><span data-stu-id="1b217-111">This sets the attributes upon the creation of the control.</span></span>

<span data-ttu-id="1b217-112">Alguns atributos não podem ser definidos para cada controle ou ser especificados por todos os métodos acima.</span><span class="sxs-lookup"><span data-stu-id="1b217-112">Some attributes cannot be set for every control or be specified by all of the above methods.</span></span> <span data-ttu-id="1b217-113">Consulte os tópicos de controle e atributo específicos para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="1b217-113">See the particular control and attribute topics for details.</span></span>

<span data-ttu-id="1b217-114">Os valores iniciais de alguns atributos de controle podem ser definidos com bits na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="1b217-114">The initial values of some control attributes can be set with bits in the [Control table](control-table.md).</span></span>



| <span data-ttu-id="1b217-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b217-115">Attribute</span></span>                                          | <span data-ttu-id="1b217-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="1b217-116">Decimal</span></span> | <span data-ttu-id="1b217-117">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1b217-117">Hexadecimal</span></span> | <span data-ttu-id="1b217-118">Constante</span><span class="sxs-lookup"><span data-stu-id="1b217-118">Constant</span></span>                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [<span data-ttu-id="1b217-119">BiDi</span><span class="sxs-lookup"><span data-stu-id="1b217-119">BiDi</span></span>](bidi-control-attribute.md)                 | <span data-ttu-id="1b217-120">224</span><span class="sxs-lookup"><span data-stu-id="1b217-120">224</span></span>     | <span data-ttu-id="1b217-121">0x000000E0</span><span class="sxs-lookup"><span data-stu-id="1b217-121">0x000000E0</span></span>  | <span data-ttu-id="1b217-122">**msidbControlAttributesBiDi**</span><span class="sxs-lookup"><span data-stu-id="1b217-122">**msidbControlAttributesBiDi**</span></span>         |
| [<span data-ttu-id="1b217-123">Enabled</span><span class="sxs-lookup"><span data-stu-id="1b217-123">Enabled</span></span>](enabled-control-attribute.md)           | <span data-ttu-id="1b217-124">2</span><span class="sxs-lookup"><span data-stu-id="1b217-124">2</span></span>       | <span data-ttu-id="1b217-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1b217-125">0x00000002</span></span>  | <span data-ttu-id="1b217-126">**msidbControlAttributesEnabled**</span><span class="sxs-lookup"><span data-stu-id="1b217-126">**msidbControlAttributesEnabled**</span></span>      |
| [<span data-ttu-id="1b217-127">Indireto.</span><span class="sxs-lookup"><span data-stu-id="1b217-127">Indirect</span></span>](indirect-control-attribute.md)         | <span data-ttu-id="1b217-128">8</span><span class="sxs-lookup"><span data-stu-id="1b217-128">8</span></span>       | <span data-ttu-id="1b217-129">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1b217-129">0x00000008</span></span>  | <span data-ttu-id="1b217-130">**msidbControlAttributesIndirect**</span><span class="sxs-lookup"><span data-stu-id="1b217-130">**msidbControlAttributesIndirect**</span></span>     |
| [<span data-ttu-id="1b217-131">Controle de inteiro</span><span class="sxs-lookup"><span data-stu-id="1b217-131">Integer Control</span></span>](integer-control-attribute.md)   | <span data-ttu-id="1b217-132">16</span><span class="sxs-lookup"><span data-stu-id="1b217-132">16</span></span>      | <span data-ttu-id="1b217-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b217-133">0x00000010</span></span>  | <span data-ttu-id="1b217-134">**msidbControlAttributesInteger**</span><span class="sxs-lookup"><span data-stu-id="1b217-134">**msidbControlAttributesInteger**</span></span>      |
| [<span data-ttu-id="1b217-135">LeftScroll</span><span class="sxs-lookup"><span data-stu-id="1b217-135">LeftScroll</span></span>](leftscroll-control-attribute.md)     | <span data-ttu-id="1b217-136">128</span><span class="sxs-lookup"><span data-stu-id="1b217-136">128</span></span>     | <span data-ttu-id="1b217-137">0x00000080</span><span class="sxs-lookup"><span data-stu-id="1b217-137">0x00000080</span></span>  | <span data-ttu-id="1b217-138">**msidbControlAttributesLeftScroll**</span><span class="sxs-lookup"><span data-stu-id="1b217-138">**msidbControlAttributesLeftScroll**</span></span>   |
| [<span data-ttu-id="1b217-139">RightAligned</span><span class="sxs-lookup"><span data-stu-id="1b217-139">RightAligned</span></span>](rightaligned-control-attribute.md) | <span data-ttu-id="1b217-140">64</span><span class="sxs-lookup"><span data-stu-id="1b217-140">64</span></span>      | <span data-ttu-id="1b217-141">0x00000040</span><span class="sxs-lookup"><span data-stu-id="1b217-141">0x00000040</span></span>  | <span data-ttu-id="1b217-142">**msidbControlAttributesRightAligned**</span><span class="sxs-lookup"><span data-stu-id="1b217-142">**msidbControlAttributesRightAligned**</span></span> |
| [<span data-ttu-id="1b217-143">RTLRO</span><span class="sxs-lookup"><span data-stu-id="1b217-143">RTLRO</span></span>](rtlro-control-attribute.md)               | <span data-ttu-id="1b217-144">32</span><span class="sxs-lookup"><span data-stu-id="1b217-144">32</span></span>      | <span data-ttu-id="1b217-145">0x00000020</span><span class="sxs-lookup"><span data-stu-id="1b217-145">0x00000020</span></span>  | <span data-ttu-id="1b217-146">**msidbControlAttributesRTLRO**</span><span class="sxs-lookup"><span data-stu-id="1b217-146">**msidbControlAttributesRTLRO**</span></span>        |
| [<span data-ttu-id="1b217-147">Submersa</span><span class="sxs-lookup"><span data-stu-id="1b217-147">Sunken</span></span>](sunken-control-attribute.md)             | <span data-ttu-id="1b217-148">4</span><span class="sxs-lookup"><span data-stu-id="1b217-148">4</span></span>       | <span data-ttu-id="1b217-149">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1b217-149">0x00000004</span></span>  | <span data-ttu-id="1b217-150">**msidbControlAttributesSunken**</span><span class="sxs-lookup"><span data-stu-id="1b217-150">**msidbControlAttributesSunken**</span></span>       |
| [<span data-ttu-id="1b217-151">Visível</span><span class="sxs-lookup"><span data-stu-id="1b217-151">Visible</span></span>](visible-control-attribute.md)           | <span data-ttu-id="1b217-152">1</span><span class="sxs-lookup"><span data-stu-id="1b217-152">1</span></span>       | <span data-ttu-id="1b217-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1b217-153">0x00000001</span></span>  | <span data-ttu-id="1b217-154">**msidbControlAttributesVisible**</span><span class="sxs-lookup"><span data-stu-id="1b217-154">**msidbControlAttributesVisible**</span></span>      |



 

<span data-ttu-id="1b217-155">Esses atributos de controles de texto são definidos com bits.</span><span class="sxs-lookup"><span data-stu-id="1b217-155">These attributes of Text controls are set with bits.</span></span>



| <span data-ttu-id="1b217-156">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b217-156">Attribute</span></span>                                            | <span data-ttu-id="1b217-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="1b217-157">Decimal</span></span> | <span data-ttu-id="1b217-158">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1b217-158">Hexadecimal</span></span> | <span data-ttu-id="1b217-159">Constante</span><span class="sxs-lookup"><span data-stu-id="1b217-159">Constant</span></span>                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [<span data-ttu-id="1b217-160">Formatar</span><span class="sxs-lookup"><span data-stu-id="1b217-160">FormatSize</span></span>](formatsize-control-attribute.md)       | <span data-ttu-id="1b217-161">524288</span><span class="sxs-lookup"><span data-stu-id="1b217-161">524288</span></span>  | <span data-ttu-id="1b217-162">0x00080000</span><span class="sxs-lookup"><span data-stu-id="1b217-162">0x00080000</span></span>  | <span data-ttu-id="1b217-163">**msidbControlAttributesFormatSize**</span><span class="sxs-lookup"><span data-stu-id="1b217-163">**msidbControlAttributesFormatSize**</span></span>    |
| [<span data-ttu-id="1b217-164">NoPrefix</span><span class="sxs-lookup"><span data-stu-id="1b217-164">NoPrefix</span></span>](noprefix-control-attribute.md)           | <span data-ttu-id="1b217-165">131072</span><span class="sxs-lookup"><span data-stu-id="1b217-165">131072</span></span>  | <span data-ttu-id="1b217-166">0x00020000</span><span class="sxs-lookup"><span data-stu-id="1b217-166">0x00020000</span></span>  | <span data-ttu-id="1b217-167">**msidbControlAttributesNoPrefix**</span><span class="sxs-lookup"><span data-stu-id="1b217-167">**msidbControlAttributesNoPrefix**</span></span>      |
| [<span data-ttu-id="1b217-168">Desencapsular</span><span class="sxs-lookup"><span data-stu-id="1b217-168">NoWrap</span></span>](nowrap-control-attribute.md)               | <span data-ttu-id="1b217-169">262144</span><span class="sxs-lookup"><span data-stu-id="1b217-169">262144</span></span>  | <span data-ttu-id="1b217-170">0x00040000</span><span class="sxs-lookup"><span data-stu-id="1b217-170">0x00040000</span></span>  | <span data-ttu-id="1b217-171">**msidbControlAttributesNoWrap**</span><span class="sxs-lookup"><span data-stu-id="1b217-171">**msidbControlAttributesNoWrap**</span></span>        |
| [<span data-ttu-id="1b217-172">Senha</span><span class="sxs-lookup"><span data-stu-id="1b217-172">Password</span></span>](password-control-attribute.md)           | <span data-ttu-id="1b217-173">2097152</span><span class="sxs-lookup"><span data-stu-id="1b217-173">2097152</span></span> | <span data-ttu-id="1b217-174">0x00200000</span><span class="sxs-lookup"><span data-stu-id="1b217-174">0x00200000</span></span>  | <span data-ttu-id="1b217-175">**msidbControlAttributesPasswordInput**</span><span class="sxs-lookup"><span data-stu-id="1b217-175">**msidbControlAttributesPasswordInput**</span></span> |
| [<span data-ttu-id="1b217-176">Transparente</span><span class="sxs-lookup"><span data-stu-id="1b217-176">Transparent</span></span>](transparent-control-attribute.md)     | <span data-ttu-id="1b217-177">65536</span><span class="sxs-lookup"><span data-stu-id="1b217-177">65536</span></span>   | <span data-ttu-id="1b217-178">0x00010000</span><span class="sxs-lookup"><span data-stu-id="1b217-178">0x00010000</span></span>  | <span data-ttu-id="1b217-179">**msidbControlAttributesTransparent**</span><span class="sxs-lookup"><span data-stu-id="1b217-179">**msidbControlAttributesTransparent**</span></span>   |
| [<span data-ttu-id="1b217-180">UsersLanguage</span><span class="sxs-lookup"><span data-stu-id="1b217-180">UsersLanguage</span></span>](userslanguage-control-attribute.md) | <span data-ttu-id="1b217-181">1048576</span><span class="sxs-lookup"><span data-stu-id="1b217-181">1048576</span></span> | <span data-ttu-id="1b217-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="1b217-182">0x00100000</span></span>  | <span data-ttu-id="1b217-183">**msidbControlAttributesUsersLanguage**</span><span class="sxs-lookup"><span data-stu-id="1b217-183">**msidbControlAttributesUsersLanguage**</span></span> |



 

<span data-ttu-id="1b217-184">Esse atributo do controle ProgressBar é definido com um bit.</span><span class="sxs-lookup"><span data-stu-id="1b217-184">This attribute of the ProgressBar control is set with a bit.</span></span>



| <span data-ttu-id="1b217-185">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b217-185">Attribute</span></span>                                      | <span data-ttu-id="1b217-186">Decimal</span><span class="sxs-lookup"><span data-stu-id="1b217-186">Decimal</span></span> | <span data-ttu-id="1b217-187">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1b217-187">Hexadecimal</span></span> | <span data-ttu-id="1b217-188">Constante</span><span class="sxs-lookup"><span data-stu-id="1b217-188">Constant</span></span>                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="1b217-189">Progress95</span><span class="sxs-lookup"><span data-stu-id="1b217-189">Progress95</span></span>](progress95-control-attribute.md) | <span data-ttu-id="1b217-190">65536</span><span class="sxs-lookup"><span data-stu-id="1b217-190">65536</span></span>   | <span data-ttu-id="1b217-191">0x00010000</span><span class="sxs-lookup"><span data-stu-id="1b217-191">0x00010000</span></span>  | <span data-ttu-id="1b217-192">**msidbControlAttributesProgress95**</span><span class="sxs-lookup"><span data-stu-id="1b217-192">**msidbControlAttributesProgress95**</span></span> |



 

<span data-ttu-id="1b217-193">Esses atributos dos controles SelectCombo de volume e de diretório são definidos com bits.</span><span class="sxs-lookup"><span data-stu-id="1b217-193">These attributes of Volume and Directory SelectCombo controls are set with bits.</span></span>



| <span data-ttu-id="1b217-194">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b217-194">Attribute</span></span>                                                | <span data-ttu-id="1b217-195">Decimal</span><span class="sxs-lookup"><span data-stu-id="1b217-195">Decimal</span></span> | <span data-ttu-id="1b217-196">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1b217-196">Hexadecimal</span></span> | <span data-ttu-id="1b217-197">Constante</span><span class="sxs-lookup"><span data-stu-id="1b217-197">Constant</span></span>                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="1b217-198">CDROMVolume</span><span class="sxs-lookup"><span data-stu-id="1b217-198">CDROMVolume</span></span>](cdromvolume-control-attribute.md)         | <span data-ttu-id="1b217-199">524288</span><span class="sxs-lookup"><span data-stu-id="1b217-199">524288</span></span>  | <span data-ttu-id="1b217-200">0x00080000</span><span class="sxs-lookup"><span data-stu-id="1b217-200">0x00080000</span></span>  | <span data-ttu-id="1b217-201">**msidbControlAttributesCDROMVolume**</span><span class="sxs-lookup"><span data-stu-id="1b217-201">**msidbControlAttributesCDROMVolume**</span></span>     |
| [<span data-ttu-id="1b217-202">FixedVolume</span><span class="sxs-lookup"><span data-stu-id="1b217-202">FixedVolume</span></span>](fixedvolume-control-attribute.md)         | <span data-ttu-id="1b217-203">131072</span><span class="sxs-lookup"><span data-stu-id="1b217-203">131072</span></span>  | <span data-ttu-id="1b217-204">0x00020000</span><span class="sxs-lookup"><span data-stu-id="1b217-204">0x00020000</span></span>  | <span data-ttu-id="1b217-205">**msidbControlAttributesFixedVolume**</span><span class="sxs-lookup"><span data-stu-id="1b217-205">**msidbControlAttributesFixedVolume**</span></span>     |
| [<span data-ttu-id="1b217-206">FloppyVolume</span><span class="sxs-lookup"><span data-stu-id="1b217-206">FloppyVolume</span></span>](floppyvolume-control-attribute.md)       | <span data-ttu-id="1b217-207">2097152</span><span class="sxs-lookup"><span data-stu-id="1b217-207">2097152</span></span> | <span data-ttu-id="1b217-208">0x00200000</span><span class="sxs-lookup"><span data-stu-id="1b217-208">0x00200000</span></span>  | <span data-ttu-id="1b217-209">**msidbControlAttributesFloppyVolume**</span><span class="sxs-lookup"><span data-stu-id="1b217-209">**msidbControlAttributesFloppyVolume**</span></span>    |
| [<span data-ttu-id="1b217-210">RAMDiskVolume</span><span class="sxs-lookup"><span data-stu-id="1b217-210">RAMDiskVolume</span></span>](ramdiskvolume-control-attribute.md)     | <span data-ttu-id="1b217-211">1048576</span><span class="sxs-lookup"><span data-stu-id="1b217-211">1048576</span></span> | <span data-ttu-id="1b217-212">0x00100000</span><span class="sxs-lookup"><span data-stu-id="1b217-212">0x00100000</span></span>  | <span data-ttu-id="1b217-213">**msidbControlAttributesRAMDiskVolume**</span><span class="sxs-lookup"><span data-stu-id="1b217-213">**msidbControlAttributesRAMDiskVolume**</span></span>   |
| [<span data-ttu-id="1b217-214">RemoteVolume</span><span class="sxs-lookup"><span data-stu-id="1b217-214">RemoteVolume</span></span>](remotevolume-control-attribute.md)       | <span data-ttu-id="1b217-215">262144</span><span class="sxs-lookup"><span data-stu-id="1b217-215">262144</span></span>  | <span data-ttu-id="1b217-216">0x00040000</span><span class="sxs-lookup"><span data-stu-id="1b217-216">0x00040000</span></span>  | <span data-ttu-id="1b217-217">**msidbControlAttributesRemoteVolume**</span><span class="sxs-lookup"><span data-stu-id="1b217-217">**msidbControlAttributesRemoteVolume**</span></span>    |
| [<span data-ttu-id="1b217-218">RemovableVolume</span><span class="sxs-lookup"><span data-stu-id="1b217-218">RemovableVolume</span></span>](removablevolume-control-attribute.md) | <span data-ttu-id="1b217-219">65536</span><span class="sxs-lookup"><span data-stu-id="1b217-219">65536</span></span>   | <span data-ttu-id="1b217-220">0x00010000</span><span class="sxs-lookup"><span data-stu-id="1b217-220">0x00010000</span></span>  | <span data-ttu-id="1b217-221">**msidbControlAttributesRemovableVolume**</span><span class="sxs-lookup"><span data-stu-id="1b217-221">**msidbControlAttributesRemovableVolume**</span></span> |



 

<span data-ttu-id="1b217-222">Esses atributos dos controles ListBox e ComboBox são definidos com bits.</span><span class="sxs-lookup"><span data-stu-id="1b217-222">These attributes of ListBox and ComboBox controls are set with bits.</span></span>



| <span data-ttu-id="1b217-223">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b217-223">Attribute</span></span>                                            | <span data-ttu-id="1b217-224">Decimal</span><span class="sxs-lookup"><span data-stu-id="1b217-224">Decimal</span></span> | <span data-ttu-id="1b217-225">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1b217-225">Hexadecimal</span></span> | <span data-ttu-id="1b217-226">Constante</span><span class="sxs-lookup"><span data-stu-id="1b217-226">Constant</span></span>                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="1b217-227">Controle de combinação de combinações</span><span class="sxs-lookup"><span data-stu-id="1b217-227">ComboList Control</span></span>](combolist-control-attribute.md) | <span data-ttu-id="1b217-228">131072</span><span class="sxs-lookup"><span data-stu-id="1b217-228">131072</span></span>  | <span data-ttu-id="1b217-229">0x00020000</span><span class="sxs-lookup"><span data-stu-id="1b217-229">0x00020000</span></span>  | <span data-ttu-id="1b217-230">**msidbControlAttributesComboList**</span><span class="sxs-lookup"><span data-stu-id="1b217-230">**msidbControlAttributesComboList**</span></span> |
| [<span data-ttu-id="1b217-231">Controle classificado</span><span class="sxs-lookup"><span data-stu-id="1b217-231">Sorted Control</span></span>](sorted-control-attribute.md)       | <span data-ttu-id="1b217-232">65536</span><span class="sxs-lookup"><span data-stu-id="1b217-232">65536</span></span>   | <span data-ttu-id="1b217-233">0x00010000</span><span class="sxs-lookup"><span data-stu-id="1b217-233">0x00010000</span></span>  | <span data-ttu-id="1b217-234">**msidbControlAttributesSorted**</span><span class="sxs-lookup"><span data-stu-id="1b217-234">**msidbControlAttributesSorted**</span></span>    |



 

<span data-ttu-id="1b217-235">Esse atributo do controle de edição é definido com um bit.</span><span class="sxs-lookup"><span data-stu-id="1b217-235">This attribute of the Edit control is set with a bit.</span></span>



| <span data-ttu-id="1b217-236">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b217-236">Attribute</span></span>                                    | <span data-ttu-id="1b217-237">Decimal</span><span class="sxs-lookup"><span data-stu-id="1b217-237">Decimal</span></span> | <span data-ttu-id="1b217-238">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1b217-238">Hexadecimal</span></span> | <span data-ttu-id="1b217-239">Constante</span><span class="sxs-lookup"><span data-stu-id="1b217-239">Constant</span></span>                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="1b217-240">Tiverem</span><span class="sxs-lookup"><span data-stu-id="1b217-240">MultiLine</span></span>](multiline-control-attribute.md) | <span data-ttu-id="1b217-241">65536</span><span class="sxs-lookup"><span data-stu-id="1b217-241">65536</span></span>   | <span data-ttu-id="1b217-242">0x00010000</span><span class="sxs-lookup"><span data-stu-id="1b217-242">0x00010000</span></span>  | <span data-ttu-id="1b217-243">**msidbControlAttributesMultiline**</span><span class="sxs-lookup"><span data-stu-id="1b217-243">**msidbControlAttributesMultiline**</span></span> |



 

<span data-ttu-id="1b217-244">Esses atributos de controles PictureButton são definidos com bits.</span><span class="sxs-lookup"><span data-stu-id="1b217-244">These attributes of PictureButton controls are set with bits.</span></span>



| <span data-ttu-id="1b217-245">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b217-245">Attribute</span></span>                                          | <span data-ttu-id="1b217-246">Decimal</span><span class="sxs-lookup"><span data-stu-id="1b217-246">Decimal</span></span> | <span data-ttu-id="1b217-247">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1b217-247">Hexadecimal</span></span> | <span data-ttu-id="1b217-248">Constante</span><span class="sxs-lookup"><span data-stu-id="1b217-248">Constant</span></span>                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="1b217-249">Bitmap</span><span class="sxs-lookup"><span data-stu-id="1b217-249">Bitmap</span></span>](bitmap-control-attribute.md)             | <span data-ttu-id="1b217-250">262144</span><span class="sxs-lookup"><span data-stu-id="1b217-250">262144</span></span>  | <span data-ttu-id="1b217-251">0x00040000</span><span class="sxs-lookup"><span data-stu-id="1b217-251">0x00040000</span></span>  | <span data-ttu-id="1b217-252">**msidbControlAttributesBitmap**</span><span class="sxs-lookup"><span data-stu-id="1b217-252">**msidbControlAttributesBitmap**</span></span>     |
| [<span data-ttu-id="1b217-253">FixedSize</span><span class="sxs-lookup"><span data-stu-id="1b217-253">FixedSize</span></span>](fixedsize-control-attribute.md)       | <span data-ttu-id="1b217-254">1048576</span><span class="sxs-lookup"><span data-stu-id="1b217-254">1048576</span></span> | <span data-ttu-id="1b217-255">0x00100000</span><span class="sxs-lookup"><span data-stu-id="1b217-255">0x00100000</span></span>  | <span data-ttu-id="1b217-256">**msidbControlAttributesFixedSize**</span><span class="sxs-lookup"><span data-stu-id="1b217-256">**msidbControlAttributesFixedSize**</span></span>  |
| [<span data-ttu-id="1b217-257">Ícone</span><span class="sxs-lookup"><span data-stu-id="1b217-257">Icon</span></span>](icon-control-attribute.md)                 | <span data-ttu-id="1b217-258">524288</span><span class="sxs-lookup"><span data-stu-id="1b217-258">524288</span></span>  | <span data-ttu-id="1b217-259">0x00080000</span><span class="sxs-lookup"><span data-stu-id="1b217-259">0x00080000</span></span>  | <span data-ttu-id="1b217-260">**msidbControlAttributesIcon**</span><span class="sxs-lookup"><span data-stu-id="1b217-260">**msidbControlAttributesIcon**</span></span>       |
| [<span data-ttu-id="1b217-261">IconSize16</span><span class="sxs-lookup"><span data-stu-id="1b217-261">IconSize16</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="1b217-262">2097152</span><span class="sxs-lookup"><span data-stu-id="1b217-262">2097152</span></span> | <span data-ttu-id="1b217-263">0x00200000</span><span class="sxs-lookup"><span data-stu-id="1b217-263">0x00200000</span></span>  | <span data-ttu-id="1b217-264">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="1b217-264">**msidbControlAttributesIconSize16**</span></span> |
| [<span data-ttu-id="1b217-265">IconSize32</span><span class="sxs-lookup"><span data-stu-id="1b217-265">IconSize32</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="1b217-266">4194304</span><span class="sxs-lookup"><span data-stu-id="1b217-266">4194304</span></span> | <span data-ttu-id="1b217-267">0x00400000</span><span class="sxs-lookup"><span data-stu-id="1b217-267">0x00400000</span></span>  | <span data-ttu-id="1b217-268">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="1b217-268">**msidbControlAttributesIconSize32**</span></span> |
| [<span data-ttu-id="1b217-269">IconSize48</span><span class="sxs-lookup"><span data-stu-id="1b217-269">IconSize48</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="1b217-270">6291456</span><span class="sxs-lookup"><span data-stu-id="1b217-270">6291456</span></span> | <span data-ttu-id="1b217-271">0x00600000</span><span class="sxs-lookup"><span data-stu-id="1b217-271">0x00600000</span></span>  | <span data-ttu-id="1b217-272">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="1b217-272">**msidbControlAttributesIconSize48**</span></span> |
| [<span data-ttu-id="1b217-273">Controle PushLike</span><span class="sxs-lookup"><span data-stu-id="1b217-273">PushLike Control</span></span>](pushlike-control-attribute.md) | <span data-ttu-id="1b217-274">131072</span><span class="sxs-lookup"><span data-stu-id="1b217-274">131072</span></span>  | <span data-ttu-id="1b217-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="1b217-275">0x00020000</span></span>  | <span data-ttu-id="1b217-276">**msidbControlAttributesPushLike**</span><span class="sxs-lookup"><span data-stu-id="1b217-276">**msidbControlAttributesPushLike**</span></span>   |



 

<span data-ttu-id="1b217-277">Esse atributo do controle RadioButton é definido com um bit.</span><span class="sxs-lookup"><span data-stu-id="1b217-277">This attribute of RadioButton control is set with a bit.</span></span>



| <span data-ttu-id="1b217-278">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b217-278">Attribute</span></span>                                    | <span data-ttu-id="1b217-279">Decimal</span><span class="sxs-lookup"><span data-stu-id="1b217-279">Decimal</span></span>  | <span data-ttu-id="1b217-280">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1b217-280">Hexadecimal</span></span> | <span data-ttu-id="1b217-281">Constante</span><span class="sxs-lookup"><span data-stu-id="1b217-281">Constant</span></span>                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [<span data-ttu-id="1b217-282">HasBorder</span><span class="sxs-lookup"><span data-stu-id="1b217-282">HasBorder</span></span>](hasborder-control-attribute.md) | <span data-ttu-id="1b217-283">16777216</span><span class="sxs-lookup"><span data-stu-id="1b217-283">16777216</span></span> | <span data-ttu-id="1b217-284">0x01000000</span><span class="sxs-lookup"><span data-stu-id="1b217-284">0x01000000</span></span>  | <span data-ttu-id="1b217-285">**msidbControlAttributesHasBorder**</span><span class="sxs-lookup"><span data-stu-id="1b217-285">**msidbControlAttributesHasBorder**</span></span> |



 

<span data-ttu-id="1b217-286">Esse atributo de controle de supressão é definido com um bit.</span><span class="sxs-lookup"><span data-stu-id="1b217-286">This attribute of PushButton control is set with a bit.</span></span>



| <span data-ttu-id="1b217-287">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b217-287">Attribute</span></span>                                        | <span data-ttu-id="1b217-288">Decimal</span><span class="sxs-lookup"><span data-stu-id="1b217-288">Decimal</span></span> | <span data-ttu-id="1b217-289">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1b217-289">Hexadecimal</span></span> | <span data-ttu-id="1b217-290">Constante</span><span class="sxs-lookup"><span data-stu-id="1b217-290">Constant</span></span>                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="1b217-291">ElevationShield</span><span class="sxs-lookup"><span data-stu-id="1b217-291">ElevationShield</span></span>](elevationshield-attribute.md) | <span data-ttu-id="1b217-292">8388608</span><span class="sxs-lookup"><span data-stu-id="1b217-292">8388608</span></span> | <span data-ttu-id="1b217-293">0x00800000</span><span class="sxs-lookup"><span data-stu-id="1b217-293">0x00800000</span></span>  | <span data-ttu-id="1b217-294">**msidbControlAttributesElevationShield**</span><span class="sxs-lookup"><span data-stu-id="1b217-294">**msidbControlAttributesElevationShield**</span></span> |



 

<span data-ttu-id="1b217-295">Esse atributo do controle VolumeCostList é definido com um bit.</span><span class="sxs-lookup"><span data-stu-id="1b217-295">This attribute of VolumeCostList control is set with a bit.</span></span>



| <span data-ttu-id="1b217-296">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b217-296">Attribute</span></span>                                                                | <span data-ttu-id="1b217-297">Decimal</span><span class="sxs-lookup"><span data-stu-id="1b217-297">Decimal</span></span> | <span data-ttu-id="1b217-298">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1b217-298">Hexadecimal</span></span> | <span data-ttu-id="1b217-299">Constante</span><span class="sxs-lookup"><span data-stu-id="1b217-299">Constant</span></span>                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [<span data-ttu-id="1b217-300">ControlShowRollbackCost</span><span class="sxs-lookup"><span data-stu-id="1b217-300">ControlShowRollbackCost</span></span>](controlshowrollbackcost-control-attribute.md) | <span data-ttu-id="1b217-301">4194304</span><span class="sxs-lookup"><span data-stu-id="1b217-301">4194304</span></span> | <span data-ttu-id="1b217-302">0x00400000</span><span class="sxs-lookup"><span data-stu-id="1b217-302">0x00400000</span></span>  | <span data-ttu-id="1b217-303">**msidbControlShowRollbackCost**</span><span class="sxs-lookup"><span data-stu-id="1b217-303">**msidbControlShowRollbackCost**</span></span> |



 

<span data-ttu-id="1b217-304">Os atributos de controle a seguir não estão definidos com bits.</span><span class="sxs-lookup"><span data-stu-id="1b217-304">The following control attributes are not set with bits.</span></span> <span data-ttu-id="1b217-305">Esses atributos são criados nas tabelas de interface do usuário ou são definidos usando [eventos de controle](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="1b217-305">These attributes are authored into the user interface tables or are set using [Control Events](control-events.md).</span></span>

[<span data-ttu-id="1b217-306">Muralname</span><span class="sxs-lookup"><span data-stu-id="1b217-306">BillboardName</span></span>](billboardname-control-attribute.md)

 

[<span data-ttu-id="1b217-307">IndirectPropertyName</span><span class="sxs-lookup"><span data-stu-id="1b217-307">IndirectPropertyName</span></span>](indirectpropertyname-control-attribute.md)

 

[<span data-ttu-id="1b217-308">Posição</span><span class="sxs-lookup"><span data-stu-id="1b217-308">Position</span></span>](position-control-attribute.md)

 

[<span data-ttu-id="1b217-309">Controle de progresso</span><span class="sxs-lookup"><span data-stu-id="1b217-309">Progress Control</span></span>](progress-control-attribute.md)

 

[<span data-ttu-id="1b217-310">PropertyName</span><span class="sxs-lookup"><span data-stu-id="1b217-310">PropertyName</span></span>](propertyname-control-attribute.md)

 

[<span data-ttu-id="1b217-311">PropertyValue</span><span class="sxs-lookup"><span data-stu-id="1b217-311">PropertyValue</span></span>](propertyvalue-control-attribute.md)

 

[<span data-ttu-id="1b217-312">Text Control</span><span class="sxs-lookup"><span data-stu-id="1b217-312">Text Control</span></span>](text-control-attribute.md)

 

[<span data-ttu-id="1b217-313">TimeRemaining</span><span class="sxs-lookup"><span data-stu-id="1b217-313">TimeRemaining</span></span>](timeremaining-control-attribute.md)

<span data-ttu-id="1b217-314">Consulte [adicionando controles e texto](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="1b217-314">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

 

 



