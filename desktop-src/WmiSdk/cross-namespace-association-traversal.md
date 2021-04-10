---
description: A partir do Windows 7, Instrumentação de Gerenciamento do Windows (WMI) implementou um mecanismo padrão para descobrir perfis usando o esquema CIM.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Passagem de associação entre namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827844"
---
# <a name="cross-namespace-association-traversal"></a><span data-ttu-id="6a081-103">Passagem de associação entre namespaces</span><span class="sxs-lookup"><span data-stu-id="6a081-103">Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="6a081-104">A partir do Windows 7, Instrumentação de Gerenciamento do Windows (WMI) implementou um mecanismo padrão para descobrir perfis usando o esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="6a081-104">Starting in Windows 7, Windows Management Instrumentation (WMI) implemented a standard mechanism for discovering profiles by using the CIM schema.</span></span>

<span data-ttu-id="6a081-105">O WMI dá suporte à passagem de associação entre namespaces e ao registro de perfil de associação.</span><span class="sxs-lookup"><span data-stu-id="6a081-105">WMI supports the cross-namespace association traversal and association profile registration.</span></span> <span data-ttu-id="6a081-106">Para obter mais informações sobre o registro de perfil e a implementação padrão de CIM de passagem de associação, consulte DSP1033 ( [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf) )</span><span class="sxs-lookup"><span data-stu-id="6a081-106">For more information about profile registration and the CIM standard implementation of association traversal, see DSP1033 ([https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf))</span></span>

<span data-ttu-id="6a081-107">Para dar suporte a esse recurso, a infraestrutura do WMI fez o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6a081-107">To support this feature, the WMI infrastructure did the following:</span></span>

-   <span data-ttu-id="6a081-108">Criou o namespace Interop: \\ root \\ Interop.</span><span class="sxs-lookup"><span data-stu-id="6a081-108">Created the interop namespace: \\root\\interop.</span></span>
-   <span data-ttu-id="6a081-109">Passagem de associação entre namespaces permitidas.</span><span class="sxs-lookup"><span data-stu-id="6a081-109">Allowed cross namespace association traversal.</span></span> <span data-ttu-id="6a081-110">Associações que cruzam namespaces dão suporte à filtragem no nível de classe de associação e no nível de namespace implementado.</span><span class="sxs-lookup"><span data-stu-id="6a081-110">Associations that cross namespaces support filtering at the association class level and at the implemented namespace level.</span></span>
-   <span data-ttu-id="6a081-111">Adicionadas as classes [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)e [**CIM \_ ReferencedProfile**](cim-referencedprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="6a081-111">Added the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile), and [**CIM\_ReferencedProfile**](cim-referencedprofile.md) classes.</span></span>
-   <span data-ttu-id="6a081-112">Implementação da compatibilidade de 2.17.1 da versão do esquema CIM implementada.</span><span class="sxs-lookup"><span data-stu-id="6a081-112">Implemented CIM Schema version 2.17.1 compatibility.</span></span> <span data-ttu-id="6a081-113">Para obter mais informações, consulte [compatibilidade do esquema CIM](cim-schema-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="6a081-113">For more information, see [CIM Schema Compatibility](cim-schema-compatibility.md).</span></span>

## <a name="interop-namespace"></a><span data-ttu-id="6a081-114">Namespace de interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="6a081-114">Interop Namespace</span></span>

<span data-ttu-id="6a081-115">O namespace Interop fornece um local comum para um aplicativo cliente descobrir todos os perfis com suporte em um computador.</span><span class="sxs-lookup"><span data-stu-id="6a081-115">The interop namespace provides a common location for a client application to discover all of the profiles that are supported on a computer.</span></span> <span data-ttu-id="6a081-116">Os perfis podem ser usados para gerenciar vários aspectos de um sistema operacional, matriz de armazenamento ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6a081-116">Profiles can be used to manage various aspects of an operating system, storage array, or database.</span></span>

<span data-ttu-id="6a081-117">Todos os objetos e classes de interoperabilidade devem ser definidos no \\ namespace de interoperabilidade raiz.</span><span class="sxs-lookup"><span data-stu-id="6a081-117">All interop classes and objects must be defined in the root\\interop namespace.</span></span>

## <a name="cim-classes"></a><span data-ttu-id="6a081-118">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="6a081-118">CIM Classes</span></span>

<span data-ttu-id="6a081-119">As classes CIM descritas na lista a seguir dão suporte à passagem de associação entre namespaces.</span><span class="sxs-lookup"><span data-stu-id="6a081-119">The CIM classes described in the following list support cross-namespace association traversal.</span></span>

<dl> <dt>

<span data-ttu-id="6a081-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a081-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="6a081-121">Usado para identificar a especificação de perfil que é anunciada como sendo implementada.</span><span class="sxs-lookup"><span data-stu-id="6a081-121">Used to identify the profile specification that is advertised as being implemented.</span></span> <span data-ttu-id="6a081-122">Essa classe especifica informações que incluem o nome do perfil, a organização e a versão com a qual a implementação é compatível.</span><span class="sxs-lookup"><span data-stu-id="6a081-122">This class specifies information that includes the profile name, organization, and version with which the implementation is compliant.</span></span>

</dd> <dt>

<span data-ttu-id="6a081-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span><span class="sxs-lookup"><span data-stu-id="6a081-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span></span>
</dt> <dd>

<span data-ttu-id="6a081-124">Usado para associar instâncias de elementos de gerenciamento que são definidos em perfis com a classe [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) que identifica as especificações de perfil específicas que são implementadas.</span><span class="sxs-lookup"><span data-stu-id="6a081-124">Used to associate instances of management elements that are defined in profiles with the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) class that identifies the particular profile specifications that are implemented.</span></span>

</dd> <dt>

<span data-ttu-id="6a081-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)</span><span class="sxs-lookup"><span data-stu-id="6a081-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM\_ReferencedProfile**](cim-referencedprofile.md)</span></span>
</dt> <dd>

<span data-ttu-id="6a081-126">Usado para representar a relação entre os perfis.</span><span class="sxs-lookup"><span data-stu-id="6a081-126">Used to represent the relationship between profiles.</span></span>

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a><span data-ttu-id="6a081-127">Implementando a passagem de associação entre namespaces</span><span class="sxs-lookup"><span data-stu-id="6a081-127">Implementing Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="6a081-128">O serviço WMI permite a passagem de associação entre namespaces.</span><span class="sxs-lookup"><span data-stu-id="6a081-128">The WMI service allows cross-namespace association traversal.</span></span> <span data-ttu-id="6a081-129">O WMI fornece o namespace Interop para registrar perfis e associá-los a perfis que são implementados em namespaces diferentes.</span><span class="sxs-lookup"><span data-stu-id="6a081-129">WMI provides the interop namespace for registering profiles and associating them with profiles that are implemented in different namespaces.</span></span> <span data-ttu-id="6a081-130">No entanto, para usar a passagem de associação, os implementadores devem instanciar as classes de perfil na interoperabilidade e no namespace implementado.</span><span class="sxs-lookup"><span data-stu-id="6a081-130">However, to use association traversal, implementers must instantiate the profile classes both in the interop and in the implemented namespace.</span></span> <span data-ttu-id="6a081-131">Para obter mais informações, consulte [escrevendo um provedor de associação para interoperabilidade](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="6a081-131">For more information, see [Writing an Association Provider for Interop](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="6a081-132">Associações que cruzam namespaces dentro do mesmo ambiente de gerenciamento devem ser instanciadas nos namespaces Interop e implemented.</span><span class="sxs-lookup"><span data-stu-id="6a081-132">Associations that cross namespaces within the same management environment must be instantiated in both the interop and implemented namespaces.</span></span> <span data-ttu-id="6a081-133">Caso contrário, a passagem de associação não funcionará.</span><span class="sxs-lookup"><span data-stu-id="6a081-133">Otherwise, association traversal will not work.</span></span> <span data-ttu-id="6a081-134">Por exemplo, o provedor de associação do perfil de energia deve ser registrado com os namespaces de raiz/interoperabilidade e raiz/cimv2/energia.</span><span class="sxs-lookup"><span data-stu-id="6a081-134">For example, the power profile association provider must be registered with both root/interop and root/cimv2/power namespaces.</span></span> <span data-ttu-id="6a081-135">A passagem de associação deve ser capaz de ocorrer de um namespace de volta para o outro.</span><span class="sxs-lookup"><span data-stu-id="6a081-135">Association traversal should be able to occur from either namespace back to the other.</span></span> <span data-ttu-id="6a081-136">Para obter exemplos de passagem de associação, consulte [acessando dados no namespace Interop](accessing-data-in-the-interop-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="6a081-136">For examples of association traversal, see [Accessing Data in the Interop Namespace](accessing-data-in-the-interop-namespace.md).</span></span>

<span data-ttu-id="6a081-137">\* \* Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="6a081-137">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="6a081-138">Após a atualização para o Windows 7, se houver perfis de dispositivo de interoperabilidade instalados anteriormente no namespace de raiz/interoperabilidade, nenhum perfil do Windows 7 será instalado.</span><span class="sxs-lookup"><span data-stu-id="6a081-138">After upgrading to Windows 7, if there are interop device profiles that were previously installed in the root/interop namespace, no Windows 7 profiles will be installed.</span></span> <span data-ttu-id="6a081-139">Esses objetos de perfil de terceiros substituem o esquema de interoperabilidade do Windows 7 para manter a funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="6a081-139">These third-party profile objects overwrite Windows 7 interop schema to maintain functionality.</span></span> <span data-ttu-id="6a081-140">Além disso, a ID de evento 5631 do aplicativo WMI é registrada.</span><span class="sxs-lookup"><span data-stu-id="6a081-140">Additionally, the WMI application event ID 5631 is recorded.</span></span>

<span data-ttu-id="6a081-141">Para obter os perfis de interoperabilidade do Windows 7, a versão do Windows 7 do arquivo Interop. mof e os arquivos MFL relacionados devem ser compilados.</span><span class="sxs-lookup"><span data-stu-id="6a081-141">To get the Windows 7 interop profiles, the Windows 7 version of the Interop.mof file and the related MFL files must be compiled.</span></span> <span data-ttu-id="6a081-142">Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="6a081-142">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a081-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a081-143">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6a081-144">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a081-144">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6a081-145">**\_ELEMENTCONFORMSTOPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="6a081-145">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[<span data-ttu-id="6a081-146">**\_REFERENCEDPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="6a081-146">**CIM\_ReferencedProfile**</span></span>](cim-referencedprofile.md)
</dt> <dt>

[<span data-ttu-id="6a081-147">Compatibilidade do esquema CIM</span><span class="sxs-lookup"><span data-stu-id="6a081-147">CIM Schema Compatibility</span></span>](cim-schema-compatibility.md)
</dt> <dt>

[<span data-ttu-id="6a081-148">Escrevendo um provedor de associação para interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="6a081-148">Writing an Association Provider for Interop</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

[<span data-ttu-id="6a081-149">Acessando dados no namespace Interop</span><span class="sxs-lookup"><span data-stu-id="6a081-149">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
