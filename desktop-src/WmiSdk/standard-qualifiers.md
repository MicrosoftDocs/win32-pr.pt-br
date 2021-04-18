---
description: Todas as implementações em conformidade com o CIM devem lidar com um conjunto padrão de qualificadores.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Qualificadores padrão
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814120"
---
# <a name="standard-qualifiers"></a><span data-ttu-id="48880-103">Qualificadores padrão</span><span class="sxs-lookup"><span data-stu-id="48880-103">Standard Qualifiers</span></span>

<span data-ttu-id="48880-104">Todas as implementações em conformidade com o CIM devem lidar com um conjunto padrão de qualificadores.</span><span class="sxs-lookup"><span data-stu-id="48880-104">All CIM-compliant implementations must handle a standard set of qualifiers.</span></span> <span data-ttu-id="48880-105">Qualquer objeto específico não tem todos os qualificadores listados.</span><span class="sxs-lookup"><span data-stu-id="48880-105">Any specific object does not have all of the qualifiers listed.</span></span> <span data-ttu-id="48880-106">Normalmente, as classes de extensão fornecem qualificadores adicionais para facilitar o provisionamento de instâncias de classe e outras operações na classe.</span><span class="sxs-lookup"><span data-stu-id="48880-106">Usually, extension classes supply additional qualifiers to facilitate provision of class instances and other operations on the class.</span></span>

<span data-ttu-id="48880-107">É responsabilidade do provedor impor os qualificadores.</span><span class="sxs-lookup"><span data-stu-id="48880-107">It is the responsibility of the provider to enforce the qualifiers.</span></span> <span data-ttu-id="48880-108">O WMI não impõe qualificadores, mas os usa apenas para informar ao usuário sobre como a propriedade é usada.</span><span class="sxs-lookup"><span data-stu-id="48880-108">WMI does not enforce qualifiers, but uses them only to inform the user about how the property is used.</span></span>

> [!Note]  
> <span data-ttu-id="48880-109">O WMI é compatível com a especificação CIM 2,5.</span><span class="sxs-lookup"><span data-stu-id="48880-109">WMI is compliant with the CIM 2.5 specification.</span></span>

 

<span data-ttu-id="48880-110">Os qualificadores têm as seguintes limitações:</span><span class="sxs-lookup"><span data-stu-id="48880-110">Qualifiers have the following limitations:</span></span>

-   <span data-ttu-id="48880-111">Nem todos os qualificadores padrão podem ser usados juntos.</span><span class="sxs-lookup"><span data-stu-id="48880-111">Not all standard qualifiers can be used together.</span></span>
-   <span data-ttu-id="48880-112">Nem todos os qualificadores podem ser aplicados a todas as construções, como associação ou referência.</span><span class="sxs-lookup"><span data-stu-id="48880-112">Not all qualifiers can be applied to all constructs, such as association or reference.</span></span> <span data-ttu-id="48880-113">Essas limitações são identificadas na lista aplica-se a.</span><span class="sxs-lookup"><span data-stu-id="48880-113">These limitations are identified in the Applies to list.</span></span>
-   <span data-ttu-id="48880-114">Para um constructo específico, como associação ou referência, o uso dos qualificadores legais pode ser mais restrito porque alguns qualificadores são mutuamente exclusivos, o uso de um qualificador pode implicar algumas restrições no valor de outro e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="48880-114">For a particular construct, such as association or reference, the use of the legal qualifiers can be further constrained because some qualifiers are mutually exclusive, the use of one qualifier may imply some restrictions on the value of another, and so on.</span></span> <span data-ttu-id="48880-115">Essas regras de uso estão documentadas.</span><span class="sxs-lookup"><span data-stu-id="48880-115">These usage rules are documented.</span></span>
-   <span data-ttu-id="48880-116">Os qualificadores legais são herdados por entidades como propriedades, métodos, instâncias ou subclasses somente, não por associações ou referências.</span><span class="sxs-lookup"><span data-stu-id="48880-116">Legal qualifiers are inherited by entities such as properties, methods, instances, or subclasses only, not by associations or references.</span></span> <span data-ttu-id="48880-117">Por exemplo, o qualificador **maxlen** que se aplica a propriedades não é herdado por referências.</span><span class="sxs-lookup"><span data-stu-id="48880-117">For example, the **MaxLen** qualifier that applies to properties is not inherited by references.</span></span>

<span data-ttu-id="48880-118">O a seguir lista os qualificadores padrão do WMI.</span><span class="sxs-lookup"><span data-stu-id="48880-118">The following lists WMI standard qualifiers.</span></span>

<dt>

<span data-ttu-id="48880-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Resume**</span><span class="sxs-lookup"><span data-stu-id="48880-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstract**</span></span>
</dt> <dd>

<span data-ttu-id="48880-120">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-120">Data type: **boolean**</span></span>

<span data-ttu-id="48880-121">Aplica-se a: classes, associações, indicações</span><span class="sxs-lookup"><span data-stu-id="48880-121">Applies to: classes, associations, indications</span></span>

<span data-ttu-id="48880-122">Indica se a classe é abstrata e serve apenas como base para novas classes.</span><span class="sxs-lookup"><span data-stu-id="48880-122">Indicates whether the class is abstract and serves only as a base for new classes.</span></span> <span data-ttu-id="48880-123">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-123">The default is **FALSE**.</span></span> <span data-ttu-id="48880-124">Você não pode criar instâncias de classes abstratas.</span><span class="sxs-lookup"><span data-stu-id="48880-124">You cannot create instances of abstract classes.</span></span> <span data-ttu-id="48880-125">A ausência desse qualificador indica que a classe não é abstrata; Portanto, esse qualificador é necessário para todas as classes abstratas.</span><span class="sxs-lookup"><span data-stu-id="48880-125">The absence of this qualifier indicates that the class is not abstract; therefore, this qualifier is required for all abstract classes.</span></span>

</dd> <dt>

<span data-ttu-id="48880-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Tais**</span><span class="sxs-lookup"><span data-stu-id="48880-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Aggregate**</span></span>
</dt> <dd>

<span data-ttu-id="48880-127">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-127">Data type: **boolean**</span></span>

<span data-ttu-id="48880-128">Aplica-se a: referências</span><span class="sxs-lookup"><span data-stu-id="48880-128">Applies to: references</span></span>

<span data-ttu-id="48880-129">Indica se a referência é o componente pai de uma associação de agregação.</span><span class="sxs-lookup"><span data-stu-id="48880-129">Indicates whether the reference is the parent component of an aggregation association.</span></span> <span data-ttu-id="48880-130">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-130">The default is **FALSE**.</span></span>

<span data-ttu-id="48880-131">Uso: a **agregação e os** qualificadores de **agregação** são usados em conjunto com a   **agregação** qualifica a associação, e a **agregação** especifica a referência pai.</span><span class="sxs-lookup"><span data-stu-id="48880-131">Usage: The **Aggregation** and **Aggregate** qualifiers are used together   **Aggregation** qualifies the association, and **Aggregate** specifies the parent reference.</span></span>

</dd> <dt>

<span data-ttu-id="48880-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregation**</span><span class="sxs-lookup"><span data-stu-id="48880-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="48880-133">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-133">Data type: **boolean**</span></span>

<span data-ttu-id="48880-134">Aplica-se a: associações</span><span class="sxs-lookup"><span data-stu-id="48880-134">Applies to: associations</span></span>

<span data-ttu-id="48880-135">Indica se a associação é uma agregação.</span><span class="sxs-lookup"><span data-stu-id="48880-135">Indicates whether the association is an aggregation.</span></span> <span data-ttu-id="48880-136">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-136">The default is **FALSE**.</span></span> <span data-ttu-id="48880-137">Usado com **Aggregate**.</span><span class="sxs-lookup"><span data-stu-id="48880-137">Used with **Aggregate**.</span></span> <span data-ttu-id="48880-138">Esse qualificador é necessário para todas as associações de agregação.</span><span class="sxs-lookup"><span data-stu-id="48880-138">This qualifier is required for all aggregation associations.</span></span>

</dd> <dt>

<span data-ttu-id="48880-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Receber**</span><span class="sxs-lookup"><span data-stu-id="48880-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**</span></span>
</dt> <dd>

<span data-ttu-id="48880-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-140">Data type: **string**</span></span>

<span data-ttu-id="48880-141">Aplica-se a: Propriedades, referências, métodos</span><span class="sxs-lookup"><span data-stu-id="48880-141">Applies to: properties, references, methods</span></span>

<span data-ttu-id="48880-142">Nome alternativo para uma propriedade ou um método no esquema.</span><span class="sxs-lookup"><span data-stu-id="48880-142">Alternate name for a property or method in the schema.</span></span> <span data-ttu-id="48880-143">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-143">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span><span class="sxs-lookup"><span data-stu-id="48880-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span></span>
</dt> <dd>

<span data-ttu-id="48880-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-145">Data type: **string**</span></span>

<span data-ttu-id="48880-146">Aplica-se a: Propriedades, parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-146">Applies to: properties, parameters</span></span>

<span data-ttu-id="48880-147">Tipo da matriz qualificada.</span><span class="sxs-lookup"><span data-stu-id="48880-147">Type of the qualified array.</span></span>

<span data-ttu-id="48880-148">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="48880-148">Valid values are:</span></span>

-   <span data-ttu-id="48880-149">recipiente (padrão)</span><span class="sxs-lookup"><span data-stu-id="48880-149">bag (default)</span></span>
-   <span data-ttu-id="48880-150">indexado</span><span class="sxs-lookup"><span data-stu-id="48880-150">indexed</span></span>
-   <span data-ttu-id="48880-151">ordered</span><span class="sxs-lookup"><span data-stu-id="48880-151">ordered</span></span>

<span data-ttu-id="48880-152">Uso: aplique este tipo de qualificador somente a propriedades e parâmetros que são matrizes (definidas usando a sintaxe de colchete).</span><span class="sxs-lookup"><span data-stu-id="48880-152">Usage: Apply this type of qualifier only to properties and parameters that are arrays (defined by using bracket syntax).</span></span>

</dd> <dt>

<span data-ttu-id="48880-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**BitMap**</span><span class="sxs-lookup"><span data-stu-id="48880-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**BitMap**</span></span>
</dt> <dd>

<span data-ttu-id="48880-154">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-154">Data type: **string array**</span></span>

<span data-ttu-id="48880-155">Aplica-se a: Propriedades, métodos, parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-155">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="48880-156">Mapa de posições de bits significativas em que cada posição significativa pode ser "ativada" ou "desativada".</span><span class="sxs-lookup"><span data-stu-id="48880-156">Map of significant bit positions where each significant position can be "on" or "off".</span></span> <span data-ttu-id="48880-157">Cada bit "on" é mapeado para um valor correspondente na matriz **Bitvalues** .</span><span class="sxs-lookup"><span data-stu-id="48880-157">Each "on" bit maps to a corresponding value in the **BitValues** array.</span></span> <span data-ttu-id="48880-158">Com vários bits "on", vários valores simultâneos na matriz **Bitvalues** são indicados.</span><span class="sxs-lookup"><span data-stu-id="48880-158">By having multiple bits "on", multiple concurrent values in the **BitValues** array are indicated.</span></span> <span data-ttu-id="48880-159">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-159">The default is **NULL**.</span></span>

<span data-ttu-id="48880-160">Para obter mais informações, consulte [bitmap e Bitvalues](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="48880-160">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="48880-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**Bitvalues**</span><span class="sxs-lookup"><span data-stu-id="48880-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**</span></span>
</dt> <dd>

<span data-ttu-id="48880-162">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-162">Data type: **string array**</span></span>

<span data-ttu-id="48880-163">Aplica-se a: Propriedades, métodos, parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-163">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="48880-164">Tradução de um valor de posição de bits em uma **cadeia de caracteres** associada.</span><span class="sxs-lookup"><span data-stu-id="48880-164">Translation of a bit position value into an associated **string**.</span></span> <span data-ttu-id="48880-165">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-165">The default is **NULL**.</span></span>

<span data-ttu-id="48880-166">Para obter mais informações, consulte [bitmap e Bitvalues](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="48880-166">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="48880-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Qu**</span><span class="sxs-lookup"><span data-stu-id="48880-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructor**</span></span>
</dt> <dd>

<span data-ttu-id="48880-168">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-168">Data type: **boolean**</span></span>

<span data-ttu-id="48880-169">Aplica-se a: métodos</span><span class="sxs-lookup"><span data-stu-id="48880-169">Applies to: methods</span></span>

<span data-ttu-id="48880-170">Indica se o método cria instâncias.</span><span class="sxs-lookup"><span data-stu-id="48880-170">Indicates whether the method creates instances.</span></span> <span data-ttu-id="48880-171">Esses métodos não são restritos a atuar em uma única instância ou em uma única classe.</span><span class="sxs-lookup"><span data-stu-id="48880-171">These methods are not constrained to acting on a single instance or a single class.</span></span> <span data-ttu-id="48880-172">Por exemplo, um construtor pode criar instâncias de associação, bem como instâncias da classe que define o construtor.</span><span class="sxs-lookup"><span data-stu-id="48880-172">For example, a constructor can create association instances as well as instances of the class that defines the constructor.</span></span>

<span data-ttu-id="48880-173">O qualificador de **Construtor** destina-se apenas a informações e não é esperado que ele seja acionado pelo Gerenciador de objetos.</span><span class="sxs-lookup"><span data-stu-id="48880-173">The **Constructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="48880-174">O Gerenciador de objetos não precisa chamar métodos de Construtor quando um objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="48880-174">The object manager does not have to call constructor methods when an object is created.</span></span> <span data-ttu-id="48880-175">Além disso, quando um construtor é chamado, o Gerenciador de objetos não precisa invocar nenhum método de Construtor definido para qualquer classe pai da classe original.</span><span class="sxs-lookup"><span data-stu-id="48880-175">Also when a constructor is called, the object manager does not have to invoke any constructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="48880-176">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-176">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span><span class="sxs-lookup"><span data-stu-id="48880-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span></span>
</dt> <dd>

<span data-ttu-id="48880-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-178">Data type: **string**</span></span>

<span data-ttu-id="48880-179">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="48880-179">Applies to: classes</span></span>

<span data-ttu-id="48880-180">Nome do método pelo qual as instâncias dessa classe são criadas.</span><span class="sxs-lookup"><span data-stu-id="48880-180">Name of the method by which instances of this class are created.</span></span> <span data-ttu-id="48880-181">O valor é "PutInstance" ou o nome de outro método que cria as instâncias.</span><span class="sxs-lookup"><span data-stu-id="48880-181">The value is either "PutInstance" or the name of another method that creates the instances.</span></span> <span data-ttu-id="48880-182">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-182">The default is **NULL**.</span></span>

<span data-ttu-id="48880-183">Uso: esse qualificador só poderá ser usado se o qualificador **SupportsCreate** estiver presente.</span><span class="sxs-lookup"><span data-stu-id="48880-183">Usage: This qualifier can only be used if the **SupportsCreate** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="48880-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span><span class="sxs-lookup"><span data-stu-id="48880-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span></span>
</dt> <dd>

<span data-ttu-id="48880-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-185">Data type: **string**</span></span>

<span data-ttu-id="48880-186">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="48880-186">Applies to: classes</span></span>

<span data-ttu-id="48880-187">Nome do método pelo qual as instâncias dessa classe são excluídas.</span><span class="sxs-lookup"><span data-stu-id="48880-187">Name of the method by which instances of this class are deleted.</span></span> <span data-ttu-id="48880-188">O valor é "DeleteInstance" ou o nome de outro método que exclui as instâncias.</span><span class="sxs-lookup"><span data-stu-id="48880-188">The value is either "DeleteInstance", or the name of another method that deletes the instances.</span></span> <span data-ttu-id="48880-189">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-189">The default is **NULL**.</span></span>

<span data-ttu-id="48880-190">Uso: esse qualificador só poderá ser usado se o qualificador **SupportsDelete** estiver presente.</span><span class="sxs-lookup"><span data-stu-id="48880-190">Usage: This qualifier can only be used if the **SupportsDelete** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="48880-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="48880-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="48880-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-192">Data type: **string**</span></span>

<span data-ttu-id="48880-193">Aplica-se a: qualquer</span><span class="sxs-lookup"><span data-stu-id="48880-193">Applies to: any</span></span>

<span data-ttu-id="48880-194">Descrição de um elemento nomeado.</span><span class="sxs-lookup"><span data-stu-id="48880-194">Description of a named element.</span></span> <span data-ttu-id="48880-195">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-195">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destruidor**</span><span class="sxs-lookup"><span data-stu-id="48880-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructor**</span></span>
</dt> <dd>

<span data-ttu-id="48880-197">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-197">Data type: **boolean**</span></span>

<span data-ttu-id="48880-198">Aplica-se a: métodos</span><span class="sxs-lookup"><span data-stu-id="48880-198">Applies to: methods</span></span>

<span data-ttu-id="48880-199">Indica se o método exclui instâncias.</span><span class="sxs-lookup"><span data-stu-id="48880-199">Indicates whether the method deletes instances.</span></span> <span data-ttu-id="48880-200">Os métodos que usam o qualificador do **destruidor** excluem as instâncias às quais o destruidor é aplicado e não são restritos a atuar em uma única instância ou classe.</span><span class="sxs-lookup"><span data-stu-id="48880-200">Methods using the **Destructor** qualifier delete the instance(s) to which the destructor is applied, and are not constrained to acting on a single instance or class.</span></span> <span data-ttu-id="48880-201">Por exemplo, um destruidor pode excluir instâncias de associação, bem como instâncias da classe que define o destruidor.</span><span class="sxs-lookup"><span data-stu-id="48880-201">For example, a destructor might delete association instances as well as instances of the class that defines the destructor.</span></span>

<span data-ttu-id="48880-202">O qualificador do **destruidor** destina-se apenas a informações e não é esperado que ele seja acionado pelo Gerenciador de objetos.</span><span class="sxs-lookup"><span data-stu-id="48880-202">The **Destructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="48880-203">Não há nenhuma obrigação para o Gerenciador de objetos chamar um método que tenha o qualificador do **destruidor** quando uma instância é excluída.</span><span class="sxs-lookup"><span data-stu-id="48880-203">There is no obligation for the object manager to call a method that has the **Destructor** qualifier when an instance is deleted.</span></span> <span data-ttu-id="48880-204">Além disso, quando um destruidor é chamado, o Gerenciador de objetos não precisa invocar nenhum método destruidor definido para qualquer classe pai da classe original.</span><span class="sxs-lookup"><span data-stu-id="48880-204">Also, when a destructor is called, the object manager does not have to invoke any destructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="48880-205">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-205">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="48880-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="48880-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-207">Data type: **string**</span></span>

<span data-ttu-id="48880-208">Aplica-se a: qualquer</span><span class="sxs-lookup"><span data-stu-id="48880-208">Applies to: any</span></span>

<span data-ttu-id="48880-209">Nome exibido na interface do usuário em vez do nome real do elemento.</span><span class="sxs-lookup"><span data-stu-id="48880-209">Name displayed in the UI instead of the actual name of the element.</span></span> <span data-ttu-id="48880-210">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-210">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span><span class="sxs-lookup"><span data-stu-id="48880-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span></span>
</dt> <dd>

<span data-ttu-id="48880-212">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-212">Data type: **string**</span></span>

<span data-ttu-id="48880-213">Aplica-se a: qualquer</span><span class="sxs-lookup"><span data-stu-id="48880-213">Applies to: any</span></span>

<span data-ttu-id="48880-214">O elemento de tipo de cadeia de caracteres qualificado contém uma instância inserida.</span><span class="sxs-lookup"><span data-stu-id="48880-214">The qualified string type element contains an embedded instance.</span></span> <span data-ttu-id="48880-215">O valor do qualificador especifica o nome de uma classe CIM no mesmo namespace que a classe que possui o elemento qualificado.</span><span class="sxs-lookup"><span data-stu-id="48880-215">The qualifier value specifies the name of a CIM class in the same namespace as the class owning the qualified element.</span></span> <span data-ttu-id="48880-216">A instância inserida é uma instância da classe especificada, incluindo instâncias de suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="48880-216">The embedded instance is an instance of the specified class, including instances of its subclasses.</span></span> <span data-ttu-id="48880-217">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-217">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Indicadores**</span><span class="sxs-lookup"><span data-stu-id="48880-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge**</span></span>
</dt> <dd>

<span data-ttu-id="48880-219">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-219">Data type: **boolean**</span></span>

<span data-ttu-id="48880-220">Aplica-se a: qualquer</span><span class="sxs-lookup"><span data-stu-id="48880-220">Applies to: any</span></span>

<span data-ttu-id="48880-221">Indica se a propriedade representa um inteiro não negativo, que pode aumentar ou diminuir, mas nunca excede um valor máximo.</span><span class="sxs-lookup"><span data-stu-id="48880-221">Indicates whether the property represents a non-negative integer, which can increase or decrease, but never exceed a maximum value.</span></span> <span data-ttu-id="48880-222">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-222">The default is **FALSE**.</span></span>

<span data-ttu-id="48880-223">O valor máximo da propriedade não pode ser maior que 2 ^*n* -1.</span><span class="sxs-lookup"><span data-stu-id="48880-223">The maximum value of the property cannot be greater than 2^*n* - 1.</span></span> <span data-ttu-id="48880-224">*N* pode ser 8, 16, 32 ou 64, dependendo do tipo de dados da propriedade ao qual esse qualificador é aplicado.</span><span class="sxs-lookup"><span data-stu-id="48880-224">*N* can be 8, 16, 32, or 64 depending on the data type of the property to which this qualifier is applied.</span></span> <span data-ttu-id="48880-225">O valor de um medidor tem seu valor máximo sempre que as informações que estão sendo modeladas são maiores ou iguais ao valor máximo.</span><span class="sxs-lookup"><span data-stu-id="48880-225">The value of a gauge has its maximum value whenever the information being modeled is greater or equal to that maximum value.</span></span> <span data-ttu-id="48880-226">Se as informações modeladas subsequentemente diminuirem abaixo do valor máximo, o medidor também diminuirá.</span><span class="sxs-lookup"><span data-stu-id="48880-226">If the information being modeled subsequently decreases below the maximum value, the gauge also decreases.</span></span> <span data-ttu-id="48880-227">Esse qualificador é aplicável somente a propriedades com um tipo de dados inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="48880-227">This qualifier is applicable only to properties with an unsigned integer data type.</span></span>

</dd> <dt>

<span data-ttu-id="48880-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**No**</span><span class="sxs-lookup"><span data-stu-id="48880-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**In**</span></span>
</dt> <dd>

<span data-ttu-id="48880-229">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-229">Data type: **boolean**</span></span>

<span data-ttu-id="48880-230">Aplica-se a: parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-230">Applies to: parameters</span></span>

<span data-ttu-id="48880-231">Indica se o parâmetro é usado para passar valores para um método.</span><span class="sxs-lookup"><span data-stu-id="48880-231">Indicates whether the parameter is used to pass values to a method.</span></span> <span data-ttu-id="48880-232">O padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="48880-232">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**Entrada, saída**</span><span class="sxs-lookup"><span data-stu-id="48880-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, Out**</span></span>
</dt> <dd>

<span data-ttu-id="48880-234">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-234">Data type: **boolean**</span></span>

<span data-ttu-id="48880-235">Aplica-se a: parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-235">Applies to: parameters</span></span>

<span data-ttu-id="48880-236">Indica se o parâmetro é um parâmetro de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="48880-236">Indicates whether the parameter is both an input and output parameter.</span></span>

</dd> <dt>

<span data-ttu-id="48880-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Chaves**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="48880-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Key**](key-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="48880-238">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-238">Data type: **boolean**</span></span>

<span data-ttu-id="48880-239">Aplica-se a: Propriedades, referências</span><span class="sxs-lookup"><span data-stu-id="48880-239">Applies to: properties, references</span></span>

<span data-ttu-id="48880-240">Indica se a propriedade faz parte do identificador do namespace.</span><span class="sxs-lookup"><span data-stu-id="48880-240">Indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="48880-241">Se mais de uma propriedade tiver o qualificador de [**chave**](key-qualifier.md) , todas essas propriedades formarão coletivamente a chave (uma chave composta).</span><span class="sxs-lookup"><span data-stu-id="48880-241">If more than one property has the [**Key**](key-qualifier.md) qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="48880-242">Quando agrupadas, as propriedades de chave devem fornecer uma referência exclusiva para cada instância de classe.</span><span class="sxs-lookup"><span data-stu-id="48880-242">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="48880-243">Se esse qualificador for colocado em uma propriedade, somente o valor **true** será permitido.</span><span class="sxs-lookup"><span data-stu-id="48880-243">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="48880-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Ocioso**</span><span class="sxs-lookup"><span data-stu-id="48880-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Lazy**</span></span>
</dt> <dd>

<span data-ttu-id="48880-245">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="48880-245">Applies to: properties</span></span>

<span data-ttu-id="48880-246">Indica que a propriedade tem uso intensivo de recursos para retornar e requer muito tempo de processador e memória.</span><span class="sxs-lookup"><span data-stu-id="48880-246">Indicates that the property is resource-intensive to return and requires a lot of processor time and memory.</span></span> <span data-ttu-id="48880-247">O WMI melhora o desempenho de consultas sem tentar retornar as propriedades marcadas com o qualificador **lento** .</span><span class="sxs-lookup"><span data-stu-id="48880-247">WMI improves the performance of queries by not attempting to return the properties marked with the **Lazy** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="48880-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span><span class="sxs-lookup"><span data-stu-id="48880-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span></span>
</dt> <dd>

<span data-ttu-id="48880-249">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-249">Data type: **string array**</span></span>

<span data-ttu-id="48880-250">Aplica-se a: classes, propriedades, associações, indicações, referências</span><span class="sxs-lookup"><span data-stu-id="48880-250">Applies to: classes, properties, associations, indications, references</span></span>

<span data-ttu-id="48880-251">Conjunto de valores que indicam um caminho para um local onde você pode encontrar mais informações sobre a origem de uma propriedade, classe, associação, indicação ou referência.</span><span class="sxs-lookup"><span data-stu-id="48880-251">Set of values that indicate a path to a location where you can find more information about the origin of a property, class, association, indication, or reference.</span></span> <span data-ttu-id="48880-252">A cadeia de caracteres de mapeamento pode ser um caminho de diretório, uma URL, uma chave do registro, um arquivo de inclusão, uma referência a uma classe CIM ou algum outro formato.</span><span class="sxs-lookup"><span data-stu-id="48880-252">The mapping string can be a directory path, a URL, a registry key, an include file, reference to a CIM class, or some other format.</span></span> <span data-ttu-id="48880-253">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-253">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Maximizar**</span><span class="sxs-lookup"><span data-stu-id="48880-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**</span></span>
</dt> <dd>

<span data-ttu-id="48880-255">Tipo de dados: **int**</span><span class="sxs-lookup"><span data-stu-id="48880-255">Data type: **int**</span></span>

<span data-ttu-id="48880-256">Aplica-se a: referências</span><span class="sxs-lookup"><span data-stu-id="48880-256">Applies to: references</span></span>

<span data-ttu-id="48880-257">Número máximo de valores que uma determinada referência pode ter para cada conjunto de outros valores de referência na associação.</span><span class="sxs-lookup"><span data-stu-id="48880-257">Maximum number of values a given reference can have for each set of other reference values in the association.</span></span> <span data-ttu-id="48880-258">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-258">The default is **NULL**.</span></span> <span data-ttu-id="48880-259">Por exemplo, se uma associação relacionar instâncias em instâncias B e deve haver no máximo uma instância para cada instância B, a referência a um deve ter um máximo de um qualificador.</span><span class="sxs-lookup"><span data-stu-id="48880-259">For example, if an association relates A instances to B instances and there must be at most one A instance for each B instance, then the reference to A should have a maximum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="48880-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span><span class="sxs-lookup"><span data-stu-id="48880-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span></span>
</dt> <dd>

<span data-ttu-id="48880-261">Tipo de dados: **int**</span><span class="sxs-lookup"><span data-stu-id="48880-261">Data type: **int**</span></span>

<span data-ttu-id="48880-262">Aplica-se a: Propriedades, métodos, parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-262">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="48880-263">Comprimento máximo (em caracteres) de um item de dados de **cadeia de caracteres** e indica suporte a matrizes de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="48880-263">Maximum length (in characters) of a **string** data item and indicates support of fixed-length arrays.</span></span>

<span data-ttu-id="48880-264">Se uma matriz de comprimento fixo for encontrada, o qualificador **maxlen** conterá o comprimento fixo encontrado durante a análise.</span><span class="sxs-lookup"><span data-stu-id="48880-264">If a fixed-length array is encountered, the **MaxLen** qualifier contains the fixed length found during parsing.</span></span> <span data-ttu-id="48880-265">Se uma matriz de comprimento variável for encontrada, esse qualificador não será usado.</span><span class="sxs-lookup"><span data-stu-id="48880-265">If a variable-length array is encountered, then this qualifier is not used.</span></span> <span data-ttu-id="48880-266">**Maxlen** é usado para sugerir o número máximo de elementos que devem ser armazenados em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="48880-266">**MaxLen** is used to suggest the maximum number of elements that should be stored in an array.</span></span> <span data-ttu-id="48880-267">Ao substituir o valor padrão, qualquer valor inteiro não atribuído (**UInt32**) pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="48880-267">When overriding the default value, any unsigned integer value (**uint32**) can be specified.</span></span> <span data-ttu-id="48880-268">Um valor de **NULL** (padrão) implica comprimento ilimitado.</span><span class="sxs-lookup"><span data-stu-id="48880-268">A value of **NULL** (default) implies unlimited length.</span></span>

</dd> <dt>

<span data-ttu-id="48880-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="48880-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="48880-270">Tipo de dados: **int**</span><span class="sxs-lookup"><span data-stu-id="48880-270">Data type: **int**</span></span>

<span data-ttu-id="48880-271">Aplica-se a: Propriedades, métodos, parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-271">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="48880-272">Valor máximo do objeto.</span><span class="sxs-lookup"><span data-stu-id="48880-272">Maximum value of the object.</span></span> <span data-ttu-id="48880-273">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-273">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**</span><span class="sxs-lookup"><span data-stu-id="48880-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**</span></span>
</dt> <dd>

<span data-ttu-id="48880-275">Tipo de dados: **int**</span><span class="sxs-lookup"><span data-stu-id="48880-275">Data type: **int**</span></span>

<span data-ttu-id="48880-276">Aplica-se a: referências</span><span class="sxs-lookup"><span data-stu-id="48880-276">Applies to: references</span></span>

<span data-ttu-id="48880-277">Cardinalidade mínima da referência (o número mínimo de valores que uma determinada referência pode ter para cada conjunto de outros valores de referência na associação).</span><span class="sxs-lookup"><span data-stu-id="48880-277">Minimum cardinality of the reference (the minimum number of values a given reference can have for each set of other reference values in the association).</span></span> <span data-ttu-id="48880-278">O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="48880-278">The default is 0.</span></span>

<span data-ttu-id="48880-279">Por exemplo, se uma associação relacionar instâncias a B, e deve haver pelo menos uma instância para cada instância B, a referência a um deve ter, no mínimo, um qualificador.</span><span class="sxs-lookup"><span data-stu-id="48880-279">For example, if an association relates A instances to B instances, and there must be at least one A instance for each B instance, then the reference to A should have a minimum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="48880-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span><span class="sxs-lookup"><span data-stu-id="48880-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="48880-281">Tipo de dados: **int**</span><span class="sxs-lookup"><span data-stu-id="48880-281">Data type: **int**</span></span>

<span data-ttu-id="48880-282">Aplica-se a: Propriedades, métodos, parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-282">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="48880-283">Indica o valor mínimo do objeto.</span><span class="sxs-lookup"><span data-stu-id="48880-283">Indicates the minimum value of the object.</span></span> <span data-ttu-id="48880-284">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-284">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span><span class="sxs-lookup"><span data-stu-id="48880-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span></span>
</dt> <dd>

<span data-ttu-id="48880-286">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-286">Data type: **string array**</span></span>

<span data-ttu-id="48880-287">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="48880-287">Applies to: properties</span></span>

<span data-ttu-id="48880-288">Conjunto de valores que indicam a correspondência entre a propriedade de um objeto e outras propriedades no esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="48880-288">Set of values that indicate correspondence between an object's property and other properties in the CIM schema.</span></span> <span data-ttu-id="48880-289">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-289">The default is **NULL**.</span></span>

<span data-ttu-id="48880-290">As propriedades do objeto são identificadas usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="48880-290">Object properties are identified using the following syntax.</span></span>

<span data-ttu-id="48880-291"><schema name> "\_" <class or association name> "." <property name></span><span class="sxs-lookup"><span data-stu-id="48880-291"><schema name> "\_" <class or association name> "." <property name></span></span>

</dd> <dt>

<span data-ttu-id="48880-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Diagnóstico não locais**</span><span class="sxs-lookup"><span data-stu-id="48880-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Nonlocal**</span></span>
</dt> <dd>

<span data-ttu-id="48880-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-293">Data type: **string**</span></span>

<span data-ttu-id="48880-294">Aplica-se a: referências</span><span class="sxs-lookup"><span data-stu-id="48880-294">Applies to: references</span></span>

<span data-ttu-id="48880-295">Local de uma instância, o valor de que é <*namespacetype*>://<*namespacehandle*> o padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-295">Location of an instance, the value of which is <*namespacetype*>://<*namespacehandle*> The default is **NULL**.</span></span>

<span data-ttu-id="48880-296">Uso: este qualificador não pode ser usado com o qualificador não **LocalType** .</span><span class="sxs-lookup"><span data-stu-id="48880-296">Usage: This qualifier cannot be used with the **NonlocalType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="48880-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**Não LocalType**</span><span class="sxs-lookup"><span data-stu-id="48880-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**</span></span>
</dt> <dd>

<span data-ttu-id="48880-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-298">Data type: **string**</span></span>

<span data-ttu-id="48880-299">Aplica-se a: referências</span><span class="sxs-lookup"><span data-stu-id="48880-299">Applies to: references</span></span>

<span data-ttu-id="48880-300">Tipo de local de uma instância.</span><span class="sxs-lookup"><span data-stu-id="48880-300">Type of location of an instance.</span></span> <span data-ttu-id="48880-301">Seu valor é <namespacetype> .</span><span class="sxs-lookup"><span data-stu-id="48880-301">Its value is <namespacetype>.</span></span> <span data-ttu-id="48880-302">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-302">The default is **NULL**.</span></span>

<span data-ttu-id="48880-303">Uso: este qualificador não pode ser usado com o qualificador não **local** .</span><span class="sxs-lookup"><span data-stu-id="48880-303">Usage: This qualifier cannot be used with the **Nonlocal** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="48880-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span><span class="sxs-lookup"><span data-stu-id="48880-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span></span>
</dt> <dd>

<span data-ttu-id="48880-305">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-305">Data type: **string**</span></span>

<span data-ttu-id="48880-306">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="48880-306">Applies to: properties</span></span>

<span data-ttu-id="48880-307">Valor que indica que a propriedade associada é **nula** (a propriedade não tem um valor válido ou significativo).</span><span class="sxs-lookup"><span data-stu-id="48880-307">Value that indicates that the associated property is **NULL** (the property does not have a valid or meaningful value).</span></span> <span data-ttu-id="48880-308">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-308">The default is **NULL**.</span></span>

<span data-ttu-id="48880-309">As convenções e restrições usadas para definir valores **nulos** são as mesmas aplicáveis ao qualificador **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="48880-309">The conventions and restrictions used for defining **NULL** values are the same as those applicable to the **ValueMap** qualifier.</span></span> <span data-ttu-id="48880-310">Observe que esse qualificador não pode ser substituído.</span><span class="sxs-lookup"><span data-stu-id="48880-310">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="48880-311">Não é razoável permitir que uma subclasse retorne um valor **nulo** diferente daquele da classe pai.</span><span class="sxs-lookup"><span data-stu-id="48880-311">It is unreasonable to permit a subclass to return a different **NULL** value than that of the parent class.</span></span>

</dd> <dt>

<span data-ttu-id="48880-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Fora**</span><span class="sxs-lookup"><span data-stu-id="48880-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Out**</span></span>
</dt> <dd>

<span data-ttu-id="48880-313">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-313">Data type: **boolean**</span></span>

<span data-ttu-id="48880-314">Aplica-se a: parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-314">Applies to: parameters</span></span>

<span data-ttu-id="48880-315">Indica se o parâmetro retorna valores de um método.</span><span class="sxs-lookup"><span data-stu-id="48880-315">Indicates whether the parameter returns values from a method.</span></span> <span data-ttu-id="48880-316">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-316">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Substituição**</span><span class="sxs-lookup"><span data-stu-id="48880-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Override**</span></span>
</dt> <dd>

<span data-ttu-id="48880-318">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-318">Data type: **string**</span></span>

<span data-ttu-id="48880-319">Aplica-se a: Propriedades, métodos, referências</span><span class="sxs-lookup"><span data-stu-id="48880-319">Applies to: properties, methods, references</span></span>

<span data-ttu-id="48880-320">Classe pai ou construção subordinada (Propriedade, método ou referência) que é substituída pela propriedade, método ou referência do mesmo nome na classe derivada.</span><span class="sxs-lookup"><span data-stu-id="48880-320">Parent class or subordinate construct (property, method, or reference) which is overridden by the property, method, or reference of the same name in the derived class.</span></span> <span data-ttu-id="48880-321">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-321">The default is **NULL**.</span></span>

<span data-ttu-id="48880-322">O formato é:</span><span class="sxs-lookup"><span data-stu-id="48880-322">The format is:</span></span>

<span data-ttu-id="48880-323">\[<> de *classe* . \] < *construção subordinada*></span><span class="sxs-lookup"><span data-stu-id="48880-323">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="48880-324">Se o nome da classe for omitido, a substituição se aplicará à construção subordinada na classe pai na hierarquia de classe.</span><span class="sxs-lookup"><span data-stu-id="48880-324">If the class name is omitted, the override applies to the subordinate construct in the parent class in the class hierarchy.</span></span>

<span data-ttu-id="48880-325">Uso: o qualificador de **substituição** pode se referir a construções com base no mesmo modelo meta apenas.</span><span class="sxs-lookup"><span data-stu-id="48880-325">Usage: The **Override** qualifier can refer to constructs based on the same meta model only.</span></span> <span data-ttu-id="48880-326">Não é permitido alterar um nome ou assinatura de construção durante uma operação de substituição.</span><span class="sxs-lookup"><span data-stu-id="48880-326">It is not allowed to change a construct name or signature during an override operation.</span></span>

</dd> <dt>

<span data-ttu-id="48880-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**Sobreridevalue**</span><span class="sxs-lookup"><span data-stu-id="48880-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**</span></span>
</dt> <dd>

<span data-ttu-id="48880-328">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="48880-328">Applies to: classes</span></span>

<span data-ttu-id="48880-329">Indica se o valor da propriedade em uma subclasse substitui o valor em uma classe pai.</span><span class="sxs-lookup"><span data-stu-id="48880-329">Indicates whether the property value on a subclass overrides the value in a parent class.</span></span> <span data-ttu-id="48880-330">A implicação funcional é que, se você executar uma consulta em relação à classe pai e se a cláusula **Where** incluir essa propriedade, o pai deverá retornar uma instância com o valor substituído.</span><span class="sxs-lookup"><span data-stu-id="48880-330">The functional implication is that, if you perform a query against the parent class, and if your **WHERE** clause includes this property, the parent must return an instance with the overridden value.</span></span> <span data-ttu-id="48880-331">Como resultado, o gerenciamento do Windows ajusta a cláusula **Where** da consulta enviada para a classe pai para excluir referências a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="48880-331">As a result, Windows Management adjusts the **WHERE** clause of the query sent to the parent class to exclude references to this property.</span></span>

</dd> <dt>

<span data-ttu-id="48880-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagadas**</span><span class="sxs-lookup"><span data-stu-id="48880-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagated**</span></span>
</dt> <dd>

<span data-ttu-id="48880-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-333">Data type: **string**</span></span>

<span data-ttu-id="48880-334">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="48880-334">Applies to: properties</span></span>

<span data-ttu-id="48880-335">Nome da chave que está sendo propagada.</span><span class="sxs-lookup"><span data-stu-id="48880-335">Name of the key being propagated.</span></span> <span data-ttu-id="48880-336">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-336">The default is **NULL**.</span></span>

<span data-ttu-id="48880-337">O uso desse qualificador pressupõe a existência de apenas um qualificador fraco em uma referência que tem a classe que a contém como seu destino.</span><span class="sxs-lookup"><span data-stu-id="48880-337">Use of this qualifier assumes the existence of only one weak qualifier on a reference that has the containing class as its target.</span></span> <span data-ttu-id="48880-338">A propriedade associada deve ter o mesmo valor que a propriedade nomeada pelo qualificador na classe no outro lado da Associação fraca.</span><span class="sxs-lookup"><span data-stu-id="48880-338">The associated property must have the same value as the property named by the qualifier in the class on the other side of the weak association.</span></span> <span data-ttu-id="48880-339">O formato é:</span><span class="sxs-lookup"><span data-stu-id="48880-339">The format is:</span></span>

<span data-ttu-id="48880-340">\[<> de *classe* . \] < *construção subordinada*></span><span class="sxs-lookup"><span data-stu-id="48880-340">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="48880-341">Uso: quando o qualificador **propagado** é usado, o qualificador de [**chave**](key-qualifier.md) deve ser especificado com um valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="48880-341">Usage: When the **Propagated** qualifier is used, the [**Key**](key-qualifier.md) qualifier must be specified with a value of **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Leitura**</span><span class="sxs-lookup"><span data-stu-id="48880-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read**</span></span>
</dt> <dd>

<span data-ttu-id="48880-343">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-343">Data type: **boolean**</span></span>

<span data-ttu-id="48880-344">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="48880-344">Applies to: properties</span></span>

<span data-ttu-id="48880-345">Indica se a propriedade é legível.</span><span class="sxs-lookup"><span data-stu-id="48880-345">Indicates whether the property is readable.</span></span> <span data-ttu-id="48880-346">O padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="48880-346">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Necessário**</span><span class="sxs-lookup"><span data-stu-id="48880-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Required**</span></span>
</dt> <dd>

<span data-ttu-id="48880-348">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-348">Data type: **boolean**</span></span>

<span data-ttu-id="48880-349">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="48880-349">Applies to: properties</span></span>

<span data-ttu-id="48880-350">Indica se um valor não nulo é necessário para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="48880-350">Indicates whether a non-null value is required for the property.</span></span> <span data-ttu-id="48880-351">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-351">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revisão**</span><span class="sxs-lookup"><span data-stu-id="48880-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="48880-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-353">Data type: **string**</span></span>

<span data-ttu-id="48880-354">Aplica-se a: classes, associações, indicações, esquemas</span><span class="sxs-lookup"><span data-stu-id="48880-354">Applies to: classes, associations, indications, schemas</span></span>

<span data-ttu-id="48880-355">Número de revisão secundária do objeto de esquema.</span><span class="sxs-lookup"><span data-stu-id="48880-355">Minor revision number of the schema object.</span></span> <span data-ttu-id="48880-356">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-356">The default is **NULL**.</span></span>

<span data-ttu-id="48880-357">Uso: o qualificador de **versão** deve estar presente para fornecer o número de versão principal quando o qualificador de **revisão** é usado.</span><span class="sxs-lookup"><span data-stu-id="48880-357">Usage: The **Version** qualifier must be present to supply the major version number when the **Revision** qualifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="48880-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Esquema**</span><span class="sxs-lookup"><span data-stu-id="48880-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schema**</span></span>
</dt> <dd>

<span data-ttu-id="48880-359">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-359">Data type: **string**</span></span>

<span data-ttu-id="48880-360">Aplica-se a: Propriedades, métodos</span><span class="sxs-lookup"><span data-stu-id="48880-360">Applies to: properties, methods</span></span>

<span data-ttu-id="48880-361">Nome do esquema no qual o recurso está definido.</span><span class="sxs-lookup"><span data-stu-id="48880-361">Name of the schema in which the feature is defined.</span></span> <span data-ttu-id="48880-362">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-362">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Original**</span><span class="sxs-lookup"><span data-stu-id="48880-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Source**</span></span>
</dt> <dd>

<span data-ttu-id="48880-364">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-364">Data type: **string**</span></span>

<span data-ttu-id="48880-365">Aplica-se a: classes, associações, indicações, referências</span><span class="sxs-lookup"><span data-stu-id="48880-365">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="48880-366">Local de uma instância.</span><span class="sxs-lookup"><span data-stu-id="48880-366">Location of an instance.</span></span> <span data-ttu-id="48880-367">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-367">The default is **NULL**.</span></span>

<span data-ttu-id="48880-368">O valor do qualificador é <*namespacetype*>://<*namespacehandle*>.</span><span class="sxs-lookup"><span data-stu-id="48880-368">The qualifier's value is <*namespacetype*>://<*namespacehandle*>.</span></span>

<span data-ttu-id="48880-369">Uso: o qualificador de **origem** não pode ser usado com o qualificador **SourceType** .</span><span class="sxs-lookup"><span data-stu-id="48880-369">Usage: The **Source** qualifier cannot be used with the **SourceType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="48880-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span><span class="sxs-lookup"><span data-stu-id="48880-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span></span>
</dt> <dd>

<span data-ttu-id="48880-371">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-371">Data type: **string**</span></span>

<span data-ttu-id="48880-372">Aplica-se a: classes, associações, indicações, referências</span><span class="sxs-lookup"><span data-stu-id="48880-372">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="48880-373">Tipo de local de uma instância.</span><span class="sxs-lookup"><span data-stu-id="48880-373">Type of location of an instance.</span></span> <span data-ttu-id="48880-374">O valor desse qualificador é <*namespacetype*>.</span><span class="sxs-lookup"><span data-stu-id="48880-374">The value of this qualifier is <*namespacetype*>.</span></span> <span data-ttu-id="48880-375">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-375">The default is **NULL**.</span></span>

<span data-ttu-id="48880-376">Uso: o qualificador **SourceType** não pode ser usado com o qualificador de **origem** .</span><span class="sxs-lookup"><span data-stu-id="48880-376">Usage: The **SourceType** qualifier cannot be used with the **Source** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="48880-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span><span class="sxs-lookup"><span data-stu-id="48880-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span></span>
</dt> <dd>

<span data-ttu-id="48880-378">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-378">Data type: **boolean**</span></span>

<span data-ttu-id="48880-379">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="48880-379">Applies to: classes</span></span>

<span data-ttu-id="48880-380">Indica se a classe oferece suporte à criação de instâncias.</span><span class="sxs-lookup"><span data-stu-id="48880-380">Indicates whether the class supports the creation of instances.</span></span> <span data-ttu-id="48880-381">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-381">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="48880-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span></span>
</dt> <dd>

<span data-ttu-id="48880-383">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-383">Data type: **boolean**</span></span>

<span data-ttu-id="48880-384">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="48880-384">Applies to: classes</span></span>

<span data-ttu-id="48880-385">Indica se a classe oferece suporte à exclusão de instâncias.</span><span class="sxs-lookup"><span data-stu-id="48880-385">Indicates whether the class supports the deletion of instances.</span></span> <span data-ttu-id="48880-386">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-386">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span><span class="sxs-lookup"><span data-stu-id="48880-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="48880-388">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-388">Data type: **boolean**</span></span>

<span data-ttu-id="48880-389">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="48880-389">Applies to: classes</span></span>

<span data-ttu-id="48880-390">Indica se a classe oferece suporte à modificação (atualização) de instâncias.</span><span class="sxs-lookup"><span data-stu-id="48880-390">Indicates whether the class supports the modification (updating) of instances.</span></span> <span data-ttu-id="48880-391">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-391">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Componentes**</span><span class="sxs-lookup"><span data-stu-id="48880-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**</span></span>
</dt> <dd>

<span data-ttu-id="48880-393">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-393">Data type: **boolean**</span></span>

<span data-ttu-id="48880-394">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="48880-394">Applies to: classes</span></span>

<span data-ttu-id="48880-395">Indica se a classe pode ter subclasses.</span><span class="sxs-lookup"><span data-stu-id="48880-395">Indicates whether the class can have subclasses.</span></span> <span data-ttu-id="48880-396">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-396">The default is **FALSE**.</span></span>

<span data-ttu-id="48880-397">Se uma subclasse for declarada, o compilador gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="48880-397">If a subclass is declared, the compiler generates an error.</span></span>

<span data-ttu-id="48880-398">Uso: esse qualificador não pode coexistir com o qualificador **abstrato** .</span><span class="sxs-lookup"><span data-stu-id="48880-398">Usage: This qualifier cannot coexist with the **Abstract** qualifier.</span></span> <span data-ttu-id="48880-399">Se os qualificadores **terminal** e **abstract** forem especificados, o compilador gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="48880-399">If both the **Terminal** and **Abstract** qualifiers are specified, the compiler generates an error.</span></span>

</dd> <dt>

<span data-ttu-id="48880-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Unit**</span><span class="sxs-lookup"><span data-stu-id="48880-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Units**</span></span>
</dt> <dd>

<span data-ttu-id="48880-401">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-401">Data type: **string**</span></span>

<span data-ttu-id="48880-402">Aplica-se a: Propriedades, métodos, parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-402">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="48880-403">Tipo de unidade na qual o item de dados associado é expresso.</span><span class="sxs-lookup"><span data-stu-id="48880-403">Type of unit in which the associated data item is expressed.</span></span> <span data-ttu-id="48880-404">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-404">The default is **NULL**.</span></span>

<span data-ttu-id="48880-405">Por exemplo, um item de dados de tamanho pode ter um valor de "bytes" para **unidades**.</span><span class="sxs-lookup"><span data-stu-id="48880-405">For example, a size data item might have a value of "bytes" for **Units**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span><span class="sxs-lookup"><span data-stu-id="48880-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span></span>
</dt> <dd>

<span data-ttu-id="48880-407">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-407">Data type: **string array**</span></span>

<span data-ttu-id="48880-408">Aplica-se a: Propriedades, métodos, parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-408">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="48880-409">Conjunto de valores permitidos para uma propriedade, tipo de retorno de método ou parâmetro de método.</span><span class="sxs-lookup"><span data-stu-id="48880-409">Set of permissible values for a property, method return type, or method parameter.</span></span> <span data-ttu-id="48880-410">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-410">The default is **NULL**.</span></span>

<span data-ttu-id="48880-411">Uso: esse qualificador pode ser usado sozinha ou em combinação com o qualificador de **valores** .</span><span class="sxs-lookup"><span data-stu-id="48880-411">Usage: This qualifier can be used alone or in combination with the **Values** qualifier.</span></span> <span data-ttu-id="48880-412">Quando usado em combinação com o qualificador de **valores** , o local do valor na matriz **ValueMap** fornece o local da entrada correspondente na matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="48880-412">When used in combination with the **Values** qualifier, the location of the value in the **ValueMap** array provides the location of the corresponding entry in the **Values** array.</span></span> <span data-ttu-id="48880-413">Use o qualificador **ValueMap** somente com valores de cadeia de caracteres e inteiros.</span><span class="sxs-lookup"><span data-stu-id="48880-413">Use the **ValueMap** qualifier only with string and integer values.</span></span> <span data-ttu-id="48880-414">A sintaxe para representar um valor inteiro na matriz de mapa de valor é dígito dígito \[ + \| = \] \[ \* \] .</span><span class="sxs-lookup"><span data-stu-id="48880-414">The syntax for representing an integer value in the value map array is \[+\|=\]digit\[\*digit\].</span></span> <span data-ttu-id="48880-415">O conteúdo, o número máximo de dígitos e o valor representado são restritos pelo tipo da propriedade associada.</span><span class="sxs-lookup"><span data-stu-id="48880-415">The content, maximum number of digits, and represented value are constrained by the type of the associated property.</span></span> <span data-ttu-id="48880-416">Por exemplo, uint8 não pode ser assinado, deve ter menos de quatro dígitos e deve representar um valor menor que 256.</span><span class="sxs-lookup"><span data-stu-id="48880-416">For example, uint8 may not be signed, must be less than four digits, and must represent a value less than 256.</span></span>

</dd> <dt>

<span data-ttu-id="48880-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Os**</span><span class="sxs-lookup"><span data-stu-id="48880-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Values**</span></span>
</dt> <dd>

<span data-ttu-id="48880-418">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-418">Data type: **string array**</span></span>

<span data-ttu-id="48880-419">Aplica-se a: Propriedades, métodos, parâmetros</span><span class="sxs-lookup"><span data-stu-id="48880-419">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="48880-420">Conjunto de valores que convertem um valor inteiro em uma cadeia de caracteres associada.</span><span class="sxs-lookup"><span data-stu-id="48880-420">Set of values translating an integer value into an associated string.</span></span> <span data-ttu-id="48880-421">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-421">The default is **NULL**.</span></span>

<span data-ttu-id="48880-422">Essa propriedade também especifica uma matriz de valores de cadeia de caracteres a ser mapeada para uma propriedade de enumeração.</span><span class="sxs-lookup"><span data-stu-id="48880-422">This property also specifies an array of string values to be mapped to an enumeration property.</span></span> <span data-ttu-id="48880-423">Esse qualificador pode ser aplicado a uma propriedade de inteiro ou a uma propriedade de cadeia de caracteres, e o mapeamento pode ser implícito ou explícito.</span><span class="sxs-lookup"><span data-stu-id="48880-423">This qualifier can be applied to either an integer property or a string property, and the mapping can be implicit or explicit.</span></span> <span data-ttu-id="48880-424">Se o mapeamento for implícito, os valores de propriedade de inteiro ou de cadeia de caracteres representarão posições ordinais na matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="48880-424">If the mapping is implicit, integer or string property values represent ordinal positions in the **Values** array.</span></span> <span data-ttu-id="48880-425">Se o mapeamento for explícito, a propriedade deverá ser um inteiro e os valores de propriedade válidos serão listados na matriz definida pelo qualificador **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="48880-425">If the mapping is explicit, the property must be an integer, and valid property values are listed in the array defined by the **ValueMap** qualifier.</span></span> <span data-ttu-id="48880-426">Para obter mais informações, consulte [mapa de valor](value-map.md).</span><span class="sxs-lookup"><span data-stu-id="48880-426">For more information, see [Value Map](value-map.md).</span></span>

<span data-ttu-id="48880-427">Se um qualificador de **ValueMap** não estiver presente, a matriz **Values** será indexada (relativa a zero) usando o valor na propriedade associada, no tipo de retorno do método ou no parâmetro do método.</span><span class="sxs-lookup"><span data-stu-id="48880-427">If a **ValueMap** qualifier is not present, the **Values** array is indexed (zero-relative) by using the value in the associated property, method return type, or method parameter.</span></span> <span data-ttu-id="48880-428">Se um qualificador de **ValueMap** estiver presente, o índice de valores será definido pelo local do valor da propriedade no mapa de valores.</span><span class="sxs-lookup"><span data-stu-id="48880-428">If a **ValueMap** qualifier is present, the values index is defined by the location of the property value in the value map.</span></span>

</dd> <dt>

<span data-ttu-id="48880-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versão**</span><span class="sxs-lookup"><span data-stu-id="48880-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="48880-430">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48880-430">Data type: **string**</span></span>

<span data-ttu-id="48880-431">Aplica-se a: classes, esquemas, associações, indicações</span><span class="sxs-lookup"><span data-stu-id="48880-431">Applies to: classes, schemas, associations, indications</span></span>

<span data-ttu-id="48880-432">Número de versão principal do objeto de esquema.</span><span class="sxs-lookup"><span data-stu-id="48880-432">Major version number of the schema object.</span></span> <span data-ttu-id="48880-433">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="48880-433">The default is **NULL**.</span></span> <span data-ttu-id="48880-434">O número de versão é incrementado quando são feitas alterações no esquema que alteram a interface.</span><span class="sxs-lookup"><span data-stu-id="48880-434">The version number is incremented when changes are made to the schema that alter the interface.</span></span>

</dd> <dt>

<span data-ttu-id="48880-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Baixas**</span><span class="sxs-lookup"><span data-stu-id="48880-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Weak**</span></span>
</dt> <dd>

<span data-ttu-id="48880-436">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-436">Data type: **boolean**</span></span>

<span data-ttu-id="48880-437">Aplica-se a: referências</span><span class="sxs-lookup"><span data-stu-id="48880-437">Applies to: references</span></span>

<span data-ttu-id="48880-438">Indica se as chaves da classe referenciada incluem as chaves dos outros participantes na associação.</span><span class="sxs-lookup"><span data-stu-id="48880-438">Indicates whether the keys of the referenced class include the keys of the other participants in the association.</span></span> <span data-ttu-id="48880-439">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-439">The default is **FALSE**.</span></span>

<span data-ttu-id="48880-440">Esse qualificador é usado quando a identidade da classe referenciada depende da identidade dos outros participantes na associação.</span><span class="sxs-lookup"><span data-stu-id="48880-440">This qualifier is used when the identity of the referenced class depends on the identity of the other participants in the association.</span></span> <span data-ttu-id="48880-441">Não mais de uma referência a uma determinada classe pode ser fraca.</span><span class="sxs-lookup"><span data-stu-id="48880-441">No more than one reference to any given class can be weak.</span></span> <span data-ttu-id="48880-442">As outras classes na associação devem definir uma chave.</span><span class="sxs-lookup"><span data-stu-id="48880-442">The other classes in the association must define a key.</span></span> <span data-ttu-id="48880-443">As chaves das outras classes na associação são repetidas na classe referenciada e são marcadas com um qualificador **propagado** .</span><span class="sxs-lookup"><span data-stu-id="48880-443">The keys of the other classes in the association are repeated in the referenced class and are tagged with a **Propagated** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="48880-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Gravá**</span><span class="sxs-lookup"><span data-stu-id="48880-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Write**</span></span>
</dt> <dd>

<span data-ttu-id="48880-445">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-445">Data type: **boolean**</span></span>

<span data-ttu-id="48880-446">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="48880-446">Applies to: properties</span></span>

<span data-ttu-id="48880-447">Indica que os aplicativos ou scripts podem alterar o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="48880-447">Indicates that applications or scripts can change the property value.</span></span> <span data-ttu-id="48880-448">A conta que executa o aplicativo deve ter acesso ao namespace que contém instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="48880-448">The account that runs the application must have access to the namespace that contains instances of the class.</span></span> <span data-ttu-id="48880-449">A implementação do provedor também pode limitar o acesso aos dados do provedor.</span><span class="sxs-lookup"><span data-stu-id="48880-449">The provider implementation may also limit access to provider data.</span></span> <span data-ttu-id="48880-450">Um valor **true** indica que a propriedade é legível e gravável por consumidores que têm permissão de acesso pelo WMI e pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="48880-450">A value of **TRUE** indicates that the property is readable and writeable by consumers that are allowed access by WMI and the provider.</span></span> <span data-ttu-id="48880-451">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-451">The default is **FALSE**.</span></span>

<span data-ttu-id="48880-452">Uma propriedade que não tem o qualificador de **gravação** ainda pode ser gravável.</span><span class="sxs-lookup"><span data-stu-id="48880-452">A property that lacks the **Write** qualifier may still be writeable.</span></span> <span data-ttu-id="48880-453">A implementação do provedor pode permitir que todas as propriedades nas classes do provedor sejam alteradas, se o qualificador de **gravação** estiver presente.</span><span class="sxs-lookup"><span data-stu-id="48880-453">The provider implementation may allow any properties in the provider classes to be changed, whether the **Write** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="48880-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span><span class="sxs-lookup"><span data-stu-id="48880-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span></span>
</dt> <dd>

<span data-ttu-id="48880-455">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-455">Data type: **boolean**</span></span>

<span data-ttu-id="48880-456">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="48880-456">Applies to: properties</span></span>

<span data-ttu-id="48880-457">Indica se a propriedade é gravável na criação da instância.</span><span class="sxs-lookup"><span data-stu-id="48880-457">Indicates whether the property is writeable at instance creation.</span></span> <span data-ttu-id="48880-458">Esse qualificador pode ser usado em conjunto com o qualificador **WriteAtCreate** .</span><span class="sxs-lookup"><span data-stu-id="48880-458">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="48880-459">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-459">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="48880-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span><span class="sxs-lookup"><span data-stu-id="48880-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="48880-461">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="48880-461">Data type: **boolean**</span></span>

<span data-ttu-id="48880-462">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="48880-462">Applies to: properties</span></span>

<span data-ttu-id="48880-463">Indica se a propriedade é gravável na atualização da instância.</span><span class="sxs-lookup"><span data-stu-id="48880-463">Indicates whether the property is writeable at instance update.</span></span> <span data-ttu-id="48880-464">Esse qualificador pode ser usado em conjunto com o qualificador **WriteAtCreate** .</span><span class="sxs-lookup"><span data-stu-id="48880-464">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="48880-465">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="48880-465">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="48880-466">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48880-466">Examples</span></span>

<span data-ttu-id="48880-467">Para obter mais informações sobre como recuperar qualificadores, consulte o exemplo de código do PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) na galeria do TechNet.</span><span class="sxs-lookup"><span data-stu-id="48880-467">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

## <a name="requirements"></a><span data-ttu-id="48880-468">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48880-468">Requirements</span></span>



| <span data-ttu-id="48880-469">Requisito</span><span class="sxs-lookup"><span data-stu-id="48880-469">Requirement</span></span> | <span data-ttu-id="48880-470">Valor</span><span class="sxs-lookup"><span data-stu-id="48880-470">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="48880-471">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48880-471">Minimum supported client</span></span><br/> | <span data-ttu-id="48880-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48880-472">Windows Vista</span></span><br/>       |
| <span data-ttu-id="48880-473">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48880-473">Minimum supported server</span></span><br/> | <span data-ttu-id="48880-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48880-474">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48880-475">Confira também</span><span class="sxs-lookup"><span data-stu-id="48880-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48880-476">Qualificadores WMI</span><span class="sxs-lookup"><span data-stu-id="48880-476">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="48880-477">Adicionando um qualificador</span><span class="sxs-lookup"><span data-stu-id="48880-477">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




