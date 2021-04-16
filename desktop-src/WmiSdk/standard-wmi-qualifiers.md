---
description: O a seguir lista os qualificadores padrão específicos ao WMI.
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: Qualificadores WMI padrão
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
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782519"
---
# <a name="standard-wmi-qualifiers"></a><span data-ttu-id="42ae2-103">Qualificadores WMI padrão</span><span class="sxs-lookup"><span data-stu-id="42ae2-103">Standard WMI Qualifiers</span></span>

<span data-ttu-id="42ae2-104">O a seguir lista os qualificadores padrão específicos ao WMI.</span><span class="sxs-lookup"><span data-stu-id="42ae2-104">The following lists standard qualifiers specific to WMI.</span></span>

<dt>

<span data-ttu-id="42ae2-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Aditamento**</span><span class="sxs-lookup"><span data-stu-id="42ae2-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Amendment**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-106">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-106">Data type: **boolean**</span></span>

<span data-ttu-id="42ae2-107">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="42ae2-107">Applies to: classes</span></span>

<span data-ttu-id="42ae2-108">Indica que uma classe contém qualificadores corrigidos que estão localizados.</span><span class="sxs-lookup"><span data-stu-id="42ae2-108">Indicates that a class contains amended qualifiers that are localized.</span></span> <span data-ttu-id="42ae2-109">O padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="42ae2-109">The default is **TRUE**.</span></span>

<span data-ttu-id="42ae2-110">A classe associada pode ser convertida.</span><span class="sxs-lookup"><span data-stu-id="42ae2-110">The associated class can be translated.</span></span> <span data-ttu-id="42ae2-111">Para acessar a versão traduzida, use o identificador de localidade para construir um nome de namespace.</span><span class="sxs-lookup"><span data-stu-id="42ae2-111">To access the translated version, use the locale identifier to construct a namespace name.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Ignorar \_ GetObject**</span><span class="sxs-lookup"><span data-stu-id="42ae2-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Bypass\_GetObject**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-113">Data type: **boolean**</span></span>

<span data-ttu-id="42ae2-114">Aplica-se a: métodos</span><span class="sxs-lookup"><span data-stu-id="42ae2-114">Applies to: methods</span></span>

<span data-ttu-id="42ae2-115">Indica que a chamada de método deve passar diretamente para a chamada **ExecMethodAsync** do provedor, em vez do provedor, primeiro fazendo uma chamada para **GetObject** para validar o caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="42ae2-115">Indicates that the method call should pass directly to the **ExecMethodAsync** call of the provider rather than the provider first making a call to **GetObject** to validate the object path.</span></span> <span data-ttu-id="42ae2-116">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="42ae2-116">The default is **FALSE**.</span></span> <span data-ttu-id="42ae2-117">Usar **bypass \_ GetObject** pode melhorar significativamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="42ae2-117">Using **Bypass\_GetObject** can significantly improve performance.</span></span>

<span data-ttu-id="42ae2-118">Antes de usar **ignorar \_ GetObject**, certifique-se de que nenhuma das seguintes ações seja executada:</span><span class="sxs-lookup"><span data-stu-id="42ae2-118">Before using **Bypass\_GetObject**, ensure that neither of the following actions are taken:</span></span>

-   <span data-ttu-id="42ae2-119">Derive uma classe da sua classe.</span><span class="sxs-lookup"><span data-stu-id="42ae2-119">Derive a class from your class.</span></span>
-   <span data-ttu-id="42ae2-120">Substitua o método que tem o qualificador **\_ GetObject de bypass** .</span><span class="sxs-lookup"><span data-stu-id="42ae2-120">Override the method that has the **Bypass\_GetObject** qualifier.</span></span>

<span data-ttu-id="42ae2-121">A falha em seguir essas precauções pode resultar na invocação da implementação do método da classe pai em vez da classe filho.</span><span class="sxs-lookup"><span data-stu-id="42ae2-121">Failure to follow these precautions can result in invoking the method implementation of the parent class instead of the child class.</span></span> <span data-ttu-id="42ae2-122">Para obter mais informações, consulte usando o \_ qualificador GetObject de bypass.</span><span class="sxs-lookup"><span data-stu-id="42ae2-122">For more information, see Using the Bypass\_GetObject Qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**\_Chave CIM**</span><span class="sxs-lookup"><span data-stu-id="42ae2-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**CIM\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-124">Tipo de dados: **CIM \_ booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-124">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="42ae2-125">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="42ae2-125">Applies to: properties</span></span>

<span data-ttu-id="42ae2-126">Indica que a propriedade associada é uma propriedade de chave no CIM, mas não no WMI.</span><span class="sxs-lookup"><span data-stu-id="42ae2-126">Indicates that the associated property is a key property in CIM but not in WMI.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="42ae2-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-128">Tipo de dados: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="42ae2-128">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="42ae2-129">Aplica-se a: Propriedades, métodos, parâmetros</span><span class="sxs-lookup"><span data-stu-id="42ae2-129">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="42ae2-130">Contém o texto que descreve o tipo de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="42ae2-130">Contains text describing the type of a property.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span><span class="sxs-lookup"><span data-stu-id="42ae2-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-132">Tipo de dados: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="42ae2-132">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="42ae2-133">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="42ae2-133">Applies to: classes</span></span>

<span data-ttu-id="42ae2-134">Indica que uma classe tem instâncias associadas a mais informações fornecidas dinamicamente por um provedor.</span><span class="sxs-lookup"><span data-stu-id="42ae2-134">Indicates that a class has instances associated with more information dynamically supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Preterido**</span><span class="sxs-lookup"><span data-stu-id="42ae2-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Deprecated**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-136">Tipo de dados: **CIM \_ booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-136">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="42ae2-137">Aplica-se a: Propriedades, classes</span><span class="sxs-lookup"><span data-stu-id="42ae2-137">Applies to: properties, classes</span></span>

<span data-ttu-id="42ae2-138">Indica que a propriedade foi substituída por outra propriedade.</span><span class="sxs-lookup"><span data-stu-id="42ae2-138">Indicates the property has been superseded by another property.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Display**</span><span class="sxs-lookup"><span data-stu-id="42ae2-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Display**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-140">Aplica-se a: classes, propriedades</span><span class="sxs-lookup"><span data-stu-id="42ae2-140">Applies to: classes, properties</span></span>

<span data-ttu-id="42ae2-141">O **UUID** da classe associada.</span><span class="sxs-lookup"><span data-stu-id="42ae2-141">The **UUID** of the associated class.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dinâmico**](dynamic-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="42ae2-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dynamic**](dynamic-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-143">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-143">Data type: **boolean**</span></span>

<span data-ttu-id="42ae2-144">Aplica-se a: classes, propriedades</span><span class="sxs-lookup"><span data-stu-id="42ae2-144">Applies to: classes, properties</span></span>

<span data-ttu-id="42ae2-145">Indica uma classe cujas instâncias são criadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="42ae2-145">Indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="42ae2-146">O valor desse qualificador deve ser definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="42ae2-146">The value of this qualifier must be set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span><span class="sxs-lookup"><span data-stu-id="42ae2-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-148">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-148">Data type: **boolean**</span></span>

<span data-ttu-id="42ae2-149">Aplica-se a: classes, instâncias</span><span class="sxs-lookup"><span data-stu-id="42ae2-149">Applies to: classes, instances</span></span>

<span data-ttu-id="42ae2-150">Indica que uma instância contém valores fornecidos por provedores de propriedades dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="42ae2-150">Indicates that an instance contains values provided by dynamic property providers.</span></span> <span data-ttu-id="42ae2-151">O padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="42ae2-151">The default is **TRUE**.</span></span>

<span data-ttu-id="42ae2-152">Você deve especificar esse qualificador em uma instância desse tipo.</span><span class="sxs-lookup"><span data-stu-id="42ae2-152">You must specify this qualifier on such an instance.</span></span> <span data-ttu-id="42ae2-153">Somente o valor **true** é permitido.</span><span class="sxs-lookup"><span data-stu-id="42ae2-153">Only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Fixado**</span><span class="sxs-lookup"><span data-stu-id="42ae2-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Fixed**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-155">Tipo de dados: **CIM \_ booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-155">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="42ae2-156">Aplica-se a: instâncias</span><span class="sxs-lookup"><span data-stu-id="42ae2-156">Applies to: instances</span></span>

<span data-ttu-id="42ae2-157">Indica que o valor dessa propriedade não pode ser alterado durante o tempo de vida da instância.</span><span class="sxs-lookup"><span data-stu-id="42ae2-157">Indicates that the value of this property cannot change during the lifetime of the instance.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-158"><span id="ID"></span><span id="id"></span>**SESSÃO**</span><span class="sxs-lookup"><span data-stu-id="42ae2-158"><span id="ID"></span><span id="id"></span>**ID**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-159">Tipo de dados: **VT \_ i4**</span><span class="sxs-lookup"><span data-stu-id="42ae2-159">Data type: **VT\_I4**</span></span>

<span data-ttu-id="42ae2-160">Aplica-se a: Propriedades, parâmetros</span><span class="sxs-lookup"><span data-stu-id="42ae2-160">Applies to: properties, parameters</span></span>

<span data-ttu-id="42ae2-161">Identifica e sequencia exclusivamente um parâmetro de propriedade ou método quando as instruções MOF são geradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="42ae2-161">Uniquely identifies and sequences a property or method parameter when MOF statements are generated automatically.</span></span>

<span data-ttu-id="42ae2-162">Esse qualificador é necessário apenas para parâmetros de método.</span><span class="sxs-lookup"><span data-stu-id="42ae2-162">This qualifier is required for method parameters only.</span></span> <span data-ttu-id="42ae2-163">Ao criar parâmetros para um método, os designers de classe devem começar com ID (0) para o primeiro parâmetro e usar cada inteiro sucessivo para cada parâmetro sucessivo.</span><span class="sxs-lookup"><span data-stu-id="42ae2-163">When creating parameters for a method, class designers should begin with Id(0) for the first parameter and use each successive integer for each successive parameter.</span></span> <span data-ttu-id="42ae2-164">Se os qualificadores de **ID** forem omitidos involuntariamente, o compilador MOF gerará qualificadores de **ID** automaticamente.</span><span class="sxs-lookup"><span data-stu-id="42ae2-164">If the **ID** qualifiers are unintentionally omitted, the MOF compiler generates **ID** qualifiers automatically.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implementado**</span><span class="sxs-lookup"><span data-stu-id="42ae2-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-166">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-166">Data type: **boolean**</span></span>

<span data-ttu-id="42ae2-167">Aplica-se a: métodos</span><span class="sxs-lookup"><span data-stu-id="42ae2-167">Applies to: methods</span></span>

<span data-ttu-id="42ae2-168">Indica que um método tem uma implementação fornecida por um provedor.</span><span class="sxs-lookup"><span data-stu-id="42ae2-168">Indicates that a method has an implementation supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span><span class="sxs-lookup"><span data-stu-id="42ae2-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-170">Tipo de dados: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="42ae2-170">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="42ae2-171">Aplica-se a: instâncias</span><span class="sxs-lookup"><span data-stu-id="42ae2-171">Applies to: instances</span></span>

<span data-ttu-id="42ae2-172">Indica que uma instância contém valores fornecidos por um provedor de propriedades dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="42ae2-172">Indicates that an instance contains values provided by a dynamic property provider.</span></span>

<span data-ttu-id="42ae2-173">O valor é passado para o provedor de propriedades como um argumento para o método [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="42ae2-173">The value is passed to the property provider as an argument to the [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) method.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Localidade**</span><span class="sxs-lookup"><span data-stu-id="42ae2-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-175">Tipo de dados: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="42ae2-175">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="42ae2-176">Aplica-se a: classes ou instâncias</span><span class="sxs-lookup"><span data-stu-id="42ae2-176">Applies to: classes or instances</span></span>

<span data-ttu-id="42ae2-177">Especifica o idioma de origem para uma classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="42ae2-177">Specifies the language of origin for a class or instance.</span></span> <span data-ttu-id="42ae2-178">Para obter mais informações sobre valores de localidade, consulte [códigos de localidade](#locale-codes).</span><span class="sxs-lookup"><span data-stu-id="42ae2-178">For more information about locale values, see [Locale Codes](#locale-codes).</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span><span class="sxs-lookup"><span data-stu-id="42ae2-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-180">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42ae2-180">Data type: **string array**</span></span>

<span data-ttu-id="42ae2-181">Aplica-se a: instâncias de namespace</span><span class="sxs-lookup"><span data-stu-id="42ae2-181">Applies to: namespace instances</span></span>

<span data-ttu-id="42ae2-182">Especifica um descritor de segurança para o namespace no formato [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="42ae2-182">Specifies a security descriptor for the namespace in [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span> <span data-ttu-id="42ae2-183">Para obter mais informações, consulte [definindo a segurança do namespace quando o namespace é criado](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="42ae2-183">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span> <span data-ttu-id="42ae2-184">A cadeia de caracteres SDDL é processada pelo WMI para estabelecer a segurança do namespace, mas não é armazenada como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="42ae2-184">The SDDL string is processed by WMI to establish the namespace security but not stored as a string.</span></span> <span data-ttu-id="42ae2-185">Se nenhum descritor de segurança for especificado, a segurança padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="42ae2-185">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="42ae2-186">Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="42ae2-186">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Adicional**</span><span class="sxs-lookup"><span data-stu-id="42ae2-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Optional**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-188">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-188">Data type: **boolean**</span></span>

<span data-ttu-id="42ae2-189">Aplica-se a: parâmetros</span><span class="sxs-lookup"><span data-stu-id="42ae2-189">Applies to: parameters</span></span>

<span data-ttu-id="42ae2-190">Indica que um parâmetro não é necessário e que tem um valor padrão com bom desempenho.</span><span class="sxs-lookup"><span data-stu-id="42ae2-190">Indicates that a parameter is not required, and that it has a well-behaved default value.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Direitos**</span><span class="sxs-lookup"><span data-stu-id="42ae2-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Privileges**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-192">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42ae2-192">Data type: **string array**</span></span>

<span data-ttu-id="42ae2-193">Aplica-se a: Propriedades, métodos</span><span class="sxs-lookup"><span data-stu-id="42ae2-193">Applies to: properties, methods</span></span>

<span data-ttu-id="42ae2-194">Conjunto de valores usado para informar ao cliente quais privilégios são necessários para criar instâncias, preencher propriedades ou executar métodos.</span><span class="sxs-lookup"><span data-stu-id="42ae2-194">Set of values used to inform the client which privileges are required to create instances, fill in properties, or perform methods.</span></span> <span data-ttu-id="42ae2-195">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="42ae2-195">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**</span><span class="sxs-lookup"><span data-stu-id="42ae2-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-197">Tipo de dados: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="42ae2-197">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="42ae2-198">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="42ae2-198">Applies to: properties</span></span>

<span data-ttu-id="42ae2-199">Indica que uma propriedade de instância contém valores fornecidos por provedores de propriedades dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="42ae2-199">Indicates that an instance property contains values provided by dynamic property providers.</span></span>

<span data-ttu-id="42ae2-200">Você deve especificar esse qualificador nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="42ae2-200">You must specify this qualifier on such a property.</span></span> <span data-ttu-id="42ae2-201">O valor é passado para o provedor de propriedades como um argumento para [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span><span class="sxs-lookup"><span data-stu-id="42ae2-201">The value is passed to the property provider as an argument to [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Operador**</span><span class="sxs-lookup"><span data-stu-id="42ae2-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-203">Tipo de dados: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="42ae2-203">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="42ae2-204">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="42ae2-204">Applies to: classes</span></span>

<span data-ttu-id="42ae2-205">O valor desse qualificador é o nome do provedor dinâmico que fornece instâncias de classe e atualiza os dados da instância.</span><span class="sxs-lookup"><span data-stu-id="42ae2-205">The value of this qualifier is the name of the dynamic provider that provides class instances and refreshes instance data.</span></span> <span data-ttu-id="42ae2-206">Esse nome deve ser registrado com WMI criando uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) com a propriedade **Name** que contém esse nome.</span><span class="sxs-lookup"><span data-stu-id="42ae2-206">This name must be registered with WMI by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) class with the **Name** property containing this name.</span></span> <span data-ttu-id="42ae2-207">Quando esse qualificador é especificado em uma classe cujas instâncias são fornecidas dinamicamente, o qualificador **dinâmico** também deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="42ae2-207">When this qualifier is specified on a class whose instances are provided dynamically, the **Dynamic** qualifier must also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span><span class="sxs-lookup"><span data-stu-id="42ae2-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-209">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-209">Data type: **boolean**</span></span>

<span data-ttu-id="42ae2-210">Aplica-se a: instâncias de namespace</span><span class="sxs-lookup"><span data-stu-id="42ae2-210">Applies to: namespace instances</span></span>

<span data-ttu-id="42ae2-211">Se definido como **true**, **RequiresEncryption** marca um namespace para que os aplicativos e scripts cliente devam se conectar com a autenticação criptografada.</span><span class="sxs-lookup"><span data-stu-id="42ae2-211">If set to **TRUE**, **RequiresEncryption** marks a namespace so that client applications and scripts must connect with encrypted authentication.</span></span> <span data-ttu-id="42ae2-212">O nível de autenticação deve ser definido para a **privacidade de PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C** em C++.</span><span class="sxs-lookup"><span data-stu-id="42ae2-212">The authentication level must be set to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** in C++.</span></span> <span data-ttu-id="42ae2-213">Em script ou Visual Basic, o nível de autenticação deve ser definido como **WbemAuthenticationLevelPktPrivacy**.</span><span class="sxs-lookup"><span data-stu-id="42ae2-213">In scripting or Visual Basic, authentication level must be set to **WbemAuthenticationLevelPktPrivacy**.</span></span> <span data-ttu-id="42ae2-214">Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="42ae2-214">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span> <span data-ttu-id="42ae2-215">O qualificador é usado no [*MOF*](gloss-m.md) com o comando de pré-processador do namespace pragma.</span><span class="sxs-lookup"><span data-stu-id="42ae2-215">The qualifier is used in [*MOF*](gloss-m.md) with the pragma namespace preprocessor command.</span></span>

<span data-ttu-id="42ae2-216">Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md) ou [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="42ae2-216">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md) or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="42ae2-217">Os níveis de autenticação de script são definidos em [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="42ae2-217">Scripting authentication levels are defined in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Único**</span><span class="sxs-lookup"><span data-stu-id="42ae2-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-219">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-219">Data type: **boolean**</span></span>

<span data-ttu-id="42ae2-220">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="42ae2-220">Applies to: classes</span></span>

<span data-ttu-id="42ae2-221">Designa uma classe que só pode ter uma instância do e que não contenha propriedades de chave.</span><span class="sxs-lookup"><span data-stu-id="42ae2-221">Designates a class that can only have one instance and that does not contain key properties.</span></span>

<span data-ttu-id="42ae2-222">Somente o valor **true** (padrão) é permitido.</span><span class="sxs-lookup"><span data-stu-id="42ae2-222">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Auto-estática**</span><span class="sxs-lookup"><span data-stu-id="42ae2-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Static**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-224">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42ae2-224">Data type: **boolean**</span></span>

<span data-ttu-id="42ae2-225">Aplica-se a: métodos</span><span class="sxs-lookup"><span data-stu-id="42ae2-225">Applies to: methods</span></span>

<span data-ttu-id="42ae2-226">Indica se um método pode ser chamado usando a definição de classe ou suas instâncias.</span><span class="sxs-lookup"><span data-stu-id="42ae2-226">Indicates whether a method can called by using the class definition or its instances.</span></span>

<span data-ttu-id="42ae2-227">O método não pode ser invocado de uma instância.</span><span class="sxs-lookup"><span data-stu-id="42ae2-227">The method cannot be invoked from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="42ae2-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**SubType**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-229">Tipo de dados: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="42ae2-229">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="42ae2-230">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="42ae2-230">Applies to: properties</span></span>

<span data-ttu-id="42ae2-231">Indica que uma propriedade do tipo **CIM \_ DateTime** representa um intervalo de tempo em vez de uma hora específica.</span><span class="sxs-lookup"><span data-stu-id="42ae2-231">Indicates that a property of type **CIM\_DATETIME** represents a time interval rather than a specific time.</span></span>

<span data-ttu-id="42ae2-232">Para identificar a propriedade como um intervalo, o valor desse qualificador deve ser "Interval".</span><span class="sxs-lookup"><span data-stu-id="42ae2-232">To identify the property as an interval, the value of this qualifier must be "interval".</span></span> <span data-ttu-id="42ae2-233">Todos os outros valores para esse qualificador são reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="42ae2-233">All other values for this qualifier are reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-234"><span id="UUID"></span><span id="uuid"></span>**PERSONALIZADO**</span><span class="sxs-lookup"><span data-stu-id="42ae2-234"><span id="UUID"></span><span id="uuid"></span>**UUID**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42ae2-235">Data type: **string**</span></span>

<span data-ttu-id="42ae2-236">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="42ae2-236">Applies to: classes</span></span>

<span data-ttu-id="42ae2-237">Identificador Universal exclusivo aplicado à classe.</span><span class="sxs-lookup"><span data-stu-id="42ae2-237">Universally unique identifier applied to the class.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span><span class="sxs-lookup"><span data-stu-id="42ae2-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-239">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42ae2-239">Data type: **string**</span></span>

<span data-ttu-id="42ae2-240">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="42ae2-240">Applies to: classes</span></span>

<span data-ttu-id="42ae2-241">O número de versão do objeto de classe.</span><span class="sxs-lookup"><span data-stu-id="42ae2-241">The version number of the class object.</span></span> <span data-ttu-id="42ae2-242">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="42ae2-242">The default is **NULL**.</span></span> <span data-ttu-id="42ae2-243">O número de versão é incrementado quando são feitas alterações na classe.</span><span class="sxs-lookup"><span data-stu-id="42ae2-243">The version number is incremented when changes are made to the class.</span></span>

</dd> <dt>

<span data-ttu-id="42ae2-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span><span class="sxs-lookup"><span data-stu-id="42ae2-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="42ae2-245">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42ae2-245">Data type: **string array**</span></span>

<span data-ttu-id="42ae2-246">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="42ae2-246">Applies to: properties</span></span>

<span data-ttu-id="42ae2-247">Conjunto de valores que indica quais privilégios do sistema devem estar disponíveis e habilitados para uma operação de gravação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="42ae2-247">Set of values indicating which system privileges must be available and enabled for a successful write operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42ae2-248">Comentários</span><span class="sxs-lookup"><span data-stu-id="42ae2-248">Remarks</span></span>

### <a name="locale-codes"></a><span data-ttu-id="42ae2-249">Códigos de localidade</span><span class="sxs-lookup"><span data-stu-id="42ae2-249">Locale Codes</span></span>

<span data-ttu-id="42ae2-250">Um código de localidade tem o formato "MS \_ <Three Digit Language ID> ".</span><span class="sxs-lookup"><span data-stu-id="42ae2-250">A locale code is of the form "MS\_<Three Digit Language ID>".</span></span> <span data-ttu-id="42ae2-251">Por exemplo, a localidade inglês é MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="42ae2-251">For example, English locale is MS\_409.</span></span> <span data-ttu-id="42ae2-252">A tabela a seguir lista as IDs de idioma.</span><span class="sxs-lookup"><span data-stu-id="42ae2-252">The following table lists the language IDs.</span></span>



| <span data-ttu-id="42ae2-253">Idioma</span><span class="sxs-lookup"><span data-stu-id="42ae2-253">Language</span></span>              | <span data-ttu-id="42ae2-254">ID do idioma (hexadecimal)</span><span class="sxs-lookup"><span data-stu-id="42ae2-254">Language ID (hexadecimal)</span></span> |
|-----------------------|---------------------------|
| <span data-ttu-id="42ae2-255">Árabe</span><span class="sxs-lookup"><span data-stu-id="42ae2-255">Arabic</span></span>                | <span data-ttu-id="42ae2-256">401</span><span class="sxs-lookup"><span data-stu-id="42ae2-256">401</span></span>                       |
| <span data-ttu-id="42ae2-257">Português (Brasil)</span><span class="sxs-lookup"><span data-stu-id="42ae2-257">Portuguese (Brazil)</span></span>   | <span data-ttu-id="42ae2-258">416</span><span class="sxs-lookup"><span data-stu-id="42ae2-258">416</span></span>                       |
| <span data-ttu-id="42ae2-259">Chinês (Simplificado)</span><span class="sxs-lookup"><span data-stu-id="42ae2-259">Chinese (Simplified)</span></span>  | <span data-ttu-id="42ae2-260">804</span><span class="sxs-lookup"><span data-stu-id="42ae2-260">804</span></span>                       |
| <span data-ttu-id="42ae2-261">Chinês (Tradicional)</span><span class="sxs-lookup"><span data-stu-id="42ae2-261">Chinese (Traditional)</span></span> | <span data-ttu-id="42ae2-262">404</span><span class="sxs-lookup"><span data-stu-id="42ae2-262">404</span></span>                       |
| <span data-ttu-id="42ae2-263">Tcheco</span><span class="sxs-lookup"><span data-stu-id="42ae2-263">Czech</span></span>                 | <span data-ttu-id="42ae2-264">405</span><span class="sxs-lookup"><span data-stu-id="42ae2-264">405</span></span>                       |
| <span data-ttu-id="42ae2-265">Dinamarquês</span><span class="sxs-lookup"><span data-stu-id="42ae2-265">Danish</span></span>                | <span data-ttu-id="42ae2-266">406</span><span class="sxs-lookup"><span data-stu-id="42ae2-266">406</span></span>                       |
| <span data-ttu-id="42ae2-267">Holandês</span><span class="sxs-lookup"><span data-stu-id="42ae2-267">Dutch</span></span>                 | <span data-ttu-id="42ae2-268">413</span><span class="sxs-lookup"><span data-stu-id="42ae2-268">413</span></span>                       |
| <span data-ttu-id="42ae2-269">Inglês (padrão)</span><span class="sxs-lookup"><span data-stu-id="42ae2-269">English (default)</span></span>     | <span data-ttu-id="42ae2-270">409</span><span class="sxs-lookup"><span data-stu-id="42ae2-270">409</span></span>                       |
| <span data-ttu-id="42ae2-271">Finlandês</span><span class="sxs-lookup"><span data-stu-id="42ae2-271">Finnish</span></span>               | <span data-ttu-id="42ae2-272">40b</span><span class="sxs-lookup"><span data-stu-id="42ae2-272">40b</span></span>                       |
| <span data-ttu-id="42ae2-273">Francês</span><span class="sxs-lookup"><span data-stu-id="42ae2-273">French</span></span>                | <span data-ttu-id="42ae2-274">40c</span><span class="sxs-lookup"><span data-stu-id="42ae2-274">40c</span></span>                       |
| <span data-ttu-id="42ae2-275">Alemão</span><span class="sxs-lookup"><span data-stu-id="42ae2-275">German</span></span>                | <span data-ttu-id="42ae2-276">407</span><span class="sxs-lookup"><span data-stu-id="42ae2-276">407</span></span>                       |
| <span data-ttu-id="42ae2-277">Grego</span><span class="sxs-lookup"><span data-stu-id="42ae2-277">Greek</span></span>                 | <span data-ttu-id="42ae2-278">408</span><span class="sxs-lookup"><span data-stu-id="42ae2-278">408</span></span>                       |
| <span data-ttu-id="42ae2-279">Hebraico</span><span class="sxs-lookup"><span data-stu-id="42ae2-279">Hebrew</span></span>                | <span data-ttu-id="42ae2-280">40d</span><span class="sxs-lookup"><span data-stu-id="42ae2-280">40d</span></span>                       |
| <span data-ttu-id="42ae2-281">Húngaro</span><span class="sxs-lookup"><span data-stu-id="42ae2-281">Hungarian</span></span>             | <span data-ttu-id="42ae2-282">40e</span><span class="sxs-lookup"><span data-stu-id="42ae2-282">40e</span></span>                       |
| <span data-ttu-id="42ae2-283">Italiano</span><span class="sxs-lookup"><span data-stu-id="42ae2-283">Italian</span></span>               | <span data-ttu-id="42ae2-284">410</span><span class="sxs-lookup"><span data-stu-id="42ae2-284">410</span></span>                       |
| <span data-ttu-id="42ae2-285">Japonês</span><span class="sxs-lookup"><span data-stu-id="42ae2-285">Japanese</span></span>              | <span data-ttu-id="42ae2-286">411</span><span class="sxs-lookup"><span data-stu-id="42ae2-286">411</span></span>                       |
| <span data-ttu-id="42ae2-287">Coreano</span><span class="sxs-lookup"><span data-stu-id="42ae2-287">Korean</span></span>                | <span data-ttu-id="42ae2-288">412</span><span class="sxs-lookup"><span data-stu-id="42ae2-288">412</span></span>                       |
| <span data-ttu-id="42ae2-289">Norueguês</span><span class="sxs-lookup"><span data-stu-id="42ae2-289">Norwegian</span></span>             | <span data-ttu-id="42ae2-290">414</span><span class="sxs-lookup"><span data-stu-id="42ae2-290">414</span></span>                       |
| <span data-ttu-id="42ae2-291">Polonês</span><span class="sxs-lookup"><span data-stu-id="42ae2-291">Polish</span></span>                | <span data-ttu-id="42ae2-292">415</span><span class="sxs-lookup"><span data-stu-id="42ae2-292">415</span></span>                       |
| <span data-ttu-id="42ae2-293">Português (Portugal)</span><span class="sxs-lookup"><span data-stu-id="42ae2-293">Portuguese (Portugal)</span></span> | <span data-ttu-id="42ae2-294">816</span><span class="sxs-lookup"><span data-stu-id="42ae2-294">816</span></span>                       |
| <span data-ttu-id="42ae2-295">Russo</span><span class="sxs-lookup"><span data-stu-id="42ae2-295">Russian</span></span>               | <span data-ttu-id="42ae2-296">419</span><span class="sxs-lookup"><span data-stu-id="42ae2-296">419</span></span>                       |
| <span data-ttu-id="42ae2-297">Espanhol</span><span class="sxs-lookup"><span data-stu-id="42ae2-297">Spanish</span></span>               | <span data-ttu-id="42ae2-298">c0a</span><span class="sxs-lookup"><span data-stu-id="42ae2-298">c0a</span></span>                       |
| <span data-ttu-id="42ae2-299">Sueco</span><span class="sxs-lookup"><span data-stu-id="42ae2-299">Swedish</span></span>               | <span data-ttu-id="42ae2-300">41D</span><span class="sxs-lookup"><span data-stu-id="42ae2-300">41D</span></span>                       |
| <span data-ttu-id="42ae2-301">Turco</span><span class="sxs-lookup"><span data-stu-id="42ae2-301">Turkish</span></span>               | <span data-ttu-id="42ae2-302">41f</span><span class="sxs-lookup"><span data-stu-id="42ae2-302">41f</span></span>                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a><span data-ttu-id="42ae2-303">Usando o \_ qualificador GetObject de bypass</span><span class="sxs-lookup"><span data-stu-id="42ae2-303">Using the Bypass\_GetObject Qualifier</span></span>

<span data-ttu-id="42ae2-304">Usar o qualificador **\_ GetObject de bypass** em um método pode gerar resultados confusos.</span><span class="sxs-lookup"><span data-stu-id="42ae2-304">Using the **Bypass\_GetObject** qualifier on a method can produce confusing results.</span></span>

<span data-ttu-id="42ae2-305">O exemplo a seguir define as classes **Shape** e **Circle** .</span><span class="sxs-lookup"><span data-stu-id="42ae2-305">The following example defines the **Shape** and **Circle** classes.</span></span> <span data-ttu-id="42ae2-306">Observe que a classe **Circle** é derivada da classe **Shape** .</span><span class="sxs-lookup"><span data-stu-id="42ae2-306">Note that the **Circle** class is derived from the **Shape** class.</span></span>


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



<span data-ttu-id="42ae2-307">A seguinte chamada para **ExecMethod** usa um objeto **Circle** chamado "mycircle" para desenhar um círculo.</span><span class="sxs-lookup"><span data-stu-id="42ae2-307">The following call to **ExecMethod** uses a **Circle** object named "MyCircle" to draw a circle.</span></span>


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



<span data-ttu-id="42ae2-308">No cenário anterior, o WMI chama **GetObject**; descobre que "Shape. Name = ' mycircle '" é um **círculo**; e executa a implementação de **círculo** de **DrawIt**.</span><span class="sxs-lookup"><span data-stu-id="42ae2-308">In the previous scenario, WMI calls **GetObject**; discovers that "Shape.Name='MyCircle'" is a **Circle**; and executes the **Circle** implementation of **DrawIt**.</span></span> <span data-ttu-id="42ae2-309">No entanto, se você usar o qualificador **\_ GetObject de bypass** em **DrawIt**, o WMI não chamará **GetObject**, não descobrirá que "Shape. Name = ' mycircle '" é um **círculo** e executará a implementação de **forma** de **DrawIt** em vez da implementação de **Circle** de **DrawIt**.</span><span class="sxs-lookup"><span data-stu-id="42ae2-309">However, if you use the **Bypass\_GetObject** qualifier on **DrawIt**, WMI does not call **GetObject**, does not discover that "Shape.Name='MyCircle'" is a **Circle**, and executes the **Shape** implementation of **DrawIt** instead of the **Circle** implementation of **DrawIt**.</span></span>

<span data-ttu-id="42ae2-310">A chamada a seguir para **ExecMethod** sempre invoca a implementação correta de **DrawIt**.</span><span class="sxs-lookup"><span data-stu-id="42ae2-310">The following call to **ExecMethod** always invokes the correct implementation of **DrawIt**.</span></span>


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a><span data-ttu-id="42ae2-311">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42ae2-311">Requirements</span></span>



| <span data-ttu-id="42ae2-312">Requisito</span><span class="sxs-lookup"><span data-stu-id="42ae2-312">Requirement</span></span> | <span data-ttu-id="42ae2-313">Valor</span><span class="sxs-lookup"><span data-stu-id="42ae2-313">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="42ae2-314">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42ae2-314">Minimum supported client</span></span><br/> | <span data-ttu-id="42ae2-315">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42ae2-315">Windows Vista</span></span><br/>       |
| <span data-ttu-id="42ae2-316">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42ae2-316">Minimum supported server</span></span><br/> | <span data-ttu-id="42ae2-317">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42ae2-317">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42ae2-318">Confira também</span><span class="sxs-lookup"><span data-stu-id="42ae2-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ae2-319">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="42ae2-319">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="42ae2-320">Qualificadores WMI</span><span class="sxs-lookup"><span data-stu-id="42ae2-320">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="42ae2-321">Adicionando um qualificador</span><span class="sxs-lookup"><span data-stu-id="42ae2-321">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

