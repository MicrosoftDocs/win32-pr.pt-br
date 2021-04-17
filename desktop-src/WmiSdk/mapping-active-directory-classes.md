---
description: Fornece regras para mapeamento de classes WMI para Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Mapeando classes de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a606cfacc2e9d56ef07973df182f5ce1a65be35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811988"
---
# <a name="mapping-active-directory-classes"></a><span data-ttu-id="c55b2-103">Mapeando classes de Active Directory</span><span class="sxs-lookup"><span data-stu-id="c55b2-103">Mapping Active Directory Classes</span></span>

<span data-ttu-id="c55b2-104">Como Active Directory tem uma ampla variedade de objetos possíveis, o WMI não pode criar um mapeamento direto de um para um.</span><span class="sxs-lookup"><span data-stu-id="c55b2-104">Because Active Directory has a wide variety of possible objects, WMI cannot create a direct one-to-one mapping.</span></span> <span data-ttu-id="c55b2-105">Em vez disso, o provedor de serviços de diretório usa regras para mapear classes entre as duas tecnologias.</span><span class="sxs-lookup"><span data-stu-id="c55b2-105">Instead, the Directory Services provider uses rules to map classes between the two technologies.</span></span>

<span data-ttu-id="c55b2-106">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="c55b2-106">This following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="c55b2-107">Classes de mapeamento</span><span class="sxs-lookup"><span data-stu-id="c55b2-107">Mapping Classes</span></span>](#mapping-classes)
-   [<span data-ttu-id="c55b2-108">Atributos de mapeamento</span><span class="sxs-lookup"><span data-stu-id="c55b2-108">Mapping Attributes</span></span>](#mapping-attributes)
-   [<span data-ttu-id="c55b2-109">Classes de associação</span><span class="sxs-lookup"><span data-stu-id="c55b2-109">Association Classes</span></span>](#association-classes)

> [!Note]  
> <span data-ttu-id="c55b2-110">Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="c55b2-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

## <a name="mapping-classes"></a><span data-ttu-id="c55b2-111">Classes de mapeamento</span><span class="sxs-lookup"><span data-stu-id="c55b2-111">Mapping Classes</span></span>

<span data-ttu-id="c55b2-112">A lista a seguir descreve as diretrizes que o provedor de serviços de diretório usa para mapear Active Directory classes para classes WMI:</span><span class="sxs-lookup"><span data-stu-id="c55b2-112">The following list describes the guidelines that the Directory Services provider uses to map Active Directory classes to WMI classes:</span></span>

-   <span data-ttu-id="c55b2-113">Cada classe abstrata no esquema de Active Directory é mapeada para uma classe abstrata no esquema WMI.</span><span class="sxs-lookup"><span data-stu-id="c55b2-113">Each abstract class in the Active Directory schema maps to one abstract class in the WMI schema.</span></span>

    <span data-ttu-id="c55b2-114">No esquema WMI, cada classe abstrata é prefixada com DS \_ .</span><span class="sxs-lookup"><span data-stu-id="c55b2-114">In the WMI schema, each abstract class is prefixed with DS\_.</span></span> <span data-ttu-id="c55b2-115">Por exemplo, a classe **Person** do esquema de Active Directory é mapeada para a classe WMI **\_ Person do DS** .</span><span class="sxs-lookup"><span data-stu-id="c55b2-115">For example, the **person** class from the Active Directory schema maps to the **DS\_person** WMI class.</span></span>

-   <span data-ttu-id="c55b2-116">Cada classe não abstrata do esquema de Active Directory mapeia para as duas classes a seguir no esquema WMI:</span><span class="sxs-lookup"><span data-stu-id="c55b2-116">Each nonabstract class from the Active Directory schema maps to the following two classes in the WMI schema:</span></span>

    -   <span data-ttu-id="c55b2-117">A primeira classe mapeada é prefixada com anúncios \_ .</span><span class="sxs-lookup"><span data-stu-id="c55b2-117">The first mapped class is prefixed with ADS\_.</span></span> <span data-ttu-id="c55b2-118">Essas são classes abstratas, mapeadas de acordo com as regras abaixo.</span><span class="sxs-lookup"><span data-stu-id="c55b2-118">These are abstract classes, mapped according to the rules below.</span></span>
    -   <span data-ttu-id="c55b2-119">A segunda classe mapeada é uma classe não abstrata com o \_ prefixo de nome DS.</span><span class="sxs-lookup"><span data-stu-id="c55b2-119">The second mapped class is a nonabstract class with the DS\_ name prefix.</span></span> <span data-ttu-id="c55b2-120">Essa classe é derivada da \_ classe abstrata ADS, com a adição do qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="c55b2-120">This class is derived from the ADS\_ abstract class, with the addition of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

    <span data-ttu-id="c55b2-121">Por exemplo, a classe de **usuário** do esquema de Active Directory é mapeada para duas classes.</span><span class="sxs-lookup"><span data-stu-id="c55b2-121">For example, the **user** class from the Active Directory schema maps to two classes.</span></span> <span data-ttu-id="c55b2-122">A primeira classe é a classe abstrata do **\_ usuário ADS** , mapeada de acordo com as regras abaixo.</span><span class="sxs-lookup"><span data-stu-id="c55b2-122">The first class is the **ADS\_user** abstract class, mapped according to rules below.</span></span> <span data-ttu-id="c55b2-123">A segunda classe é a classe não abstrata do **\_ usuário do DS** .</span><span class="sxs-lookup"><span data-stu-id="c55b2-123">The second class is the **DS\_user** nonabstract class.</span></span> <span data-ttu-id="c55b2-124">Ele é derivado do **\_ usuário do ADS** e tem o qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) adicionado.</span><span class="sxs-lookup"><span data-stu-id="c55b2-124">It is derived from **ADS\_user** and has the added [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

-   <span data-ttu-id="c55b2-125">A menos que especificado de outra forma, o nome de uma classe mapeada é o valor desconfigurado da propriedade **LDAP-Display-Name** na classe Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c55b2-125">Unless specified otherwise, the name of a mapped class is the mangled value of the **LDAP-Display-Name** property in the Active Directory class.</span></span>
-   <span data-ttu-id="c55b2-126">Se a propriedade **subclasse-of** estiver presente na classe Active Directory, a classe MAPEADA por WMI será derivada da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="c55b2-126">If the **Sub-Class-Of** property is present on the Active Directory class, the WMI-mapped class is derived from the specified class.</span></span>

    <span data-ttu-id="c55b2-127">Se a propriedade **subclasse-of** não estiver presente, a classe MAPEADA por WMI será derivada da classe de **\_ \_ \_ classe raiz LDAP do DS** , conforme especificado no arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="c55b2-127">If the **Sub-Class-Of** property is not present, the WMI-mapped class is derived from the **DS\_LDAP\_Root\_Class** class, as specified in the MOF file.</span></span>

    > [!Note]  
    > <span data-ttu-id="c55b2-128">Essa classe tem a propriedade de chave **ADSIPath** , com um tipo **VT \_ BSTR**.</span><span class="sxs-lookup"><span data-stu-id="c55b2-128">This class has the **ADSIPath** key property, with a type **VT\_BSTR**.</span></span> <span data-ttu-id="c55b2-129">Este é o caminho ADSI exclusivo que identifica essa instância.</span><span class="sxs-lookup"><span data-stu-id="c55b2-129">This is the unique ADSI path that identifies this instance.</span></span> <span data-ttu-id="c55b2-130">O Active Directory dá suporte apenas à herança única e, portanto, isso funciona.</span><span class="sxs-lookup"><span data-stu-id="c55b2-130">Active Directory supports single-inheritance only, so this works.</span></span>

     

-   <span data-ttu-id="c55b2-131">Um qualificador **dinâmico** do tipo **VT \_ bool** e o tipo `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` definido como **true** são criados para cada classe.</span><span class="sxs-lookup"><span data-stu-id="c55b2-131">A **Dynamic** qualifier of type **VT\_BOOL**, and flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to **TRUE** is created for every class.</span></span> <span data-ttu-id="c55b2-132">Esse é um qualificador WMI padrão que indica que as instâncias dessa classe são fornecidas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="c55b2-132">This is a standard WMI qualifier that indicates that instances of this class are provided dynamically.</span></span>
-   <span data-ttu-id="c55b2-133">Se a classe não for abstrata, o provedor criará um qualificador de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) do tipo **VT \_ BSTR bool** e o tipo de qualificador `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` definido como "provedor de instância DS" para cada classe.</span><span class="sxs-lookup"><span data-stu-id="c55b2-133">If the class is not abstract, the provider creates a [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier of type **VT\_BSTR BOOL** and qualifier flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to "DS Instance Provider" for every class.</span></span> <span data-ttu-id="c55b2-134">Este é um qualificador WMI padrão que indica o nome do provedor que fornece dinamicamente instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="c55b2-134">This is a standard WMI qualifier that indicates the name of the provider dynamically providing instances of this class.</span></span>

<span data-ttu-id="c55b2-135">O restante das propriedades ADSI é mapeado para qualificadores de classe e propriedades de acordo com as tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c55b2-135">The rest of the ADSI properties map to class qualifiers and properties as per the following tables.</span></span> <span data-ttu-id="c55b2-136">Todos os qualificadores são mapeados com um valor de sinalizador de qualificador de `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .</span><span class="sxs-lookup"><span data-stu-id="c55b2-136">All qualifiers map with a qualifier flag value of `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS`.</span></span>

<span data-ttu-id="c55b2-137">O a seguir lista informações de mapeamento para a classe Active Directory, mostrando o qualificador WMI e o tipo de qualificador WMI para cada propriedade Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c55b2-137">The following lists mapping information for the Active Directory class, showing the WMI qualifier and WMI qualifier type for each Active Directory property.</span></span>

<dl> <dt>

<span data-ttu-id="c55b2-138">**Nome comum**</span><span class="sxs-lookup"><span data-stu-id="c55b2-138">**Common-Name**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-139">**CN** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="c55b2-139">**CN** (**VT\_BSTR**)</span></span>

<span data-ttu-id="c55b2-140">Mapeado diretamente do valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c55b2-140">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="c55b2-141">**Categoria de objeto-padrão**</span><span class="sxs-lookup"><span data-stu-id="c55b2-141">**Default-Object-Category**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-142">**DefaultObjectCategory** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="c55b2-142">**DefaultObjectCategory** (**VT\_BSTR**)</span></span>

<span data-ttu-id="c55b2-143">Mapeado diretamente do valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c55b2-143">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="c55b2-144">**Padrão-descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="c55b2-144">**Default-Security-Descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-145">**DefaultSecurityDescriptor** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="c55b2-145">**DefaultSecurityDescriptor** (**VT\_BSTR**)</span></span>

<span data-ttu-id="c55b2-146">Mapeado diretamente do valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c55b2-146">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="c55b2-147">**Regis-ID**</span><span class="sxs-lookup"><span data-stu-id="c55b2-147">**Governs-Id**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-148">**GovernsId** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="c55b2-148">**GovernsId** (**VT\_BSTR**)</span></span>

<span data-ttu-id="c55b2-149">Mapeado da representação de cadeia de caracteres da OID; por exemplo, "{1 3 3 6}".</span><span class="sxs-lookup"><span data-stu-id="c55b2-149">Mapped from the string representation of the OID; for example, "{ 1 3 3 6 }".</span></span>

</dd> <dt>

<span data-ttu-id="c55b2-150">**Classe de objeto**</span><span class="sxs-lookup"><span data-stu-id="c55b2-150">**Object-Class**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-151">N/D</span><span class="sxs-lookup"><span data-stu-id="c55b2-151">N/A</span></span>

<span data-ttu-id="c55b2-152">Não mapeado.</span><span class="sxs-lookup"><span data-stu-id="c55b2-152">Not mapped.</span></span>

</dd> <dt>

<span data-ttu-id="c55b2-153">**Categoria de classe de objeto**</span><span class="sxs-lookup"><span data-stu-id="c55b2-153">**Object-Class-Category**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-154">**ObjectClassCategory** (**VT \_ i4**)</span><span class="sxs-lookup"><span data-stu-id="c55b2-154">**ObjectClassCategory** (**VT\_I4**)</span></span>

<span data-ttu-id="c55b2-155">Mapeado diretamente do valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="c55b2-155">Mapped directly from the integer value.</span></span> <span data-ttu-id="c55b2-156">Além disso, se o valor for Abstract (2), o qualificador **CIM \_ bool Standard VT** , chamado de qualificador **"Abstract"** , também será criado.</span><span class="sxs-lookup"><span data-stu-id="c55b2-156">In addition, if the value is Abstract(2), then the standard **VT\_BOOL** CIM qualifier, called the **"Abstract"** qualifier, is also created.</span></span>

</dd> <dt>

<span data-ttu-id="c55b2-157">**RDN-ATT-ID**</span><span class="sxs-lookup"><span data-stu-id="c55b2-157">**RDN-ATT-ID**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-158">**RDNATTID** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="c55b2-158">**RDNATTID** (**VT\_BSTR**)</span></span>

<span data-ttu-id="c55b2-159">Mapeado da representação de cadeia de caracteres do valor de OID; por exemplo, "{1 3 3 6}".</span><span class="sxs-lookup"><span data-stu-id="c55b2-159">Mapped from the string representation of the OID value; for example, "{ 1 3 3 6 }".</span></span> <span data-ttu-id="c55b2-160">Além disso, a propriedade identificada aqui é anotada com o qualificador de CIM **indexado** padrão definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="c55b2-160">In addition, the property identified here is annotated with the standard **Indexed** CIM qualifier set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="c55b2-161">**Somente sistema**</span><span class="sxs-lookup"><span data-stu-id="c55b2-161">**System-Only**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-162">**SystemOnly** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="c55b2-162">**SystemOnly** (**VT\_BOOL**)</span></span>

<span data-ttu-id="c55b2-163">Mapeado diretamente do valor booliano.</span><span class="sxs-lookup"><span data-stu-id="c55b2-163">Mapped directly from the Boolean value.</span></span>

</dd> </dl>

 

<span data-ttu-id="c55b2-164">O seguinte lista as propriedades de classe de Active Directory mapeadas para propriedades de classe WMI.</span><span class="sxs-lookup"><span data-stu-id="c55b2-164">The following lists the Active Directory class properties mapped to WMI class properties.</span></span>

<dl> <dt>

<span data-ttu-id="c55b2-165">**Pode-conter**</span><span class="sxs-lookup"><span data-stu-id="c55b2-165">**May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-166">Cada propriedade nessa lista é mapeada para uma propriedade WMI.</span><span class="sxs-lookup"><span data-stu-id="c55b2-166">Each property in this list is mapped to a WMI property.</span></span>

</dd> <dt>

<span data-ttu-id="c55b2-167">**Deve conter**</span><span class="sxs-lookup"><span data-stu-id="c55b2-167">**Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-168">Cada propriedade nessa lista é mapeada para uma propriedade WMI.</span><span class="sxs-lookup"><span data-stu-id="c55b2-168">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="c55b2-169">O qualificador CIM padrão **não \_ nulo** é criado para cada um deles.</span><span class="sxs-lookup"><span data-stu-id="c55b2-169">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span>

</dd> <dt>

<span data-ttu-id="c55b2-170">**Sistema-pode-conter**</span><span class="sxs-lookup"><span data-stu-id="c55b2-170">**System-May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-171">Cada propriedade nessa lista é mapeada para uma propriedade WMI.</span><span class="sxs-lookup"><span data-stu-id="c55b2-171">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="c55b2-172">Além disso, cada propriedade é anotada com um qualificador de **sistema** , definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="c55b2-172">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="c55b2-173">**Sistema-deve conter**</span><span class="sxs-lookup"><span data-stu-id="c55b2-173">**System-Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="c55b2-174">Cada propriedade nessa lista é mapeada para uma propriedade WMI.</span><span class="sxs-lookup"><span data-stu-id="c55b2-174">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="c55b2-175">O qualificador CIM padrão **não \_ nulo** é criado para cada um deles.</span><span class="sxs-lookup"><span data-stu-id="c55b2-175">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span> <span data-ttu-id="c55b2-176">Além disso, cada propriedade é anotada com um qualificador de **sistema** , definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="c55b2-176">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> </dl>

## <a name="mapping-attributes"></a><span data-ttu-id="c55b2-177">Atributos de mapeamento</span><span class="sxs-lookup"><span data-stu-id="c55b2-177">Mapping Attributes</span></span>

<span data-ttu-id="c55b2-178">O provedor de serviços de diretório mapeia cada atributo de uma classe Active Directory para exatamente uma propriedade da classe WMI correspondente de acordo com as regras nesta seção.</span><span class="sxs-lookup"><span data-stu-id="c55b2-178">The Directory Services provider maps each attribute of an Active Directory class to exactly one property of the corresponding WMI class according to the rules in this section.</span></span> <span data-ttu-id="c55b2-179">Em geral, o provedor de serviços de diretório nomeia a propriedade WMI como a versão desconfigurado do valor **LDAP-Display-Name** do atributo Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c55b2-179">In general, the Directory Services Provider names the WMI property as the mangled version of the **LDAP-Display-Name** value of the Active Directory attribute.</span></span>

<span data-ttu-id="c55b2-180">Se a propriedade Active Directory **for de valor único** for **false**, essa propriedade WMI será combinada com o operador OR com a **matriz de \_ sinalizador \_ CIM**.</span><span class="sxs-lookup"><span data-stu-id="c55b2-180">If the Active Directory property **Is-Single-Valued** is **FALSE**, then this WMI property is combined with the OR operator with **CIM\_FLAG\_ARRAY**.</span></span> <span data-ttu-id="c55b2-181">Observe que cada propriedade é marcada com o qualificador **VT \_ BSTR** , **ADSyntax**.</span><span class="sxs-lookup"><span data-stu-id="c55b2-181">Note that each property is tagged with the **VT\_BSTR** qualifier, **ADSyntax**.</span></span> <span data-ttu-id="c55b2-182">Representa a sintaxe de Active Directory subjacente.</span><span class="sxs-lookup"><span data-stu-id="c55b2-182">It represents the underlying Active Directory syntax.</span></span>

<span data-ttu-id="c55b2-183">A tabela a seguir lista o mapeamento da sintaxe de Active Directory para o tipo de dados de Propriedade do WMI.</span><span class="sxs-lookup"><span data-stu-id="c55b2-183">The following table lists the mapping of the Active Directory syntax to the WMI property data type.</span></span>



| <span data-ttu-id="c55b2-184">Elemento Active Directory</span><span class="sxs-lookup"><span data-stu-id="c55b2-184">Active Directory element</span></span>                                      | <span data-ttu-id="c55b2-185">Tipo de dados WMI</span><span class="sxs-lookup"><span data-stu-id="c55b2-185">WMI data type</span></span>                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="c55b2-186">**Ponto de acesso**</span><span class="sxs-lookup"><span data-stu-id="c55b2-186">**Access-Point**</span></span>](/windows/desktop/ADSchema/s-object-access-point)            | <span data-ttu-id="c55b2-187">**\_cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-187">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="c55b2-188">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c55b2-188">**Boolean**</span></span>](/windows/desktop/ADSchema/s-boolean)                             | <span data-ttu-id="c55b2-189">**\_booliano de CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-189">**CIM\_BOOLEAN**</span></span>                                                        |
| <span data-ttu-id="c55b2-190">**Cadeia de caracteres sem diferenciação de maiúsculas**</span><span class="sxs-lookup"><span data-stu-id="c55b2-190">**Case Insensitive String**</span></span>                                   | <span data-ttu-id="c55b2-191">**\_cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-191">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="c55b2-192">**Cadeia de caracteres diferencia maiúsculas de minúscula**</span><span class="sxs-lookup"><span data-stu-id="c55b2-192">**Case Sensitive String**</span></span>](/windows/desktop/ADSchema/s-string-case-sensitive) | <span data-ttu-id="c55b2-193">**\_cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-193">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="c55b2-194">**Nome distinto**</span><span class="sxs-lookup"><span data-stu-id="c55b2-194">**Distinguished Name**</span></span>](/windows/desktop/ADSchema/s-object-ds-dn)             | <span data-ttu-id="c55b2-195">**\_cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-195">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="c55b2-196">**DN binário**</span><span class="sxs-lookup"><span data-stu-id="c55b2-196">**DN-Binary**</span></span>](/windows/desktop/ADSchema/s-object-dn-binary)                  | <span data-ttu-id="c55b2-197">Objeto inserido do DN de classe **\_ com \_ binário** definido abaixo.</span><span class="sxs-lookup"><span data-stu-id="c55b2-197">Embedded object of class **DN\_With\_Binary** defined below.</span></span><br/> |
| [<span data-ttu-id="c55b2-198">**Cadeia de caracteres DN**</span><span class="sxs-lookup"><span data-stu-id="c55b2-198">**DN-String**</span></span>](/windows/desktop/ADSchema/s-object-dn-string)                  | <span data-ttu-id="c55b2-199">Objeto inserido do DN de classe **\_ com a \_ cadeia de caracteres** definida abaixo.</span><span class="sxs-lookup"><span data-stu-id="c55b2-199">Embedded object of class **DN\_With\_String** defined below.</span></span><br/> |
| [<span data-ttu-id="c55b2-200">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="c55b2-200">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="c55b2-201">**\_Sint32 CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-201">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="c55b2-202">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="c55b2-202">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="c55b2-203">**\_cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-203">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="c55b2-204">**Valores**</span><span class="sxs-lookup"><span data-stu-id="c55b2-204">**Integer**</span></span>](/windows/desktop/ADSchema/s-integer)                             | <span data-ttu-id="c55b2-205">**\_Sint32 CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-205">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="c55b2-206">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="c55b2-206">**LargeInteger**</span></span>](/windows/desktop/ADSchema/s-largeinteger)                   | <span data-ttu-id="c55b2-207">**\_cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-207">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="c55b2-208">Descritor de Segurança</span><span class="sxs-lookup"><span data-stu-id="c55b2-208">Security Descriptor</span></span>                                           | <span data-ttu-id="c55b2-209">Objeto inserido da classe **Uint8Array** definido abaixo.</span><span class="sxs-lookup"><span data-stu-id="c55b2-209">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="c55b2-210">Cadeia de caracteres numérica</span><span class="sxs-lookup"><span data-stu-id="c55b2-210">Numeric String</span></span>                                                | <span data-ttu-id="c55b2-211">**\_cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-211">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="c55b2-212">ID de objeto</span><span class="sxs-lookup"><span data-stu-id="c55b2-212">Object ID</span></span>                                                     | <span data-ttu-id="c55b2-213">**\_cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-213">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="c55b2-214">Cadeia de caracteres de octeto</span><span class="sxs-lookup"><span data-stu-id="c55b2-214">Octet String</span></span>                                                  | <span data-ttu-id="c55b2-215">Objeto inserido da classe **Uint8Array** definido abaixo.</span><span class="sxs-lookup"><span data-stu-id="c55b2-215">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="c55b2-216">OU nome</span><span class="sxs-lookup"><span data-stu-id="c55b2-216">OR Name</span></span>                                                       | <span data-ttu-id="c55b2-217">**\_cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-217">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="c55b2-218">Presentation-Address</span><span class="sxs-lookup"><span data-stu-id="c55b2-218">Presentation-Address</span></span>                                          | <span data-ttu-id="c55b2-219">Objeto inserido da classe **Uint8Array** definido abaixo.</span><span class="sxs-lookup"><span data-stu-id="c55b2-219">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="c55b2-220">Imprimir cadeia de caracteres de caso</span><span class="sxs-lookup"><span data-stu-id="c55b2-220">Print Case String</span></span>                                             | <span data-ttu-id="c55b2-221">**\_cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-221">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="c55b2-222">Link de réplica</span><span class="sxs-lookup"><span data-stu-id="c55b2-222">Replica Link</span></span>                                                  | <span data-ttu-id="c55b2-223">Objeto inserido da classe **Uint8Array** definido abaixo.</span><span class="sxs-lookup"><span data-stu-id="c55b2-223">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| [<span data-ttu-id="c55b2-224">**Cadeia de caracteres (SID)**</span><span class="sxs-lookup"><span data-stu-id="c55b2-224">**String(Sid)**</span></span>](/windows/desktop/ADSchema/s-string-sid)                      | <span data-ttu-id="c55b2-225">Objeto inserido da classe **Uint8Array** definido abaixo.</span><span class="sxs-lookup"><span data-stu-id="c55b2-225">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="c55b2-226">Hora</span><span class="sxs-lookup"><span data-stu-id="c55b2-226">Time</span></span>                                                          | <span data-ttu-id="c55b2-227">**\_data e hora CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-227">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="c55b2-228">Hora codificada UTC</span><span class="sxs-lookup"><span data-stu-id="c55b2-228">UTC Coded Time</span></span>                                                | <span data-ttu-id="c55b2-229">**\_data e hora CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-229">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="c55b2-230">Cadeia de caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="c55b2-230">Unicode String</span></span>                                                | <span data-ttu-id="c55b2-231">**\_cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="c55b2-231">**CIM\_STRING**</span></span>                                                         |



 

<span data-ttu-id="c55b2-232">A sintaxe de cadeia de caracteres de octeto, que se refere a uma matriz de valores **uint8** , apresenta um problema quando mapeada para o WMI, pois o WMI permite Propriedades de tipos **uint8** e matrizes de **uint8**, enquanto Active Directory permite Propriedades do tipo cadeia de caracteres de octeto, bem como matrizes de cadeia de caracteres de octeto.</span><span class="sxs-lookup"><span data-stu-id="c55b2-232">The Octet String syntax, which refers to an array of **uint8** values, presents a problem when mapped to WMI because WMI allows properties of types **uint8** and arrays of **uint8**, whereas Active Directory allows properties of type Octet String as well as arrays of Octet String.</span></span>

<span data-ttu-id="c55b2-233">O exemplo a seguir mostra a classe de provedor de serviços de diretório que é usada para mapear uma matriz de propriedades de tipo de cadeia de caracteres de octeto.</span><span class="sxs-lookup"><span data-stu-id="c55b2-233">The following example shows the Directory Services Provider class that is used to map an array of Octet String type properties.</span></span>

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

<span data-ttu-id="c55b2-234">O WMI mapeia todas as cadeias de caracteres de octeto Active Directory valores de propriedade para instâncias inseridas de **Uint8Array**.</span><span class="sxs-lookup"><span data-stu-id="c55b2-234">WMI maps all Octet String Active Directory property values to embedded instances of **Uint8Array**.</span></span> <span data-ttu-id="c55b2-235">Da mesma forma, o WMI mapeia matrizes de cadeia de caracteres de octeto para matrizes de objetos **Uint8Array** inseridos.</span><span class="sxs-lookup"><span data-stu-id="c55b2-235">Similarly, WMI maps arrays of Octet String to arrays of embedded **Uint8Array** objects.</span></span>

<span data-ttu-id="c55b2-236">O exemplo a seguir mostra as classes que são mapeadas pelo WMI para DN-Binary e DN-String valores de propriedade DS.</span><span class="sxs-lookup"><span data-stu-id="c55b2-236">The following example shows the classes that are mapped by WMI to DN-Binary and DN-String DS property values.</span></span>

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

<span data-ttu-id="c55b2-237">A tabela a seguir lista como o WMI mapeia o restante das propriedades de interface de atributo Active Directory para qualificadores de propriedade WMI.</span><span class="sxs-lookup"><span data-stu-id="c55b2-237">The following table lists how WMI maps the rest of the Active Directory attribute interface properties to WMI property qualifiers.</span></span>



| <span data-ttu-id="c55b2-238">Atributo de Active Directory-nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="c55b2-238">Active Directory attribute-property name</span></span> | <span data-ttu-id="c55b2-239">Qualificador WMI</span><span class="sxs-lookup"><span data-stu-id="c55b2-239">WMI Qualifier</span></span>       | <span data-ttu-id="c55b2-240">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c55b2-240">Data type</span></span>    | <span data-ttu-id="c55b2-241">Informações de mapeamento</span><span class="sxs-lookup"><span data-stu-id="c55b2-241">Mapping information</span></span>                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| <span data-ttu-id="c55b2-242">**Sintaxe de atributo**</span><span class="sxs-lookup"><span data-stu-id="c55b2-242">**Attribute-Syntax**</span></span>                     | <span data-ttu-id="c55b2-243">**AttributeSyntax**</span><span class="sxs-lookup"><span data-stu-id="c55b2-243">**AttributeSyntax**</span></span> | <span data-ttu-id="c55b2-244">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="c55b2-244">**VT\_BSTR**</span></span> | <span data-ttu-id="c55b2-245">Mapeado a partir da representação de cadeia de caracteres do OID.</span><span class="sxs-lookup"><span data-stu-id="c55b2-245">Mapped from the string representation of the OID.</span></span> |
| <span data-ttu-id="c55b2-246">**Nome comum**</span><span class="sxs-lookup"><span data-stu-id="c55b2-246">**Common-Name**</span></span>                          | <span data-ttu-id="c55b2-247">**Hong**</span><span class="sxs-lookup"><span data-stu-id="c55b2-247">**CN**</span></span>              | <span data-ttu-id="c55b2-248">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="c55b2-248">**VT\_BSTR**</span></span> | <span data-ttu-id="c55b2-249">Mapeado a partir do valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c55b2-249">Mapped from the string value.</span></span>                     |
| <span data-ttu-id="c55b2-250">**Somente sistema**</span><span class="sxs-lookup"><span data-stu-id="c55b2-250">**System-Only**</span></span>                          | <span data-ttu-id="c55b2-251">**System**</span><span class="sxs-lookup"><span data-stu-id="c55b2-251">**System**</span></span>          | <span data-ttu-id="c55b2-252">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="c55b2-252">**VT\_BOOL**</span></span> | <span data-ttu-id="c55b2-253">Mapeado a partir do valor booliano.</span><span class="sxs-lookup"><span data-stu-id="c55b2-253">Mapped from the Boolean value.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="c55b2-254">O WMI mapeia todos os qualificadores Active Directory com os `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` tipos de qualificador.</span><span class="sxs-lookup"><span data-stu-id="c55b2-254">WMI maps all Active Directory qualifiers with the `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` qualifier flavors.</span></span>

 

## <a name="association-classes"></a><span data-ttu-id="c55b2-255">Classes de associação</span><span class="sxs-lookup"><span data-stu-id="c55b2-255">Association Classes</span></span>

<span data-ttu-id="c55b2-256">O serviço de diretório é essencialmente um repositório hierárquico de objetos.</span><span class="sxs-lookup"><span data-stu-id="c55b2-256">The Directory Service is essentially a hierarchical store of objects.</span></span> <span data-ttu-id="c55b2-257">Os objetos que podem aparecer em um nível não folha na hierarquia são chamados de "contêineres".</span><span class="sxs-lookup"><span data-stu-id="c55b2-257">Those objects that can appear at a nonleaf level in the hierarchy are called "containers".</span></span> <span data-ttu-id="c55b2-258">A estrutura dessa hierarquia é mais controlada pelas propriedades "poss-superiores" e "System-poss-superior" de uma classe no esquema.</span><span class="sxs-lookup"><span data-stu-id="c55b2-258">The structure of this hierarchy is further controlled by the "Poss-Superiors" and "System-Poss-Superiors" properties of a class in the schema.</span></span> <span data-ttu-id="c55b2-259">Eles, juntos, especificam o conjunto de classes cujas instâncias podem estar contidas em uma instância de uma classe de contêiner.</span><span class="sxs-lookup"><span data-stu-id="c55b2-259">These, taken together, specify the set of classes whose instances can be contained within an instance of a container class.</span></span>

<span data-ttu-id="c55b2-260">O exemplo a seguir modela uma associação CIM como instâncias da classe de associação estática, [**\_ \_ \_ contenção de classe LDAP do DS**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).</span><span class="sxs-lookup"><span data-stu-id="c55b2-260">The following example models a CIM association as instances of the static association class [**DS\_LDAP\_Class\_Containment**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).</span></span>

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

<span data-ttu-id="c55b2-261">O provedor de classe de associação dá suporte aos métodos [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) e [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) .</span><span class="sxs-lookup"><span data-stu-id="c55b2-261">The association class provider supports the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods.</span></span>

 

