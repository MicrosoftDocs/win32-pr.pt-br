---
description: As convenções de texto SNMP são mapeadas para tipos definidos pelo CIM.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: Macro de Convenção TEXTUAL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764456"
---
# <a name="textual-convention-macro"></a><span data-ttu-id="a64c1-103">Macro de Convenção TEXTUAL</span><span class="sxs-lookup"><span data-stu-id="a64c1-103">TEXTUAL-CONVENTION Macro</span></span>

<span data-ttu-id="a64c1-104">As convenções de texto SNMP são mapeadas para tipos definidos pelo CIM.</span><span class="sxs-lookup"><span data-stu-id="a64c1-104">SNMP textual conventions map to CIM-defined types.</span></span>

> [!Note]  
> <span data-ttu-id="a64c1-105">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a64c1-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="a64c1-106">As regras de mapeamento a seguir se aplicam às convenções de texto SNMP:</span><span class="sxs-lookup"><span data-stu-id="a64c1-106">The following mapping rules apply to SNMP textual conventions:</span></span>

-   <span data-ttu-id="a64c1-107">A definição de tipo nomeado na cláusula SYNTAX mapeia literalmente para a **\_ sintaxe de objeto** de qualificador de propriedade CIM.</span><span class="sxs-lookup"><span data-stu-id="a64c1-107">The named type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax**.</span></span>
-   <span data-ttu-id="a64c1-108">Use a tabela a seguir para mapear as convenções de texto quando a cláusula SYNTAX se referir explicitamente a uma convenção textual de uma macro de Convenção TEXTUAL do SNMPv2C ou se referir a uma convenção textual implícita.</span><span class="sxs-lookup"><span data-stu-id="a64c1-108">Use the following table to map textual conventions when the SYNTAX clause explicitly refers to a textual convention of a SNMPv2C TEXTUAL-CONVENTION macro, or refers to an implied textual convention.</span></span> <span data-ttu-id="a64c1-109">O valor padrão é sempre **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a64c1-109">The default value is always **NULL**.</span></span>



| <span data-ttu-id="a64c1-110">Convenção textual</span><span class="sxs-lookup"><span data-stu-id="a64c1-110">Textual convention</span></span> | <span data-ttu-id="a64c1-111">Tipo de variante CIM</span><span class="sxs-lookup"><span data-stu-id="a64c1-111">CIM variant type</span></span> | <span data-ttu-id="a64c1-112">Qualificador CIM</span><span class="sxs-lookup"><span data-stu-id="a64c1-112">CIM qualifier</span></span>                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a64c1-113">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="a64c1-113">DateAndTime</span></span>        | <span data-ttu-id="a64c1-114">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a64c1-114">**VT\_BSTR**</span></span>     | <span data-ttu-id="a64c1-115">**\_ Convenção textual**: DateAndTime</span><span class="sxs-lookup"><span data-stu-id="a64c1-115">**textual\_convention**: DateAndTime</span></span><br/> <span data-ttu-id="a64c1-116">**codificação**: octetstring</span><span class="sxs-lookup"><span data-stu-id="a64c1-116">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="a64c1-117">**\_ sintaxe do objeto**: DateAndTime</span><span class="sxs-lookup"><span data-stu-id="a64c1-117">**object\_syntax**: DateAndTime</span></span><br/> <span data-ttu-id="a64c1-118">**CimType**: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a64c1-118">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="a64c1-119">DisplayString</span><span class="sxs-lookup"><span data-stu-id="a64c1-119">Displaystring</span></span>      | <span data-ttu-id="a64c1-120">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a64c1-120">**VT\_BSTR**</span></span>     | <span data-ttu-id="a64c1-121">**\_ Convenção textual**: DisplayString</span><span class="sxs-lookup"><span data-stu-id="a64c1-121">**textual\_convention**: Displaystring</span></span><br/> <span data-ttu-id="a64c1-122">**codificação**: octetstring</span><span class="sxs-lookup"><span data-stu-id="a64c1-122">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="a64c1-123">**\_ sintaxe do objeto**: DisplayString</span><span class="sxs-lookup"><span data-stu-id="a64c1-123">**object\_syntax**: Displaystring</span></span><br/> <span data-ttu-id="a64c1-124">**CimType**: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a64c1-124">**cimtype**: string</span></span><br/>   |
| <span data-ttu-id="a64c1-125">MacAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-125">MacAddress</span></span>         | <span data-ttu-id="a64c1-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a64c1-126">**VT\_BSTR**</span></span>     | <span data-ttu-id="a64c1-127">**\_ Convenção textual**: MACAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-127">**textual\_convention**: MacAddress</span></span><br/> <span data-ttu-id="a64c1-128">**codificação**: octetstring</span><span class="sxs-lookup"><span data-stu-id="a64c1-128">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="a64c1-129">**\_ sintaxe do objeto**: MACAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-129">**object\_syntax**: MacAddress</span></span><br/> <span data-ttu-id="a64c1-130">**CimType**: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a64c1-130">**cimtype**: string</span></span><br/>         |
| <span data-ttu-id="a64c1-131">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-131">PhysAddress</span></span>        | <span data-ttu-id="a64c1-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a64c1-132">**VT\_BSTR**</span></span>     | <span data-ttu-id="a64c1-133">**\_ Convenção textual**: PhysAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-133">**textual\_convention**: PhysAddress</span></span><br/> <span data-ttu-id="a64c1-134">**codificação**: octetstring</span><span class="sxs-lookup"><span data-stu-id="a64c1-134">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="a64c1-135">**\_ sintaxe do objeto**: PhysAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-135">**object\_syntax**: PhysAddress</span></span><br/> <span data-ttu-id="a64c1-136">**CimType**: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a64c1-136">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="a64c1-137">SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-137">SnmpUDPAddress</span></span>     | <span data-ttu-id="a64c1-138">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a64c1-138">**VT\_BSTR**</span></span>     | <span data-ttu-id="a64c1-139">**\_ Convenção textual**: SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-139">**textual\_convention**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="a64c1-140">**codificação**: octetstring</span><span class="sxs-lookup"><span data-stu-id="a64c1-140">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="a64c1-141">**\_ sintaxe do objeto**: SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-141">**object\_syntax**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="a64c1-142">**CimType**: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a64c1-142">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="a64c1-143">SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-143">SnmpOSIAddress</span></span>     | <span data-ttu-id="a64c1-144">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a64c1-144">**VT\_BSTR**</span></span>     | <span data-ttu-id="a64c1-145">**\_ Convenção textual**: SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-145">**textual\_convention**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="a64c1-146">**codificação**: octetstring</span><span class="sxs-lookup"><span data-stu-id="a64c1-146">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="a64c1-147">**\_ sintaxe do objeto**: SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-147">**object\_syntax**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="a64c1-148">**CimType**: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a64c1-148">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="a64c1-149">SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-149">SnmpIPXAddress</span></span>     | <span data-ttu-id="a64c1-150">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a64c1-150">**VT\_BSTR**</span></span>     | <span data-ttu-id="a64c1-151">**\_ Convenção textual**: SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-151">**textual\_convention**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="a64c1-152">**codificação**: octetstring</span><span class="sxs-lookup"><span data-stu-id="a64c1-152">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="a64c1-153">**\_ sintaxe do objeto**: SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="a64c1-153">**object\_syntax**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="a64c1-154">**CimType**: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a64c1-154">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="a64c1-155">O tipo de variante definido pelo CIM e os qualificadores de propriedade CIM **\_ Convenção textual**, **codificação**, **\_ sintaxe de objeto** e mapa **CimType** usando o tipo primitivo subjacente.</span><span class="sxs-lookup"><span data-stu-id="a64c1-155">The CIM-defined variant type and the CIM property qualifiers **textual\_convention**, **encoding**, **object\_syntax**, and **cimtype** map using the underlying primitive type.</span></span>
-   <span data-ttu-id="a64c1-156">A cláusula DISPLAY-HINT da macro de Convenção TEXTUAL do SNMPv2C mapeia textualmente para a dica de **exibição \_** do qualificador de propriedade CIM.</span><span class="sxs-lookup"><span data-stu-id="a64c1-156">The DISPLAY-HINT clause of the SNMPv2C TEXTUAL-CONVENTION macro maps verbatim to the CIM property qualifier **display\_hint**.</span></span> <span data-ttu-id="a64c1-157">Esse qualificador não será gerado se não houver uma macro de Convenção TEXTUAL ou a macro não contiver uma cláusula de dica de exibição.</span><span class="sxs-lookup"><span data-stu-id="a64c1-157">This qualifier is not generated if there is no TEXTUAL-CONVENTION macro, or the macro does not contain a DISPLAY-HINT clause.</span></span>

## <a name="example-code"></a><span data-ttu-id="a64c1-158">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="a64c1-158">Example Code</span></span>

<span data-ttu-id="a64c1-159">O exemplo a seguir descreve uma Convenção de texto SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="a64c1-159">The following example describes an SNMPv1 textual convention.</span></span>

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

<span data-ttu-id="a64c1-160">Este exemplo gera os seguintes qualificadores CIM.</span><span class="sxs-lookup"><span data-stu-id="a64c1-160">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

<span data-ttu-id="a64c1-161">O exemplo a seguir descreve uma convenção textual de SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="a64c1-161">The following example describes an SNMPv2 textual convention.</span></span>

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

<span data-ttu-id="a64c1-162">Este exemplo gera os seguintes qualificadores CIM.</span><span class="sxs-lookup"><span data-stu-id="a64c1-162">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




