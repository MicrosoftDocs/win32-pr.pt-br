---
description: Contém uma cláusula de sintaxe que define os dados e o tipo para o objeto MIB.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: Cláusula de sintaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765229"
---
# <a name="syntax-clause"></a><span data-ttu-id="90ae5-103">Cláusula de sintaxe</span><span class="sxs-lookup"><span data-stu-id="90ae5-103">SYNTAX Clause</span></span>

<span data-ttu-id="90ae5-104">A macro do [tipo de objeto](object-type-macro.md) contém uma cláusula de sintaxe que define os dados e o tipo do objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="90ae5-104">The [OBJECT-TYPE](object-type-macro.md) macro contains a SYNTAX clause that defines the data and type for the MIB object.</span></span> <span data-ttu-id="90ae5-105">Embora o provedor SNMP Observe as regras gerais para mapear cláusulas de sintaxe, o provedor também segue regras específicas para vários tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="90ae5-105">While the SNMP Provider observes general rules for mapping SYNTAX clauses, the provider also follows rules specific to several data types.</span></span>

> [!Note]  
> <span data-ttu-id="90ae5-106">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="90ae5-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="90ae5-107">As regras de mapeamento a seguir se aplicam a todos os tipos de dados descritos na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="90ae5-107">The following mapping rules apply to all of the data types described in the table below:</span></span>

-   <span data-ttu-id="90ae5-108">A representação textual da cláusula de sintaxe é mapeada para a **\_ Convenção textual** do qualificador de propriedade CIM.</span><span class="sxs-lookup"><span data-stu-id="90ae5-108">The textual representation of the SYNTAX clause maps to the CIM property qualifier **textual\_convention**.</span></span>
-   <span data-ttu-id="90ae5-109">A definição de tipo nomeado na cláusula SYNTAX é mapeada para a sintaxe de **objeto \_** de qualificador de propriedade CIM.</span><span class="sxs-lookup"><span data-stu-id="90ae5-109">The named type definition in the SYNTAX clause maps to the CIM property qualifier **object\_syntax**.</span></span> <span data-ttu-id="90ae5-110">Esse mapeamento difere dependendo do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="90ae5-110">This mapping differs depending on the data type.</span></span> <span data-ttu-id="90ae5-111">Para obter mais informações, consulte as descrições de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="90ae5-111">For more information, see the mapping descriptions.</span></span>
-   <span data-ttu-id="90ae5-112">O tipo SNMP usado ao codificar quadros de protocolo SNMPv1 e SNMPv2C é mapeado para a **codificação** qualificador de propriedade CIM.</span><span class="sxs-lookup"><span data-stu-id="90ae5-112">The SNMP type used when encoding SNMPv1 and SNMPv2C protocol frames maps to the CIM property qualifier **encoding**.</span></span>
-   <span data-ttu-id="90ae5-113">O qualificador de propriedade CIM **CimType** contém a representação textual que formata o valor de protocolo CIM subjacente.</span><span class="sxs-lookup"><span data-stu-id="90ae5-113">The CIM property qualifier **cimtype** contains the textual representation that formats the underlying CIM protocol value.</span></span>

<span data-ttu-id="90ae5-114">A tabela a seguir lista os tipos de dados que têm regras específicas que regem o comportamento de mapeamento do provedor.</span><span class="sxs-lookup"><span data-stu-id="90ae5-114">The following table lists data types that have specific rules that govern the provider mapping behavior.</span></span>



| <span data-ttu-id="90ae5-115">Tipo de dados SNMP</span><span class="sxs-lookup"><span data-stu-id="90ae5-115">SNMP data type</span></span>                                     | <span data-ttu-id="90ae5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="90ae5-116">Description</span></span>                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90ae5-117">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="90ae5-117">Primitive type</span></span>](#primitive-type)                  | <span data-ttu-id="90ae5-118">Um dos tipos de dados básicos definidos na estrutura das informações de gerenciamento (SMI) documenta RFC 1213 e RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="90ae5-118">One of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span>                                                                                                                            |
| [<span data-ttu-id="90ae5-119">Convenção textual</span><span class="sxs-lookup"><span data-stu-id="90ae5-119">Textual convention</span></span>](textual-convention-macro.md) | <span data-ttu-id="90ae5-120">Definição de tipo gerada por meio do uso explícito da macro de **Convenção textual** do SNMPv2c ou gerada por meio do uso de um tipo nomeado.</span><span class="sxs-lookup"><span data-stu-id="90ae5-120">Type definition generated through the explicit use of the SNMPv2C **TEXTUAL-CONVENTION** macro or generated through the use of a named type.</span></span> <span data-ttu-id="90ae5-121">Uma convenção textual atribui um nome e, em alguns casos, um intervalo de valores a um tipo de dados existente.</span><span class="sxs-lookup"><span data-stu-id="90ae5-121">A textual convention assigns a name and, in some cases, a range of values to an existing data type.</span></span> |
| [<span data-ttu-id="90ae5-122">Tipo nomeado</span><span class="sxs-lookup"><span data-stu-id="90ae5-122">Named type</span></span>](#named-type)                          | <span data-ttu-id="90ae5-123">Referência nomeada para um tipo primitivo, Convenção textual ou tipo restrito.</span><span class="sxs-lookup"><span data-stu-id="90ae5-123">Named reference to a primitive type, textual convention, or constrained type.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="90ae5-124">Tipo restrito</span><span class="sxs-lookup"><span data-stu-id="90ae5-124">Constrained type</span></span>](#constrained-type)              | <span data-ttu-id="90ae5-125">Tipo primitivo, tipo nomeado ou convenção de texto que foi restringido por algum mecanismo de subdigitação definido nos documentos do SMI RFC 1213 e RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="90ae5-125">Primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span>                                                                                      |



 

## <a name="primitive-type"></a><span data-ttu-id="90ae5-126">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="90ae5-126">Primitive Type</span></span>

<span data-ttu-id="90ae5-127">O tipo primitivo é um dos tipos de dados básicos definidos na estrutura de informações de gerenciamento (SMI) documentos RFC 1213 e RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="90ae5-127">The primitive type is one of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="90ae5-128">Os tipos primitivos SNMP são mapeados para tipos definidos pelo CIM.</span><span class="sxs-lookup"><span data-stu-id="90ae5-128">SNMP primitive types map to CIM-defined types.</span></span> <span data-ttu-id="90ae5-129">A tabela a seguir lista o mapeamento que ocorre quando a cláusula SYNTAX se refere explicitamente a um tipo primitivo para SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="90ae5-129">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv1.</span></span> <span data-ttu-id="90ae5-130">Os qualificadores de **\_ sintaxe de objeto** , **codificação** e **\_ Convenção textual** são sempre iguais aos do tipo MIB e o valor padrão é sempre **nulo**.</span><span class="sxs-lookup"><span data-stu-id="90ae5-130">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="90ae5-131">Tipo de MIB</span><span class="sxs-lookup"><span data-stu-id="90ae5-131">MIB type</span></span>         | <span data-ttu-id="90ae5-132">Tipo de variante CIM</span><span class="sxs-lookup"><span data-stu-id="90ae5-132">CIM variant type</span></span> | <span data-ttu-id="90ae5-133">valor de CimType</span><span class="sxs-lookup"><span data-stu-id="90ae5-133">cimtype value</span></span> |
|------------------|------------------|---------------|
| <span data-ttu-id="90ae5-134">INTEGER</span><span class="sxs-lookup"><span data-stu-id="90ae5-134">INTEGER</span></span>          | <span data-ttu-id="90ae5-135">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="90ae5-135">VT\_I4</span></span>           | <span data-ttu-id="90ae5-136">**sint32**</span><span class="sxs-lookup"><span data-stu-id="90ae5-136">**sint32**</span></span>    |
| <span data-ttu-id="90ae5-137">OCTETstring</span><span class="sxs-lookup"><span data-stu-id="90ae5-137">OCTETSTRING</span></span>      | <span data-ttu-id="90ae5-138">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-138">VT\_BSTR</span></span>         | <span data-ttu-id="90ae5-139">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90ae5-139">**string**</span></span>    |
| <span data-ttu-id="90ae5-140">OBJECTIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="90ae5-140">OBJECTIDENTIFIER</span></span> | <span data-ttu-id="90ae5-141">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-141">VT\_BSTR</span></span>         | <span data-ttu-id="90ae5-142">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90ae5-142">**string**</span></span>    |
| <span data-ttu-id="90ae5-143">NULO</span><span class="sxs-lookup"><span data-stu-id="90ae5-143">NULL</span></span>             | <span data-ttu-id="90ae5-144">VT \_ nulo</span><span class="sxs-lookup"><span data-stu-id="90ae5-144">VT\_NULL</span></span>         | <span data-ttu-id="90ae5-145">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="90ae5-145">Not supported</span></span> |
| <span data-ttu-id="90ae5-146">IpAddress</span><span class="sxs-lookup"><span data-stu-id="90ae5-146">IpAddress</span></span>        | <span data-ttu-id="90ae5-147">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-147">VT\_BSTR</span></span>         | <span data-ttu-id="90ae5-148">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90ae5-148">**string**</span></span>    |
| <span data-ttu-id="90ae5-149">Contador</span><span class="sxs-lookup"><span data-stu-id="90ae5-149">Counter</span></span>          | <span data-ttu-id="90ae5-150">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="90ae5-150">VT\_I4</span></span>           | <span data-ttu-id="90ae5-151">**uint32**</span><span class="sxs-lookup"><span data-stu-id="90ae5-151">**uint32**</span></span>    |
| <span data-ttu-id="90ae5-152">Medidor</span><span class="sxs-lookup"><span data-stu-id="90ae5-152">Gauge</span></span>            | <span data-ttu-id="90ae5-153">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="90ae5-153">VT\_I4</span></span>           | <span data-ttu-id="90ae5-154">**uint32**</span><span class="sxs-lookup"><span data-stu-id="90ae5-154">**uint32**</span></span>    |
| <span data-ttu-id="90ae5-155">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="90ae5-155">TimeTicks</span></span>        | <span data-ttu-id="90ae5-156">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="90ae5-156">VT\_I4</span></span>           | <span data-ttu-id="90ae5-157">**uint32**</span><span class="sxs-lookup"><span data-stu-id="90ae5-157">**uint32**</span></span>    |
| <span data-ttu-id="90ae5-158">Opaco</span><span class="sxs-lookup"><span data-stu-id="90ae5-158">Opaque</span></span>           | <span data-ttu-id="90ae5-159">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-159">VT\_BSTR</span></span>         | <span data-ttu-id="90ae5-160">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90ae5-160">**string**</span></span>    |
| <span data-ttu-id="90ae5-161">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="90ae5-161">NetworkAddress</span></span>   | <span data-ttu-id="90ae5-162">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-162">VT\_BSTR</span></span>         | <span data-ttu-id="90ae5-163">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90ae5-163">**string**</span></span>    |



 

<span data-ttu-id="90ae5-164">O provedor ignora a macro do tipo de objeto quando a cláusula SYNTAX refere-se a **NULL**, seja explicitamente ou por meio de uma atribuição de tipo nomeado.</span><span class="sxs-lookup"><span data-stu-id="90ae5-164">The provider ignores the OBJECT-TYPE macro when the SYNTAX clause refers to **NULL**, either explicitly or through a named type assignment.</span></span> <span data-ttu-id="90ae5-165">A tabela a seguir lista o mapeamento que ocorre quando a cláusula SYNTAX se refere explicitamente a um tipo primitivo para SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="90ae5-165">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv2.</span></span> <span data-ttu-id="90ae5-166">Os qualificadores de **\_ sintaxe de objeto** , **codificação** e **\_ Convenção textual** são sempre iguais aos do tipo MIB e o valor padrão é sempre **nulo**.</span><span class="sxs-lookup"><span data-stu-id="90ae5-166">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="90ae5-167">Tipo de MIB</span><span class="sxs-lookup"><span data-stu-id="90ae5-167">MIB type</span></span>          | <span data-ttu-id="90ae5-168">Tipo de variante CIM</span><span class="sxs-lookup"><span data-stu-id="90ae5-168">CIM variant type</span></span> | <span data-ttu-id="90ae5-169">valor de CimType</span><span class="sxs-lookup"><span data-stu-id="90ae5-169">cimtype value</span></span> |
|-------------------|------------------|---------------|
| <span data-ttu-id="90ae5-170">INTEGER</span><span class="sxs-lookup"><span data-stu-id="90ae5-170">INTEGER</span></span>           | <span data-ttu-id="90ae5-171">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="90ae5-171">VT\_I4</span></span>           | <span data-ttu-id="90ae5-172">**sint32**</span><span class="sxs-lookup"><span data-stu-id="90ae5-172">**sint32**</span></span>    |
| <span data-ttu-id="90ae5-173">CADEIA DE CARACTERES DE OCTETO</span><span class="sxs-lookup"><span data-stu-id="90ae5-173">OCTET STRING</span></span>      | <span data-ttu-id="90ae5-174">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-174">VT\_BSTR</span></span>         | <span data-ttu-id="90ae5-175">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90ae5-175">**string**</span></span>    |
| <span data-ttu-id="90ae5-176">IDENTIFICADOR DE OBJETO</span><span class="sxs-lookup"><span data-stu-id="90ae5-176">OBJECT IDENTIFIER</span></span> | <span data-ttu-id="90ae5-177">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-177">VT\_BSTR</span></span>         | <span data-ttu-id="90ae5-178">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90ae5-178">**string**</span></span>    |
| <span data-ttu-id="90ae5-179">IpAddress</span><span class="sxs-lookup"><span data-stu-id="90ae5-179">IpAddress</span></span>         | <span data-ttu-id="90ae5-180">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-180">VT\_BSTR</span></span>         | <span data-ttu-id="90ae5-181">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90ae5-181">**string**</span></span>    |
| <span data-ttu-id="90ae5-182">Counter32</span><span class="sxs-lookup"><span data-stu-id="90ae5-182">Counter32</span></span>         | <span data-ttu-id="90ae5-183">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="90ae5-183">VT\_I4</span></span>           | <span data-ttu-id="90ae5-184">**uint32**</span><span class="sxs-lookup"><span data-stu-id="90ae5-184">**uint32**</span></span>    |
| <span data-ttu-id="90ae5-185">Gauge32</span><span class="sxs-lookup"><span data-stu-id="90ae5-185">Gauge32</span></span>           | <span data-ttu-id="90ae5-186">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="90ae5-186">VT\_I4</span></span>           | <span data-ttu-id="90ae5-187">**uint32**</span><span class="sxs-lookup"><span data-stu-id="90ae5-187">**uint32**</span></span>    |
| <span data-ttu-id="90ae5-188">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="90ae5-188">Unsigned32</span></span>        | <span data-ttu-id="90ae5-189">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="90ae5-189">VT\_I4</span></span>           | <span data-ttu-id="90ae5-190">**uint32**</span><span class="sxs-lookup"><span data-stu-id="90ae5-190">**uint32**</span></span>    |
| <span data-ttu-id="90ae5-191">Integer32</span><span class="sxs-lookup"><span data-stu-id="90ae5-191">Integer32</span></span>         | <span data-ttu-id="90ae5-192">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="90ae5-192">VT\_I4</span></span>           | <span data-ttu-id="90ae5-193">**sint32**</span><span class="sxs-lookup"><span data-stu-id="90ae5-193">**sint32**</span></span>    |
| <span data-ttu-id="90ae5-194">Counter64</span><span class="sxs-lookup"><span data-stu-id="90ae5-194">Counter64</span></span>         | <span data-ttu-id="90ae5-195">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-195">VT\_BSTR</span></span>         | <span data-ttu-id="90ae5-196">**uint64**</span><span class="sxs-lookup"><span data-stu-id="90ae5-196">**uint64**</span></span>    |
| <span data-ttu-id="90ae5-197">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="90ae5-197">TimeTicks</span></span>         | <span data-ttu-id="90ae5-198">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="90ae5-198">VT\_I4</span></span>           | <span data-ttu-id="90ae5-199">**uint32**</span><span class="sxs-lookup"><span data-stu-id="90ae5-199">**uint32**</span></span>    |
| <span data-ttu-id="90ae5-200">Opaco</span><span class="sxs-lookup"><span data-stu-id="90ae5-200">Opaque</span></span>            | <span data-ttu-id="90ae5-201">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-201">VT\_BSTR</span></span>         | <span data-ttu-id="90ae5-202">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90ae5-202">**string**</span></span>    |



 

## <a name="named-type"></a><span data-ttu-id="90ae5-203">Tipo nomeado</span><span class="sxs-lookup"><span data-stu-id="90ae5-203">Named Type</span></span>

<span data-ttu-id="90ae5-204">Os tipos nomeados do SNMP são mapeados para tipos definidos pelo CIM.</span><span class="sxs-lookup"><span data-stu-id="90ae5-204">SNMP named types map to CIM-defined types.</span></span> <span data-ttu-id="90ae5-205">Quando a cláusula SYNTAX se refere a um [tipo primitivo](#primitive-type), [Convenção textual](textual-convention-macro.md)ou [tipo restrito](#constrained-type) por meio de uma derivação de atribuição de tipo, use esses tipos para determinar quais procedimentos de mapeamento se aplicam.</span><span class="sxs-lookup"><span data-stu-id="90ae5-205">When the SYNTAX clause refers to a [primitive type](#primitive-type), [textual convention](textual-convention-macro.md), or [constrained type](#constrained-type) through a type assignment derivation, use the those types to determine which mapping procedures apply.</span></span>

-   <span data-ttu-id="90ae5-206">Se, por meio da derivação das regras de atribuição de tipo, você encontrará uma definição de tipo restrito:</span><span class="sxs-lookup"><span data-stu-id="90ae5-206">If, through derivation of the type assignment rules, you encounter a constrained type definition:</span></span>

    -   <span data-ttu-id="90ae5-207">E se, por meio de derivação adicional, você encontrar uma das convenções textuais listadas na [macro de Convenção textual](textual-convention-macro.md), aplique as regras de mapeamento para tipos restritos e convenções de texto.</span><span class="sxs-lookup"><span data-stu-id="90ae5-207">And if, through further derivation, you encounter one of the textual conventions listed in [TEXTUAL-CONVENTION Macro](textual-convention-macro.md), then apply the mapping rules for constrained types and textual conventions.</span></span>
    -   <span data-ttu-id="90ae5-208">Caso contrário, se você encontrar um dos tipos primitivos listados em uma tabela de tipo primitivo, aplique as regras de mapeamento para tipos primitivos e tipos restritos.</span><span class="sxs-lookup"><span data-stu-id="90ae5-208">Otherwise, if you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types and constrained types.</span></span>

-   <span data-ttu-id="90ae5-209">Se você encontrar uma das convenções textuais listadas na [ \_ macro Convenção textual](textual-convention-macro.md), aplique as regras de mapeamento para as convenções textuais.</span><span class="sxs-lookup"><span data-stu-id="90ae5-209">If you encounter one of the textual conventions listed in [TEXTUAL\_CONVENTION Macro](textual-convention-macro.md), apply the mapping rules for textual conventions.</span></span>
-   <span data-ttu-id="90ae5-210">Se você encontrar um dos tipos primitivos listados em uma tabela de tipo primitivo, aplique as regras de mapeamento para tipos primitivos.</span><span class="sxs-lookup"><span data-stu-id="90ae5-210">If you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types.</span></span>

> [!Note]  
> <span data-ttu-id="90ae5-211">Classes que contêm tipos de propriedade que não estão em conformidade com o mapeamento descrito acima não são válidas.</span><span class="sxs-lookup"><span data-stu-id="90ae5-211">Classes containing property types that do not conform to the mapping described above are not valid.</span></span> <span data-ttu-id="90ae5-212">Nesse caso, o provedor retornará um erro se e quando o provedor solicitar a recuperação de uma definição de classe durante a execução de uma função de recuperação de instância.</span><span class="sxs-lookup"><span data-stu-id="90ae5-212">In this case, the provider returns an error if and when the provider requests the retrieval of a class definition while executing an instance retrieval function.</span></span>

 

## <a name="constrained-type"></a><span data-ttu-id="90ae5-213">Tipo restrito</span><span class="sxs-lookup"><span data-stu-id="90ae5-213">Constrained Type</span></span>

<span data-ttu-id="90ae5-214">Um tipo restrito é um tipo primitivo, tipo nomeado ou convenção textual que foi restringido por algum mecanismo de subdigitação definido nos documentos do SMI RFC 1213 e RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="90ae5-214">A constrained type is a primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="90ae5-215">Quando ocorre uma subdigitação, qualificadores CIM adicionais são necessários para especificar os valores de subtipo.</span><span class="sxs-lookup"><span data-stu-id="90ae5-215">When subtyping occurs, additional CIM qualifiers are required to specify the subtype values.</span></span> <span data-ttu-id="90ae5-216">A definição de tipo nomeado na cláusula de sintaxe mapeia literalmente para a **\_ sintaxe de objeto** do qualificador de propriedade CIM até, mas não incluindo as restrições do subtipo.</span><span class="sxs-lookup"><span data-stu-id="90ae5-216">The named-type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax** up to, but not including the constraints of the subtype.</span></span>

<span data-ttu-id="90ae5-217">Os subtipos podem seguir qualquer um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="90ae5-217">Subtypes may follow any of the following formats:</span></span>

-   <span data-ttu-id="90ae5-218">INTEIRO enumerado</span><span class="sxs-lookup"><span data-stu-id="90ae5-218">Enumerated INTEGER</span></span>

    <span data-ttu-id="90ae5-219">A **Enumeração** de qualificador de propriedade CIM especifica os valores enumerados.</span><span class="sxs-lookup"><span data-stu-id="90ae5-219">The CIM property qualifier **enumeration** specifies the enumerated values.</span></span> <span data-ttu-id="90ae5-220">Esse qualificador é representado como uma cadeia de caracteres que contém uma lista separada por vírgulas de valores inteiros de 32 bits assinados.</span><span class="sxs-lookup"><span data-stu-id="90ae5-220">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="90ae5-221">A tabela a seguir lista os tipos de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="90ae5-221">The following table lists the mapping types.</span></span> <span data-ttu-id="90ae5-222">O valor padrão é sempre **nulo**.</span><span class="sxs-lookup"><span data-stu-id="90ae5-222">The default value is always **NULL**.</span></span>



| <span data-ttu-id="90ae5-223">Tipo de MIB restrito</span><span class="sxs-lookup"><span data-stu-id="90ae5-223">Constrained MIB type</span></span> | <span data-ttu-id="90ae5-224">Tipo de variante CIM</span><span class="sxs-lookup"><span data-stu-id="90ae5-224">CIM variant type</span></span> | <span data-ttu-id="90ae5-225">Qualificadores CIM</span><span class="sxs-lookup"><span data-stu-id="90ae5-225">CIM qualifiers</span></span>                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90ae5-226">INTEIRO enumerado</span><span class="sxs-lookup"><span data-stu-id="90ae5-226">Enumerated INTEGER</span></span>   | <span data-ttu-id="90ae5-227">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-227">VT\_BSTR</span></span>         | <span data-ttu-id="90ae5-228">**\_ Convenção textual**: enumeratedinteger</span><span class="sxs-lookup"><span data-stu-id="90ae5-228">**textual\_convention**: enumeratedinteger</span></span><br/> <span data-ttu-id="90ae5-229">**codificação**: inteiro</span><span class="sxs-lookup"><span data-stu-id="90ae5-229">**encoding**: INTEGER</span></span><br/> <span data-ttu-id="90ae5-230">**CimType**: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="90ae5-230">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="90ae5-231">BITS</span><span class="sxs-lookup"><span data-stu-id="90ae5-231">BITS</span></span>

    <span data-ttu-id="90ae5-232">Os **bits** do qualificador de propriedade CIM especificam os valores enumerados.</span><span class="sxs-lookup"><span data-stu-id="90ae5-232">The CIM property qualifier **bits** specifies the enumerated values.</span></span> <span data-ttu-id="90ae5-233">Esse qualificador é representado como uma cadeia de caracteres que contém uma lista separada por vírgulas de valores inteiros de 32 bits assinados.</span><span class="sxs-lookup"><span data-stu-id="90ae5-233">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="90ae5-234">A tabela a seguir lista os tipos de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="90ae5-234">The following table lists the mapping types.</span></span> <span data-ttu-id="90ae5-235">O valor padrão é sempre **nulo**.</span><span class="sxs-lookup"><span data-stu-id="90ae5-235">The default value is always **NULL**.</span></span>



| <span data-ttu-id="90ae5-236">Tipo de MIB restrito</span><span class="sxs-lookup"><span data-stu-id="90ae5-236">Constrained MIB type</span></span> | <span data-ttu-id="90ae5-237">Tipo de variante CIM</span><span class="sxs-lookup"><span data-stu-id="90ae5-237">CIM variant type</span></span>      | <span data-ttu-id="90ae5-238">Qualificadores CIM</span><span class="sxs-lookup"><span data-stu-id="90ae5-238">CIM qualifiers</span></span>                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90ae5-239">BITS</span><span class="sxs-lookup"><span data-stu-id="90ae5-239">BITS</span></span>                 | <span data-ttu-id="90ae5-240">\_matriz VT \| VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="90ae5-240">VT\_ARRAY \| VT\_BSTR</span></span> | <span data-ttu-id="90ae5-241">**\_ Convenção textual**: bits</span><span class="sxs-lookup"><span data-stu-id="90ae5-241">**textual\_convention**: bits</span></span><br/> <span data-ttu-id="90ae5-242">**codificação**: octetstring</span><span class="sxs-lookup"><span data-stu-id="90ae5-242">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="90ae5-243">**CimType**: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="90ae5-243">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="90ae5-244">Comprimento variável</span><span class="sxs-lookup"><span data-stu-id="90ae5-244">Variable-length</span></span>

    <span data-ttu-id="90ae5-245">Quando a cláusula SYNTAX refere-se a um tipo primitivo, tipo nomeado ou convenção textual que é subtipoada como uma cadeia de caracteres de OCTETO de comprimento variável ou opaco, **o \_ comprimento da variável** de qualificador de propriedade CIM especifica os valores mínimo, máximo e de comprimento fixo associados à definição de tipo.</span><span class="sxs-lookup"><span data-stu-id="90ae5-245">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a variable-length OCTET STRING or Opaque, the CIM property qualifier **variable\_length** specifies the minimum, maximum, and fixed-length values associated with the type definition.</span></span> <span data-ttu-id="90ae5-246">Esse qualificador é implementado como uma cadeia de caracteres no seguinte formato em que os valores de comprimento variável são representados como inteiros de 32 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="90ae5-246">This qualifier is implemented as a string in the following format where the variable-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   <span data-ttu-id="90ae5-247">Comprimento fixo</span><span class="sxs-lookup"><span data-stu-id="90ae5-247">Fixed-length</span></span>

    <span data-ttu-id="90ae5-248">Quando a cláusula SYNTAX refere-se a um tipo primitivo, tipo nomeado ou convenção textual que é subtipoado como uma cadeia de caracteres de OCTETO de comprimento fixo ou opaco, **o \_ comprimento fixo** do qualificador de propriedade CIM especifica o valor de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="90ae5-248">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a fixed-length OCTET STRING or Opaque, the CIM property qualifier **fixed\_length** specifies the fixed-length value.</span></span> <span data-ttu-id="90ae5-249">Esse qualificador é representado como um valor inteiro de 32 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="90ae5-249">This qualifier is represented as an unsigned 32-bit integer value.</span></span>

-   <span data-ttu-id="90ae5-250">Intervalo</span><span class="sxs-lookup"><span data-stu-id="90ae5-250">Range</span></span>

    <span data-ttu-id="90ae5-251">Quando a cláusula SYNTAX refere-se a um tipo primitivo, um tipo nomeado ou uma convenção textual que é subtipoda como um inteiro ou medidor de valor fixo ou de intervalo, o **\_ valor da variável** qualificador de propriedade CIM especifica os valores de intervalo e fixo associados à definição de tipo.</span><span class="sxs-lookup"><span data-stu-id="90ae5-251">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a ranged or fixed-value INTEGER or Gauge, the CIM property qualifier **variable\_value** specifies the ranged and fixed values associated with the type definition.</span></span> <span data-ttu-id="90ae5-252">Esse qualificador é implementado como uma cadeia de caracteres no seguinte formato em que os valores de intervalo e comprimento fixo são representados como inteiros de 32 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="90ae5-252">This qualifier is implemented as a string in the following format where the range and fixed-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a><span data-ttu-id="90ae5-253">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="90ae5-253">Example Code</span></span>

<span data-ttu-id="90ae5-254">O exemplo a seguir descreve um subtipo inteiro enumerado.</span><span class="sxs-lookup"><span data-stu-id="90ae5-254">The following example describes an enumerated INTEGER subtype.</span></span>

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

<span data-ttu-id="90ae5-255">Este exemplo é mapeado para:</span><span class="sxs-lookup"><span data-stu-id="90ae5-255">This example maps to:</span></span>

``` syntax
enumeration("up(1),down(2),testing(3)")
```

<span data-ttu-id="90ae5-256">O exemplo de código a seguir descreve um subtipo BITS.</span><span class="sxs-lookup"><span data-stu-id="90ae5-256">The following code example describes a BITS subtype.</span></span>

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

<span data-ttu-id="90ae5-257">O exemplo de código a seguir mapeia para:</span><span class="sxs-lookup"><span data-stu-id="90ae5-257">The following code example maps to:</span></span>

``` syntax
bits("up(1),down(2),testing(3)")
```

<span data-ttu-id="90ae5-258">O exemplo de código a seguir descreve um subtipo de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="90ae5-258">The following code example describes a variable-length subtype.</span></span>

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

<span data-ttu-id="90ae5-259">Este exemplo é mapeado para:</span><span class="sxs-lookup"><span data-stu-id="90ae5-259">This example maps to:</span></span>

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

<span data-ttu-id="90ae5-260">O exemplo a seguir descreve um subtipo de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="90ae5-260">The following example describes a fixed-length subtype.</span></span>

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

<span data-ttu-id="90ae5-261">Este exemplo é mapeado para:</span><span class="sxs-lookup"><span data-stu-id="90ae5-261">This example maps to:</span></span>

``` syntax
fixed_length(6)
```

<span data-ttu-id="90ae5-262">O exemplo a seguir descreve um subtipo de intervalo.</span><span class="sxs-lookup"><span data-stu-id="90ae5-262">The following example describes a range subtype.</span></span>

``` syntax
Status := INTEGER (10..20|8)
```

<span data-ttu-id="90ae5-263">Este exemplo é mapeado para:</span><span class="sxs-lookup"><span data-stu-id="90ae5-263">This example maps to:</span></span>

``` syntax
variable_value("10..20,8")
```

 

 




