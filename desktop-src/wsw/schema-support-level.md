---
title: Nível de suporte do esquema
description: Esta seção aborda os detalhes sobre o nível de suporte ao esquema.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Serviços Web de nível de suporte do esquema para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104563768"
---
# <a name="schema-support-level"></a><span data-ttu-id="92b41-106">Nível de suporte do esquema</span><span class="sxs-lookup"><span data-stu-id="92b41-106">Schema support level</span></span>

<span data-ttu-id="92b41-107">Esta seção aborda os detalhes sobre o nível de suporte ao esquema.</span><span class="sxs-lookup"><span data-stu-id="92b41-107">This section covers the details around the level of schema support.</span></span>


<span data-ttu-id="92b41-108">O esquema dá suporte diretamente ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="92b41-108">The schema directly supports the following:</span></span>

-   <span data-ttu-id="92b41-109">Sequências de elementos.</span><span class="sxs-lookup"><span data-stu-id="92b41-109">Sequences of elements.</span></span>
-   <span data-ttu-id="92b41-110">Derivação de tipos de elemento.</span><span class="sxs-lookup"><span data-stu-id="92b41-110">Derivation of element types.</span></span>
-   <span data-ttu-id="92b41-111">Opções simples de elementos (aqueles que são mapeados para uma União marcada).</span><span class="sxs-lookup"><span data-stu-id="92b41-111">Simple choices of elements (those that map to a tagged union).</span></span>
-   <span data-ttu-id="92b41-112">Tipos básicos definidos pelo formato binário XSD/.NET incluindo intervalos (mín./máx.).</span><span class="sxs-lookup"><span data-stu-id="92b41-112">Basic types defined by XSD / .NET binary format including ranges (min/max).</span></span>
-   <span data-ttu-id="92b41-113">Suporte simples para qualquer elemento (sem restrições no tipo de elemento).</span><span class="sxs-lookup"><span data-stu-id="92b41-113">Simple support for any element (no restrictions on type of element).</span></span>
-   <span data-ttu-id="92b41-114">Elementos opcionais e atributos com valores padrão.</span><span class="sxs-lookup"><span data-stu-id="92b41-114">Optional elements and attributes with default values.</span></span>
-   <span data-ttu-id="92b41-115">Repetindo elementos com intervalos (mín./máx.).</span><span class="sxs-lookup"><span data-stu-id="92b41-115">Repeating elements with ranges (min/max).</span></span>
-   <span data-ttu-id="92b41-116">Elementos anuláveis.</span><span class="sxs-lookup"><span data-stu-id="92b41-116">Nillable elements.</span></span>

<span data-ttu-id="92b41-117">O esquema não oferece suporte ao seguinte diretamente (o que implica o comportamento de "fallback"):</span><span class="sxs-lookup"><span data-stu-id="92b41-117">The schema does not support the following directly (which imply the "fallback" behavior):</span></span>

-   <span data-ttu-id="92b41-118">Tipos básicos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="92b41-118">User defined basic types.</span></span>
-   <span data-ttu-id="92b41-119">Opções mais complicadas.</span><span class="sxs-lookup"><span data-stu-id="92b41-119">More complicated choices.</span></span>
-   <span data-ttu-id="92b41-120">Rejeitando atributos desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="92b41-120">Rejecting unknown attributes.</span></span>
-   <span data-ttu-id="92b41-121">Arredondar atributos desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="92b41-121">Round tripping unknown attributes.</span></span>
-   <span data-ttu-id="92b41-122">Suporte mais complicado para qualquer elemento.</span><span class="sxs-lookup"><span data-stu-id="92b41-122">More complicated support for any element.</span></span>
-   <span data-ttu-id="92b41-123">A construção all.</span><span class="sxs-lookup"><span data-stu-id="92b41-123">The all construct.</span></span>
-   <span data-ttu-id="92b41-124">Key/keyref.</span><span class="sxs-lookup"><span data-stu-id="92b41-124">Key/keyref.</span></span>

<span data-ttu-id="92b41-125">Veja a seguir uma análise detalhada do suporte a componentes de esquema diferentes.</span><span class="sxs-lookup"><span data-stu-id="92b41-125">Following is a detailed breakdown of different schema component support.</span></span> <span data-ttu-id="92b41-126">Ele é comparado com o contrato de dados no WCF porque a similaridade na funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="92b41-126">It is compared with data contract in WCF because the similarity in functionality.</span></span> <span data-ttu-id="92b41-127">A diferença será descrita.</span><span class="sxs-lookup"><span data-stu-id="92b41-127">The difference will be described.</span></span>

<span data-ttu-id="92b41-128">Em geral, para comportamentos de fallback:</span><span class="sxs-lookup"><span data-stu-id="92b41-128">Generally, for fallback behaviors:</span></span>

-   <span data-ttu-id="92b41-129">os atributos são submetidos a backup à \_ cadeia de caracteres WS;</span><span class="sxs-lookup"><span data-stu-id="92b41-129">attributes are fall backed to WS\_STRING;</span></span>
-   <span data-ttu-id="92b41-130">o conteúdo do elemento é submetido a backup no \_ buffer XML do WS \_ .</span><span class="sxs-lookup"><span data-stu-id="92b41-130">element content are fall backed to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="92b41-131">complexType é submetido a uma estrutura que contém um campo de \_ buffer XML do WS \_ .</span><span class="sxs-lookup"><span data-stu-id="92b41-131">complexType are fall backed to structure containing a field of WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="92b41-132">Os tipos simples são submetidos a backup à \_ cadeia de caracteres WS.</span><span class="sxs-lookup"><span data-stu-id="92b41-132">Simple types are fall backed to WS\_STRING.</span></span>

<span data-ttu-id="92b41-133">o Wsutil gera avisos para componentes de esquema que atualmente não têm suporte total.</span><span class="sxs-lookup"><span data-stu-id="92b41-133">wsutil generates warnings for schema components that are not currently fully supported.</span></span> <span data-ttu-id="92b41-134">O aplicativo pode precisar fazer uma verificação adicional para esses componentes são necessários.</span><span class="sxs-lookup"><span data-stu-id="92b41-134">Application might need to do additional verification for those components are needed.</span></span> <span data-ttu-id="92b41-135">O Wsutil de horas extras pode ser melhorado para lidar com alguns dos recursos que atualmente têm suporte no tempo de execução, como suporte a valor padrão.</span><span class="sxs-lookup"><span data-stu-id="92b41-135">Overtime wsutil can be improved to handle some of the features that are currently supported in runtime, like default value support.</span></span> <span data-ttu-id="92b41-136">o Wsutil também pode ser melhorado junto com a serialização para dar suporte a outros recursos, como o abstrato.</span><span class="sxs-lookup"><span data-stu-id="92b41-136">wsutil can also be improved together with serialization to support other features like abstract.</span></span> <span data-ttu-id="92b41-137">O número de componentes de esquema sem suporte pode ser reduzido ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="92b41-137">The number of unsupported schema components can be reduced over time.</span></span>

## <a name="the-overall-schema-document"></a><span data-ttu-id="92b41-138">O documento de esquema geral</span><span class="sxs-lookup"><span data-stu-id="92b41-138">The Overall Schema Document</span></span>

<span data-ttu-id="92b41-139">Definição global que pode afetar as definições inseridas no esquema.</span><span class="sxs-lookup"><span data-stu-id="92b41-139">Global definition that might affect embedded definitions in the schema.</span></span> <span data-ttu-id="92b41-140">Esses são atributos globais que são aplicáveis a todas as definições no esquema.</span><span class="sxs-lookup"><span data-stu-id="92b41-140">These are global attributes that are applicable to all definitions in the schema.</span></span>

<span data-ttu-id="92b41-141">Atributos de> de <xs: Schema</span><span class="sxs-lookup"><span data-stu-id="92b41-141"><xs:schema> attributes</span></span>

-   <span data-ttu-id="92b41-142">attributeFromDefault ignorado.</span><span class="sxs-lookup"><span data-stu-id="92b41-142">attributeFromDefault Ignored.</span></span>
-   <span data-ttu-id="92b41-143">blockDefault ignorado.</span><span class="sxs-lookup"><span data-stu-id="92b41-143">blockDefault Ignored.</span></span>
-   <span data-ttu-id="92b41-144">elementFormDefault ignorado.</span><span class="sxs-lookup"><span data-stu-id="92b41-144">elementFormDefault Ignored.</span></span> <span data-ttu-id="92b41-145">Isso é diferente do DataContract, pois elementos não qualificados têm suporte em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="92b41-145">This is different from dataContract as unqualified elements are supported in runtime.</span></span>
-   <span data-ttu-id="92b41-146">finalDefault ignorado.</span><span class="sxs-lookup"><span data-stu-id="92b41-146">finalDefault Ignored.</span></span> <span data-ttu-id="92b41-147">Não há nenhum suporte de linguagem C para o conceito de final.</span><span class="sxs-lookup"><span data-stu-id="92b41-147">There is no C language support for the concept of final.</span></span>
-   <span data-ttu-id="92b41-148">ID ignorada.</span><span class="sxs-lookup"><span data-stu-id="92b41-148">id Ignored.</span></span>
-   <span data-ttu-id="92b41-149">targetNamespace com suporte e mapeado para o namespace de serviço.</span><span class="sxs-lookup"><span data-stu-id="92b41-149">targetNamespace Supported and mapped to the service namespace.</span></span>
-   <span data-ttu-id="92b41-150">versão ignorada.</span><span class="sxs-lookup"><span data-stu-id="92b41-150">version Ignored.</span></span>

<span data-ttu-id="92b41-151"><xs: conteúdo do> do esquema</span><span class="sxs-lookup"><span data-stu-id="92b41-151"><xs:schema> contents</span></span>

-   <span data-ttu-id="92b41-152">incluir com suporte; Wsutil requer que toda a definição necessária esteja disponível como arquivos de entrada durante o tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="92b41-152">include Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="92b41-153">redefinição ignorada.</span><span class="sxs-lookup"><span data-stu-id="92b41-153">redefine Ignored.</span></span> <span data-ttu-id="92b41-154">Wsutil não dá suporte a isso.</span><span class="sxs-lookup"><span data-stu-id="92b41-154">wsutil does not support this.</span></span>
-   <span data-ttu-id="92b41-155">importação com suporte; Wsutil requer que toda a definição necessária esteja disponível como arquivos de entrada durante o tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="92b41-155">import Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="92b41-156">simpleType com suporte – consulte a seção de tipo simples abaixo.</span><span class="sxs-lookup"><span data-stu-id="92b41-156">simpleType Supported- see simple type section below.</span></span>
-   <span data-ttu-id="92b41-157">complexType com suporte-consulte a seção ' complexType '</span><span class="sxs-lookup"><span data-stu-id="92b41-157">complexType Supported- see 'complexType' section</span></span>
-   <span data-ttu-id="92b41-158">Grupo ignorado.</span><span class="sxs-lookup"><span data-stu-id="92b41-158">group Ignored.</span></span>
-   <span data-ttu-id="92b41-159">attributeGroup ignorado.</span><span class="sxs-lookup"><span data-stu-id="92b41-159">attributeGroup Ignored.</span></span>
-   <span data-ttu-id="92b41-160">elemento com suporte; mapeia para definições de elementos globais.</span><span class="sxs-lookup"><span data-stu-id="92b41-160">element Supported; maps to global element definitions.</span></span>
-   <span data-ttu-id="92b41-161">atributo com suporte; mapeia para definições de atributo globais.</span><span class="sxs-lookup"><span data-stu-id="92b41-161">attribute Supported; maps to global attribute definitions.</span></span>
-   <span data-ttu-id="92b41-162">notação ignorada</span><span class="sxs-lookup"><span data-stu-id="92b41-162">notation Ignored</span></span>

## <a name="complex-type"></a><span data-ttu-id="92b41-163">Tipo complexo</span><span class="sxs-lookup"><span data-stu-id="92b41-163">Complex Type</span></span>

<span data-ttu-id="92b41-164">O tipo complexo, representado por <xs: complexType>, poderia ser a restrição do tipo simples ou tipo complexo, extensão de tipo simples, matrizes ou estrutura.</span><span class="sxs-lookup"><span data-stu-id="92b41-164">Complex type, represented by <xs:complexType>, could be restriction of simple type or complex type, extension of simple type, arrays or structure.</span></span> <span data-ttu-id="92b41-165">Observado que, na extensão de tipos simples, não há nenhuma herança e nenhum suporte xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="92b41-165">Noticed that in extension of simple types, there is no inheritance and no xsi:type support.</span></span>

<span data-ttu-id="92b41-166">Atributos <xs: complexType></span><span class="sxs-lookup"><span data-stu-id="92b41-166"><xs:complexType> attributes</span></span>

-   <span data-ttu-id="92b41-167">Abstract gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-167">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-168">bloquear gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-168">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-169">final da geração de aviso sobre o recurso sem suporte, nenhuma alteração na criação de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-169">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-170">ID ignorada.</span><span class="sxs-lookup"><span data-stu-id="92b41-170">id Ignored.</span></span>
-   <span data-ttu-id="92b41-171">aviso de geração mista sobre recurso sem suporte, fallback para a estrutura com o buffer XML do WS, \_ \_ se for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="92b41-171">mixed Generate warning about unsupported feature, fallback to structure with WS\_XML\_BUFFER if true.</span></span>
-   <span data-ttu-id="92b41-172">nome com suporte e mapeado para o nome do tipo de estrutura.</span><span class="sxs-lookup"><span data-stu-id="92b41-172">name Supported and mapped to structure type name.</span></span>

<span data-ttu-id="92b41-173"><xs: complexType> conteúdo</span><span class="sxs-lookup"><span data-stu-id="92b41-173"><xs:complexType> contents</span></span>

<span data-ttu-id="92b41-174">Essa é a definição de tipo para estrutura.</span><span class="sxs-lookup"><span data-stu-id="92b41-174">This is type definition for structure.</span></span> <span data-ttu-id="92b41-175">Não há suporte para a restrição complexContent.</span><span class="sxs-lookup"><span data-stu-id="92b41-175">complexContent restriction is not supported.</span></span>

-   <span data-ttu-id="92b41-176">complexContent dá suporte à extensão de conteúdo complexo.</span><span class="sxs-lookup"><span data-stu-id="92b41-176">complexContent Support complex content extension.</span></span> <span data-ttu-id="92b41-177">Mapeia para a herança de estrutura.</span><span class="sxs-lookup"><span data-stu-id="92b41-177">Maps to structure inheritance.</span></span>
-   <span data-ttu-id="92b41-178">grupo de fallback no momento para a estrutura com o \_ campo de buffer XML do WS \_ .</span><span class="sxs-lookup"><span data-stu-id="92b41-178">group Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="92b41-179">Pode ter suporte de acordo com a partícula abaixo.</span><span class="sxs-lookup"><span data-stu-id="92b41-179">Can be supported according to the underneath particle.</span></span>
-   <span data-ttu-id="92b41-180">opção com suporte como Union.</span><span class="sxs-lookup"><span data-stu-id="92b41-180">choice supported as union.</span></span> <span data-ttu-id="92b41-181">Não há suporte para isso no contrato de dados.</span><span class="sxs-lookup"><span data-stu-id="92b41-181">This is not supported in data contract.</span></span>
-   <span data-ttu-id="92b41-182">sequência com suporte – mapeia para campos de uma estrutura</span><span class="sxs-lookup"><span data-stu-id="92b41-182">sequence Supported - maps to fields of a structure</span></span>
-   <span data-ttu-id="92b41-183">atributo com suporte com uma exceção de ' proibido '.</span><span class="sxs-lookup"><span data-stu-id="92b41-183">attribute supported with one exception of 'prohibited'.</span></span> <span data-ttu-id="92b41-184">fallback para a estrutura com o \_ buffer XML do WS \_ se ' proibido '.</span><span class="sxs-lookup"><span data-stu-id="92b41-184">fallback to structure with WS\_XML\_BUFFER if 'prohibited'.</span></span>
-   <span data-ttu-id="92b41-185">attributeGroup com suporte – mapeia para sequência de atributos</span><span class="sxs-lookup"><span data-stu-id="92b41-185">attributeGroup supported - maps to sequence of attributes</span></span>
-   <span data-ttu-id="92b41-186">anyAttribute ignorado</span><span class="sxs-lookup"><span data-stu-id="92b41-186">anyAttribute Ignored</span></span>
-   <span data-ttu-id="92b41-187">AttributeGroupRef com suporte – mapeia para sequência de atributos.</span><span class="sxs-lookup"><span data-stu-id="92b41-187">AttributeGroupRef Supported - maps to sequence of attributes.</span></span>
-   <span data-ttu-id="92b41-188">GroupRef atualmente, fallback para a estrutura com o \_ campo de buffer XML do WS \_ .</span><span class="sxs-lookup"><span data-stu-id="92b41-188">GroupRef Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="92b41-189">Pode ter suporte de acordo com o grupo abaixo.</span><span class="sxs-lookup"><span data-stu-id="92b41-189">Can be supported according to the underneath group.</span></span>
-   <span data-ttu-id="92b41-190">Qualquer suporte, mapeia para o \_ buffer XML</span><span class="sxs-lookup"><span data-stu-id="92b41-190">Any Supported, maps to XML\_BUFFER</span></span>
-   <span data-ttu-id="92b41-191">(em branco) mapa com suporte para uma descrição de struct vazia sem struct gerado.</span><span class="sxs-lookup"><span data-stu-id="92b41-191">(blank) supported map to empty struct description with no struct generated.</span></span>

<span data-ttu-id="92b41-192"><xs: Sequence> em um tipo complexo: Contents</span><span class="sxs-lookup"><span data-stu-id="92b41-192"><xs:sequence> in a complex type: contents</span></span>

<span data-ttu-id="92b41-193">Wsutil só dá suporte total à sequência de minOccurs = 1 e maxOccurs = 1; caso contrário, o tipo complexo é submetido a backup no \_ buffer XML do WS \_ .</span><span class="sxs-lookup"><span data-stu-id="92b41-193">wsutil only fully support sequence of minOccurs = 1 and maxOccurs = 1; otherwise the complex type is currently fall backed to WS\_XML\_BUFFER.</span></span> <span data-ttu-id="92b41-194">Ele pode ter suporte como uma matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="92b41-194">It can be supported as array of structures.</span></span>

-   <span data-ttu-id="92b41-195">elemento com suporte; cada instância é mapeada para um campo na estrutura.</span><span class="sxs-lookup"><span data-stu-id="92b41-195">element Supported; each instance maps to a field in the structure.</span></span>
-   <span data-ttu-id="92b41-196">Fallback de grupo; o complexType é fallback para o \_ buffer XML do WS \_ .</span><span class="sxs-lookup"><span data-stu-id="92b41-196">Group fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="92b41-197">Todos os fallbacks; o complexType é fallback para o \_ buffer XML do WS \_ .</span><span class="sxs-lookup"><span data-stu-id="92b41-197">All fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="92b41-198">opção com suporte; mapear para o campo Union.</span><span class="sxs-lookup"><span data-stu-id="92b41-198">choice supported; map to union field.</span></span>
-   <span data-ttu-id="92b41-199">fallback de sequência; o complexType é fallback para o \_ buffer XML do WS \_ .</span><span class="sxs-lookup"><span data-stu-id="92b41-199">sequence fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="92b41-200">qualquer suporte; mapeado para o \_ buffer XML.</span><span class="sxs-lookup"><span data-stu-id="92b41-200">any Supported; mapped to XML\_BUFFER.</span></span>
-   <span data-ttu-id="92b41-201">(em branco) com suporte; complexType pode ser uma estrutura vazia se não houver nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="92b41-201">(blank) supported; complexType can be an empty structure if there is no attributes.</span></span>

## <a name="elements"></a><span data-ttu-id="92b41-202">Elementos</span><span class="sxs-lookup"><span data-stu-id="92b41-202">Elements</span></span>

<span data-ttu-id="92b41-203"><xs: Element>pode ocorrer em três contextos.</span><span class="sxs-lookup"><span data-stu-id="92b41-203"><xs:element>may occur in three contexts.</span></span>

-   <span data-ttu-id="92b41-204">Pode ocorrer dentro de um <xs: Sequence>, descrevendo um campo de uma estrutura regular.</span><span class="sxs-lookup"><span data-stu-id="92b41-204">It may occur within an <xs:sequence>, describing a field of a regular struct.</span></span> <span data-ttu-id="92b41-205">Nesse caso, o atributo maxOccurs deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="92b41-205">In this case, the maxOccurs attribute must be 1.</span></span> <span data-ttu-id="92b41-206">O campo será opcional se minOccurs for 0.</span><span class="sxs-lookup"><span data-stu-id="92b41-206">The field is optional if minOccurs is 0.</span></span>
-   <span data-ttu-id="92b41-207">Pode ocorrer dentro de um <xs: Sequence>, descrevendo um campo de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="92b41-207">It may occur within an <xs:sequence>, describing a field of an array.</span></span> <span data-ttu-id="92b41-208">Nesse caso, o atributo maxOccurs deve ser maior que 1 ou ' unbounded '.</span><span class="sxs-lookup"><span data-stu-id="92b41-208">In this case, the maxOccurs attribute must be greater than 1 or 'unbounded'.</span></span>
-   <span data-ttu-id="92b41-209">Pode ocorrer dentro de um <xs: Schema> como uma descrição de elemento global.</span><span class="sxs-lookup"><span data-stu-id="92b41-209">It may occur within an <xs:schema> as a global element description.</span></span>

<span data-ttu-id="92b41-210"><xs: Element> em um <xs: Sequence> ou <xs: Choice> como um campo em uma estrutura</span><span class="sxs-lookup"><span data-stu-id="92b41-210"><xs:element> within an <xs:sequence> or <xs:choice> as a field in a structure</span></span>

-   <span data-ttu-id="92b41-211">referência com suporte; resolvido para referência ao elemento global.</span><span class="sxs-lookup"><span data-stu-id="92b41-211">ref Supported; resolved to reference to global element.</span></span>
-   <span data-ttu-id="92b41-212">nome com suporte, mapeado para o nome do campo.</span><span class="sxs-lookup"><span data-stu-id="92b41-212">name Supported, maps to field name.</span></span>
-   <span data-ttu-id="92b41-213">tipo com suporte, é mapeado para o tipo de campo.</span><span class="sxs-lookup"><span data-stu-id="92b41-213">type Supported, maps to field type.</span></span> <span data-ttu-id="92b41-214">Para obter mais informações, consulte ' mapeamento de tipo '.</span><span class="sxs-lookup"><span data-stu-id="92b41-214">For more information, see 'Type Mapping'.</span></span> <span data-ttu-id="92b41-215">Se não for especificado (e o elemento não contiver um tipo anônimo), xs: anyType será assumido.</span><span class="sxs-lookup"><span data-stu-id="92b41-215">If not specified (and the element does not contain an anonymous type), xs:anyType is assumed.</span></span>
-   <span data-ttu-id="92b41-216">bloquear gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-216">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-217">padrão gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-217">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-218">correção de aviso de geração de recurso sem suporte, nenhuma alteração na criação de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-218">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-219">formulário ignorado.</span><span class="sxs-lookup"><span data-stu-id="92b41-219">form Ignored.</span></span> <span data-ttu-id="92b41-220">Nossa camada de serialização dá suporte a formulários qualificados e não qualificados.</span><span class="sxs-lookup"><span data-stu-id="92b41-220">Our serialization layer supports both qualified and unqualified forms.</span></span>
-   <span data-ttu-id="92b41-221">ID ignorada.</span><span class="sxs-lookup"><span data-stu-id="92b41-221">id Ignored.</span></span>
-   <span data-ttu-id="92b41-222">maxOccurs é mapeado para um único campo de dados se for igual a 1.</span><span class="sxs-lookup"><span data-stu-id="92b41-222">maxOccurs maps to a single data field if equals 1.</span></span> <span data-ttu-id="92b41-223">Ele será mapeado para um campo de matriz (elemento repetitivo) se maxOccurs for maior que 1.</span><span class="sxs-lookup"><span data-stu-id="92b41-223">it is mapped to an array field (repeating element) if maxOccurs is larger than 1.</span></span>
-   <span data-ttu-id="92b41-224">minOccurs se for 0, as opções de campo serão definidas como campo \_ opcional, se anulável não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="92b41-224">minOccurs if 0, the field options is set to FIELD\_OPTIONAL, if nillable is not set.</span></span>
-   <span data-ttu-id="92b41-225">anulável o campo é anulável.</span><span class="sxs-lookup"><span data-stu-id="92b41-225">nillable The field is nillable.</span></span> <span data-ttu-id="92b41-226">Consulte [serialização](serialization.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="92b41-226">See [Serialization](serialization.md) for more detail.</span></span>

<span data-ttu-id="92b41-227"><xs: Element> como elemento global: Attributes</span><span class="sxs-lookup"><span data-stu-id="92b41-227"><xs:element> as global element: attributes</span></span>

<span data-ttu-id="92b41-228">os atributos minOccurs e maxOccurs são inválidos como descrição do elemento global.</span><span class="sxs-lookup"><span data-stu-id="92b41-228">minOccurs and maxOccurs attributes are invalid as global element description.</span></span> <span data-ttu-id="92b41-229">O aplicativo pode usar a descrição do elemento gerado na camada de serialização ou nas camadas de canal diretamente.</span><span class="sxs-lookup"><span data-stu-id="92b41-229">Application can use generated element description in serialization layer or channel layers directly.</span></span>

-   <span data-ttu-id="92b41-230">Abstract gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-230">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-231">bloquear gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-231">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-232">padrão gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-232">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-233">final da geração de aviso sobre o recurso sem suporte, nenhuma alteração na criação de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-233">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-234">correção de aviso de geração de recurso sem suporte, nenhuma alteração na criação de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-234">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-235">ID ignorada.</span><span class="sxs-lookup"><span data-stu-id="92b41-235">id Ignored.</span></span>
-   <span data-ttu-id="92b41-236">nome com suporte – mapeie para o nome da descrição do elemento global e é a base para o tipo anônimo quando especificado.</span><span class="sxs-lookup"><span data-stu-id="92b41-236">name Supported- map to name of the global element description, and it is the base for the anonymous type when specified.</span></span>
-   <span data-ttu-id="92b41-237">anulável ignorado-o aplicativo precisa chamar com o sinalizador direito.</span><span class="sxs-lookup"><span data-stu-id="92b41-237">nillable Ignored-application needs to call with right flag.</span></span>
-   <span data-ttu-id="92b41-238">fallback do grupo de substituição para a estrutura com o buffer XML do WS, \_ \_ se definido.</span><span class="sxs-lookup"><span data-stu-id="92b41-238">substitutionGroup fallback to structure with WS\_XML\_BUFFER if set.</span></span> <span data-ttu-id="92b41-239">Wsutil não oferece suporte a Substitution.</span><span class="sxs-lookup"><span data-stu-id="92b41-239">wsutil does not support substitutionGroup.</span></span>
-   <span data-ttu-id="92b41-240">tipo com suporte e mapear para o tipo do elemento.</span><span class="sxs-lookup"><span data-stu-id="92b41-240">type Supported and map to the type of the element.</span></span>

<span data-ttu-id="92b41-241"><xs: Element> como elemento global: Contents</span><span class="sxs-lookup"><span data-stu-id="92b41-241"><xs:element> as global element: contents</span></span>

-   <span data-ttu-id="92b41-242">simpleType com suporte; mapeia para definição de tipo.</span><span class="sxs-lookup"><span data-stu-id="92b41-242">simpleType Supported; maps to type definition.</span></span>
-   <span data-ttu-id="92b41-243">complexType com suporte; mapeia para um tipo complexo.</span><span class="sxs-lookup"><span data-stu-id="92b41-243">complexType supported; maps to a complex type.</span></span>
-   <span data-ttu-id="92b41-244">aviso de geração exclusiva sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-244">unique Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="92b41-245">Wsutil não dá suporte a restrições de elemento.</span><span class="sxs-lookup"><span data-stu-id="92b41-245">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="92b41-246">chave de geração de aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-246">key Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="92b41-247">Wsutil não dá suporte a restrições de elemento.</span><span class="sxs-lookup"><span data-stu-id="92b41-247">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="92b41-248">keyref gera um aviso sobre o recurso sem suporte; nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-248">keyref Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="92b41-249">Wsutil não dá suporte a restrições de elemento.</span><span class="sxs-lookup"><span data-stu-id="92b41-249">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="92b41-250">ficará Porta o elemento sem nenhuma especificação de tipo é tratado como xs: anyType.</span><span class="sxs-lookup"><span data-stu-id="92b41-250">(blank) Supported; element with no type specification is treated as xs:anyType.</span></span>

## <a name="simple-types"></a><span data-ttu-id="92b41-251">Tipos simples</span><span class="sxs-lookup"><span data-stu-id="92b41-251">Simple Types</span></span>

<span data-ttu-id="92b41-252">Atributos <xs: simpleType></span><span class="sxs-lookup"><span data-stu-id="92b41-252"><xs:simpleType> attributes</span></span>

-   <span data-ttu-id="92b41-253">Final da geração de aviso sobre o recurso sem suporte, nenhuma alteração na criação de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-253">Final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-254">ID ignorada</span><span class="sxs-lookup"><span data-stu-id="92b41-254">Id Ignored</span></span>
-   <span data-ttu-id="92b41-255">Nome com suporte, mapeado para o nome do tipo.</span><span class="sxs-lookup"><span data-stu-id="92b41-255">Name Supported, maps to type name.</span></span>

<span data-ttu-id="92b41-256"><xs: simpleType> conteúdo</span><span class="sxs-lookup"><span data-stu-id="92b41-256"><xs:simpleType> contents</span></span>

-   <span data-ttu-id="92b41-257">Restrição com suporte, é mapeada para o tipo ou intervalo de enumeração.</span><span class="sxs-lookup"><span data-stu-id="92b41-257">Restriction Supported, maps to enum type or range.</span></span> <span data-ttu-id="92b41-258">Consulte a seção "xs: simpleType Restrictions".</span><span class="sxs-lookup"><span data-stu-id="92b41-258">See "xs:simpleType restrictions" section.</span></span>
-   <span data-ttu-id="92b41-259">Lista gerar aviso sobre o recurso sem suporte, fallback para o \_ buffer XML.</span><span class="sxs-lookup"><span data-stu-id="92b41-259">List Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>
-   <span data-ttu-id="92b41-260">União gere um aviso sobre o recurso sem suporte, fallback para o \_ buffer XML.</span><span class="sxs-lookup"><span data-stu-id="92b41-260">Union Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>

## <a name="simple-type-restriction"></a><span data-ttu-id="92b41-261">Restrição de tipo simples</span><span class="sxs-lookup"><span data-stu-id="92b41-261">Simple Type restriction</span></span>

<span data-ttu-id="92b41-262">Determinadas facetas são permitidas em tipos integrais e tipo de cadeias de caracteres para permitir suporte a intervalo e enumeração.</span><span class="sxs-lookup"><span data-stu-id="92b41-262">Certain facets are allowed in integral types and strings type to allow range and enum support.</span></span>

<span data-ttu-id="92b41-263">suporte à enumeração</span><span class="sxs-lookup"><span data-stu-id="92b41-263">enumeration support</span></span>

<span data-ttu-id="92b41-264"><xs: Enumeration> restrição de tipo simples para o tipo base da cadeia de caracteres é tratada como tipo enum.</span><span class="sxs-lookup"><span data-stu-id="92b41-264"><xs:enumeration> simple type restriction for base type of string is treated as enum type.</span></span> <span data-ttu-id="92b41-265">Nesse caso, o atributo base deve ser do tipo cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="92b41-265">In this case, the Base attribute MUST be string type.</span></span> <span data-ttu-id="92b41-266">Em caso de enumeração, todas as outras facetas são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="92b41-266">In enumeration case, all other facets are ignored.</span></span>

<span data-ttu-id="92b41-267">intervalo no suporte de tipo simples</span><span class="sxs-lookup"><span data-stu-id="92b41-267">range on simple type support</span></span>

<span data-ttu-id="92b41-268">Algumas facetas são suportadas em tipos simples dão suporte a um intervalo efetivamente permitido no tipo.</span><span class="sxs-lookup"><span data-stu-id="92b41-268">Some facets are support in simple types support effectively range allowed on the type.</span></span> <span data-ttu-id="92b41-269">A seguir estão restrições para tipos integrais e tipos float/double.</span><span class="sxs-lookup"><span data-stu-id="92b41-269">Following are restriction for integral types and float/double types.</span></span> <span data-ttu-id="92b41-270">Tipos simples com outras facetas são submetidos a backup para o \_ tipo de cadeia de caracteres WS</span><span class="sxs-lookup"><span data-stu-id="92b41-270">Simple types with other facets are fall backed to WS\_STRING type</span></span>

-   <span data-ttu-id="92b41-271">Suporte para minExclusive</span><span class="sxs-lookup"><span data-stu-id="92b41-271">minExclusive Supported</span></span>
-   <span data-ttu-id="92b41-272">minInclusive com suporte</span><span class="sxs-lookup"><span data-stu-id="92b41-272">minInclusive Supported</span></span>
-   <span data-ttu-id="92b41-273">maxExclusive com suporte</span><span class="sxs-lookup"><span data-stu-id="92b41-273">maxExclusive Supported</span></span>
-   <span data-ttu-id="92b41-274">maxInclusive com suporte</span><span class="sxs-lookup"><span data-stu-id="92b41-274">maxInclusive Supported</span></span>
-   <span data-ttu-id="92b41-275">totalDigits gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-275">totalDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-276">fractionDigits gere aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-276">fractionDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-277">comprimento gera um aviso sobre o recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-277">length Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-278">minLength gera um aviso sobre o recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-278">minLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-279">maxLength gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-279">maxLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-280">a enumeração gera um aviso sobre o recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-280">enumeration Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-281">Espaço em branco gera aviso sobre recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-281">whiteSpace Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-282">padrão gera um aviso sobre o recurso sem suporte, nenhuma alteração na geração de código.</span><span class="sxs-lookup"><span data-stu-id="92b41-282">pattern Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="92b41-283">ficará Porta.</span><span class="sxs-lookup"><span data-stu-id="92b41-283">(blank) Supported.</span></span>

<span data-ttu-id="92b41-284">Não há suporte para minLength e maxLength na cadeia de caracteres no momento, mas é um recurso desejável para dar suporte ao.</span><span class="sxs-lookup"><span data-stu-id="92b41-284">minLength and maxLength on string is not supported currently but is a desirable feature to support.</span></span>

## <a name="inheritance"></a><span data-ttu-id="92b41-285">Herança</span><span class="sxs-lookup"><span data-stu-id="92b41-285">Inheritance</span></span>

<span data-ttu-id="92b41-286">O Wsutil dá suporte à herança de tipos complexos, ou seja, uma estrutura pode herdar de outra estrutura, semelhante à herança de interface em C++.</span><span class="sxs-lookup"><span data-stu-id="92b41-286">Wsutil supports inheritance of complex types, that is, a structure can inherit from another structure, similar to interface inheritance in C++.</span></span> <span data-ttu-id="92b41-287">Isso é feito por meio do <xs: complexContentExtension>.</span><span class="sxs-lookup"><span data-stu-id="92b41-287">This is done through <xs:complexContentExtension>.</span></span> <span data-ttu-id="92b41-288"><há suporte para o> xs: simpleContentExtension, mas é gerado como uma estrutura simples com o tipo base como primeiro campo, em vez de herança de tipo.</span><span class="sxs-lookup"><span data-stu-id="92b41-288"><xs:simpleContentExtension> is supported but is generated as plain structure with base type as first field instead of type inheritance.</span></span>

## <a name="typeprimitive-mapping"></a><span data-ttu-id="92b41-289">Mapeamento de tipo/primitivo</span><span class="sxs-lookup"><span data-stu-id="92b41-289">Type/primitive mapping</span></span>

<span data-ttu-id="92b41-290">Os identificadores precisam ser normalizados ao converter de NCNames em XML.</span><span class="sxs-lookup"><span data-stu-id="92b41-290">Identifiers needs to be normalized when translating from NCNames in XML.</span></span> <span data-ttu-id="92b41-291">Cadeias de caracteres são anuláveis; os tipos de ponteiro são anuláveis; tipos integrais e float/double são anuláveis e defaultValue é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="92b41-291">Strings are nillable; pointer types are nillable; integral types and float/double are nillable and defaultValue is set to 0.</span></span>

![Tabela mostrando o mapeamento entre tipos XSD e tipos de dados Sapphire.](images/schematypemap.png)

 

 




