---
description: Qualificadores opcionais abordam situações recorrentes não comuns a todas as implementações em conformidade com CIM, que não são necessárias para interpretar esses qualificadores.
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: Qualificadores opcionais
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765252"
---
# <a name="optional-qualifiers"></a><span data-ttu-id="50015-103">Qualificadores opcionais</span><span class="sxs-lookup"><span data-stu-id="50015-103">Optional Qualifiers</span></span>

<span data-ttu-id="50015-104">Qualificadores opcionais abordam situações recorrentes não comuns a todas as implementações em conformidade com CIM, que não são necessárias para interpretar esses qualificadores.</span><span class="sxs-lookup"><span data-stu-id="50015-104">Optional qualifiers address recurring situations not common to all CIM-compliant implementations, which are not required to interpret these qualifiers.</span></span> <span data-ttu-id="50015-105">Os qualificadores opcionais são fornecidos na especificação para evitar qualificadores aleatórios definidos pelo usuário que podem ocorrer nessas situações recorrentes.</span><span class="sxs-lookup"><span data-stu-id="50015-105">Optional qualifiers are provided in the specification to avoid random user-defined qualifiers that might occur in these recurring situations.</span></span>

<dt>

<span data-ttu-id="50015-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Apagar**</span><span class="sxs-lookup"><span data-stu-id="50015-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete**</span></span>
</dt> <dd>

<span data-ttu-id="50015-107">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="50015-107">Data type: **boolean**</span></span>

<span data-ttu-id="50015-108">Aplica-se a: associações, referências</span><span class="sxs-lookup"><span data-stu-id="50015-108">Applies to: associations, references</span></span>

<span data-ttu-id="50015-109">Para associações, indica se a associação qualificada deve ser excluída se qualquer um dos objetos referenciados na associação for excluído e se o respectivo objeto referenciado na associação for qualificado com **IfDeleted**.</span><span class="sxs-lookup"><span data-stu-id="50015-109">For associations, indicates whether the qualified association must be deleted if any of the objects referenced in the association are deleted and if the respective object referenced in the association is qualified with **IfDeleted**.</span></span> <span data-ttu-id="50015-110">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="50015-110">The default is **FALSE**.</span></span>

<span data-ttu-id="50015-111">Para referências, esse qualificador indica se o objeto referenciado deve ser excluído se a associação que contém a referência for excluída e qualificada com **IfDeleted**, ou se qualquer um dos objetos referenciados na associação for excluído e o respectivo objeto referenciado na associação for qualificado com **IfDeleted**.</span><span class="sxs-lookup"><span data-stu-id="50015-111">For references, this qualifier indicates whether the referenced object must be deleted if the association containing the reference is deleted and qualified with **IfDeleted**, or if any of the objects referenced in the association are deleted and the respective object referenced in the association is qualified with **IfDeleted**.</span></span>

<span data-ttu-id="50015-112">Uso: os aplicativos devem controlar associações e referências marcadas com o qualificador de **exclusão** e excluir a associação ou referência adequadamente.</span><span class="sxs-lookup"><span data-stu-id="50015-112">Usage: Applications must track associations and references marked with the **Delete** qualifier and delete the association or reference appropriately.</span></span> <span data-ttu-id="50015-113">Se um objeto na associação tiver sido excluído, mas não estiver marcado com **IfDeleted**, a associação não deverá ser excluída.</span><span class="sxs-lookup"><span data-stu-id="50015-113">If an object in the association has been deleted but is not marked with **IfDeleted**, then the association should not be deleted.</span></span>

<span data-ttu-id="50015-114">Essa regra de uso deve ser verificada quando o modelo de segurança CIM é definido.</span><span class="sxs-lookup"><span data-stu-id="50015-114">This usage rule must be verified when the CIM security model is defined.</span></span>

</dd> <dt>

<span data-ttu-id="50015-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Caro**</span><span class="sxs-lookup"><span data-stu-id="50015-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Expensive**</span></span>
</dt> <dd>

<span data-ttu-id="50015-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="50015-116">Data type: **boolean**</span></span>

<span data-ttu-id="50015-117">Aplica-se a: Propriedades, referências, classes, associações, métodos</span><span class="sxs-lookup"><span data-stu-id="50015-117">Applies to: properties, references, classes, associations, methods</span></span>

<span data-ttu-id="50015-118">Indica se a ação implícita requer computação extensiva.</span><span class="sxs-lookup"><span data-stu-id="50015-118">Indicates whether the implied action requires extensive computation.</span></span> <span data-ttu-id="50015-119">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="50015-119">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="50015-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span><span class="sxs-lookup"><span data-stu-id="50015-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span></span>
</dt> <dd>

<span data-ttu-id="50015-121">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="50015-121">Data type: **boolean**</span></span>

<span data-ttu-id="50015-122">Aplica-se a: associações e referências</span><span class="sxs-lookup"><span data-stu-id="50015-122">Applies to: associations and references</span></span>

<span data-ttu-id="50015-123">Indica se todos os objetos em uma associação qualificada pela **exclusão** devem ser excluídos se o objeto referenciado ou a associação for excluída.</span><span class="sxs-lookup"><span data-stu-id="50015-123">Indicates whether all objects within an association that is qualified by **Delete** must be deleted if the referenced object or the association is deleted.</span></span> <span data-ttu-id="50015-124">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="50015-124">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="50015-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexa**</span><span class="sxs-lookup"><span data-stu-id="50015-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexed**</span></span>
</dt> <dd>

<span data-ttu-id="50015-126">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="50015-126">Data type: **boolean**</span></span>

<span data-ttu-id="50015-127">Aplica-se a: Propriedades, métodos</span><span class="sxs-lookup"><span data-stu-id="50015-127">Applies to: properties, methods</span></span>

<span data-ttu-id="50015-128">Indica se uma propriedade de classe deve ser indexada.</span><span class="sxs-lookup"><span data-stu-id="50015-128">Indicates whether a class property should be indexed.</span></span> <span data-ttu-id="50015-129">Quando aplicado a propriedades em classes hospedadas pelo repositório, isso só tem o significado de criar (no momento da criação da classe) uma pesquisa de consulta secundária rápida para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="50015-129">When applied to properties in classes hosted by the repository, this only has the meaning of creating (at the time of class creation) a fast secondary query lookup for that property.</span></span>

<span data-ttu-id="50015-130">Somente o valor **true** (padrão) é permitido.</span><span class="sxs-lookup"><span data-stu-id="50015-130">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="50015-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisível**</span><span class="sxs-lookup"><span data-stu-id="50015-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisible**</span></span>
</dt> <dd>

<span data-ttu-id="50015-132">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="50015-132">Data type: **boolean**</span></span>

<span data-ttu-id="50015-133">Aplica-se a: associações, propriedades, métodos, referências, classes</span><span class="sxs-lookup"><span data-stu-id="50015-133">Applies to: associations, properties, methods, references, classes</span></span>

<span data-ttu-id="50015-134">Indica se a associação é definida somente para fins internos (por exemplo, para definição de semântica de dependência) e não deve ser exibida (por exemplo, em mapas).</span><span class="sxs-lookup"><span data-stu-id="50015-134">Indicates whether the association is defined only for internal purposes (for example, for definition of dependency semantics) and should not be displayed (for example, in maps).</span></span> <span data-ttu-id="50015-135">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="50015-135">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="50015-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Vários**</span><span class="sxs-lookup"><span data-stu-id="50015-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Large**</span></span>
</dt> <dd>

<span data-ttu-id="50015-137">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="50015-137">Data type: **boolean**</span></span>

<span data-ttu-id="50015-138">Aplica-se a: Propriedades, classes</span><span class="sxs-lookup"><span data-stu-id="50015-138">Applies to: properties, classes</span></span>

<span data-ttu-id="50015-139">Indica se a propriedade ou classe requer uma grande quantidade de espaço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="50015-139">Indicates whether the property or class requires a large amount of storage space.</span></span> <span data-ttu-id="50015-140">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="50015-140">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="50015-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Não \_ nulo**</span><span class="sxs-lookup"><span data-stu-id="50015-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Not\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="50015-142">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="50015-142">Data type: **boolean**</span></span>

<span data-ttu-id="50015-143">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="50015-143">Applies to: properties</span></span>

<span data-ttu-id="50015-144">Indica se uma propriedade de classe não pode assumir um valor **nulo** (**VT \_ NULL**).</span><span class="sxs-lookup"><span data-stu-id="50015-144">Indicates whether a class property cannot take on a value of **NULL** (**VT\_NULL**).</span></span> <span data-ttu-id="50015-145">Somente o valor **true** (padrão) é permitido.</span><span class="sxs-lookup"><span data-stu-id="50015-145">Only the value **TRUE** (default) is allowed.</span></span>

<span data-ttu-id="50015-146">Se esse qualificador for especificado, o WMI não permitirá a criação de instâncias com a propriedade definida como **NULL**, e as propriedades **nulas** retornarão o código de erro **\_ \_ \_ nulo E o WBEM** .</span><span class="sxs-lookup"><span data-stu-id="50015-146">If this qualifier is specified, WMI does not allow creation of instances with the property set to **NULL**, and **NULL** properties return the **WBEM\_E\_ILLEGAL\_NULL** error code.</span></span>

<span data-ttu-id="50015-147">Observe que os qualificadores de [**chave**](standard-qualifiers.md) e **indexados** já implicam esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="50015-147">Note that the [**Key**](standard-qualifiers.md) and **Indexed** qualifiers already imply this behavior.</span></span>

</dd> <dt>

<span data-ttu-id="50015-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Operador**</span><span class="sxs-lookup"><span data-stu-id="50015-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="50015-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50015-149">Data type: **string**</span></span>

<span data-ttu-id="50015-150">Aplica-se a: qualquer</span><span class="sxs-lookup"><span data-stu-id="50015-150">Applies to: Any</span></span>

<span data-ttu-id="50015-151">Indicação de que o elemento de esquema é dinâmico e, portanto, preenchido por um provedor.</span><span class="sxs-lookup"><span data-stu-id="50015-151">Indication that the schema element is dynamic and thus populated by a provider.</span></span> <span data-ttu-id="50015-152">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="50015-152">The default is **NULL**.</span></span> <span data-ttu-id="50015-153">Esse qualificador é um identificador específico da implementação para a instrumentação.</span><span class="sxs-lookup"><span data-stu-id="50015-153">This qualifier is an implementation-specific handle to the instrumentation.</span></span>

</dd> <dt>

<span data-ttu-id="50015-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Experimental**</span><span class="sxs-lookup"><span data-stu-id="50015-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Experimental**</span></span>
</dt> <dd>

<span data-ttu-id="50015-155">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="50015-155">Data type: **boolean**</span></span>

<span data-ttu-id="50015-156">Aplica-se a: qualquer</span><span class="sxs-lookup"><span data-stu-id="50015-156">Applies to: any</span></span>

<span data-ttu-id="50015-157">Indica que o elemento especificado foi proposto para fazer parte de uma versão futura dos esquemas CIM, mas ainda não faz parte do esquema padrão.</span><span class="sxs-lookup"><span data-stu-id="50015-157">Indicates that the specified element has been proposed to be a part of a future release of the CIM Schemas, but is not yet part of the standard Schema.</span></span> <span data-ttu-id="50015-158">Em vez disso, o elemento está disponível para que os usuários testem, implementem e forneçam comentários sobre o.</span><span class="sxs-lookup"><span data-stu-id="50015-158">Instead, the element is available for users to experiment, implement, and provide feedback on.</span></span> <span data-ttu-id="50015-159">Com base nos comentários, o elemento pode ser adicionado ao padrão, conforme apresentado, modificado ou removido.</span><span class="sxs-lookup"><span data-stu-id="50015-159">Based on feedback, the element may added to the standard as presented, modified, or removed.</span></span> <span data-ttu-id="50015-160">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="50015-160">The default is **FALSE**.</span></span> <span data-ttu-id="50015-161">Uma implementação não precisa dar suporte a um elemento com este qualificador.</span><span class="sxs-lookup"><span data-stu-id="50015-161">An implementation does not have to support an element with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="50015-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="50015-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="50015-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50015-163">Data type: **string**</span></span>

<span data-ttu-id="50015-164">Aplica-se a: Propriedades, referências, métodos, parâmetros</span><span class="sxs-lookup"><span data-stu-id="50015-164">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="50015-165">Tipo específico atribuído a um item de dados.</span><span class="sxs-lookup"><span data-stu-id="50015-165">Specific type assigned to a data item.</span></span> <span data-ttu-id="50015-166">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="50015-166">The default is **NULL**.</span></span>

<span data-ttu-id="50015-167">Uso: você deve usar o qualificador **syntaxtype** com este qualificador.</span><span class="sxs-lookup"><span data-stu-id="50015-167">Usage: You must use the **SyntaxType** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="50015-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**Sintaxetype**</span><span class="sxs-lookup"><span data-stu-id="50015-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**</span></span>
</dt> <dd>

<span data-ttu-id="50015-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50015-169">Data type: **string**</span></span>

<span data-ttu-id="50015-170">Aplica-se a: Propriedades, referências, métodos, parâmetros</span><span class="sxs-lookup"><span data-stu-id="50015-170">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="50015-171">Formato do qualificador de **sintaxe** .</span><span class="sxs-lookup"><span data-stu-id="50015-171">Format of the **Syntax** qualifier.</span></span> <span data-ttu-id="50015-172">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="50015-172">The default is **NULL**.</span></span>

<span data-ttu-id="50015-173">Uso: você deve usar o qualificador de **sintaxe** com este qualificador.</span><span class="sxs-lookup"><span data-stu-id="50015-173">Usage: You must use the **Syntax** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="50015-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="50015-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="50015-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50015-175">Data type: **string**</span></span>

<span data-ttu-id="50015-176">Aplica-se a: classes, propriedades, métodos, associações, indicações, referências</span><span class="sxs-lookup"><span data-stu-id="50015-176">Applies to: classes, properties, methods, associations, indications, references</span></span>

<span data-ttu-id="50015-177">Circunstâncias sob as quais um gatilho é acionado.</span><span class="sxs-lookup"><span data-stu-id="50015-177">Circumstances under which a trigger is fired.</span></span> <span data-ttu-id="50015-178">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="50015-178">The default is **NULL**.</span></span> <span data-ttu-id="50015-179">Os tipos de gatilho variam de acordo com a construção do metamodelo.</span><span class="sxs-lookup"><span data-stu-id="50015-179">The trigger types vary by meta-model construct.</span></span>

<span data-ttu-id="50015-180">Para classes e associações, os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="50015-180">For classes and associations, the legal values are:</span></span>

<span data-ttu-id="50015-181">Criar</span><span class="sxs-lookup"><span data-stu-id="50015-181">Create</span></span>

<span data-ttu-id="50015-182">Excluir</span><span class="sxs-lookup"><span data-stu-id="50015-182">Delete</span></span>

<span data-ttu-id="50015-183">Atualizar</span><span class="sxs-lookup"><span data-stu-id="50015-183">Update</span></span>

<span data-ttu-id="50015-184">Access</span><span class="sxs-lookup"><span data-stu-id="50015-184">Access</span></span>

<span data-ttu-id="50015-185">Para propriedades e referências, os valores válidos são: atualização e acesso.</span><span class="sxs-lookup"><span data-stu-id="50015-185">For properties and references, the legal values are: Update and Access.</span></span>

<span data-ttu-id="50015-186">Para métodos, os valores válidos são antes e depois.</span><span class="sxs-lookup"><span data-stu-id="50015-186">For methods, the legal values are Before and After.</span></span>

<span data-ttu-id="50015-187">Para indicações, o valor legal é gerado.</span><span class="sxs-lookup"><span data-stu-id="50015-187">For indications, the legal value is Thrown.</span></span>

</dd> <dt>

<span data-ttu-id="50015-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span><span class="sxs-lookup"><span data-stu-id="50015-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span></span>
</dt> <dd>

<span data-ttu-id="50015-189">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50015-189">Data type: **string array**</span></span>

<span data-ttu-id="50015-190">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="50015-190">Applies to: properties</span></span>

<span data-ttu-id="50015-191">Conjunto de valores que indica que o valor da propriedade associada é desconhecido (a propriedade não pode ser considerada como tendo um valor válido ou significativo).</span><span class="sxs-lookup"><span data-stu-id="50015-191">Set of values indicating that the value of the associated property is unknown (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="50015-192">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="50015-192">The default is **NULL**.</span></span>

<span data-ttu-id="50015-193">As convenções e restrições usadas para definir valores desconhecidos são as mesmas aplicáveis ao qualificador [**ValueMap**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="50015-193">The conventions and restrictions used for defining unknown values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="50015-194">Observe que esse qualificador não pode ser substituído.</span><span class="sxs-lookup"><span data-stu-id="50015-194">Note that this qualifier cannot be overridden.</span></span> <span data-ttu-id="50015-195">Não é razoável permitir que uma subclasse trate um valor como um valor conhecido quando tratado como desconhecido por alguma classe pai.</span><span class="sxs-lookup"><span data-stu-id="50015-195">It is unreasonable to permit a subclass to treat a value as a known value when it is treated as unknown by some parent class.</span></span>

</dd> <dt>

<span data-ttu-id="50015-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span><span class="sxs-lookup"><span data-stu-id="50015-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span></span>
</dt> <dd>

<span data-ttu-id="50015-197">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50015-197">Data type: **string array**</span></span>

<span data-ttu-id="50015-198">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="50015-198">Applies to: properties</span></span>

<span data-ttu-id="50015-199">Conjunto de valores que indica que o valor da propriedade associada não tem suporte (a propriedade não pode ser considerada como tendo um valor válido ou significativo).</span><span class="sxs-lookup"><span data-stu-id="50015-199">Set of values indicating that the value of the associated property is unsupported (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="50015-200">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="50015-200">The default is **NULL**.</span></span>

<span data-ttu-id="50015-201">As convenções e restrições usadas para definir valores sem suporte são as mesmas aplicáveis ao qualificador [**ValueMap**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="50015-201">The conventions and restrictions used for defining unsupported values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="50015-202">Observe que esse qualificador não pode ser substituído.</span><span class="sxs-lookup"><span data-stu-id="50015-202">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="50015-203">Não é razoável permitir que uma subclasse trate um valor como um valor com suporte que seja tratado como desconhecido por alguma classe pai.</span><span class="sxs-lookup"><span data-stu-id="50015-203">It is unreasonable to permit a subclass to treat a value as a supported value that is treated as unknown by some parent class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50015-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50015-204">Requirements</span></span>



| <span data-ttu-id="50015-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="50015-205">Requirement</span></span> | <span data-ttu-id="50015-206">Valor</span><span class="sxs-lookup"><span data-stu-id="50015-206">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="50015-207">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50015-207">Minimum supported client</span></span><br/> | <span data-ttu-id="50015-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50015-208">Windows Vista</span></span><br/>       |
| <span data-ttu-id="50015-209">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50015-209">Minimum supported server</span></span><br/> | <span data-ttu-id="50015-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50015-210">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50015-211">Confira também</span><span class="sxs-lookup"><span data-stu-id="50015-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50015-212">Qualificadores WMI</span><span class="sxs-lookup"><span data-stu-id="50015-212">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="50015-213">Adicionando um qualificador</span><span class="sxs-lookup"><span data-stu-id="50015-213">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




