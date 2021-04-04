---
title: Prefixos de URI
description: O prefixo do URI de recurso é diferente dependendo de qual esquema XML descreve o recurso.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e73de4d6d1762e87aa05e72b6cb6b3fbb228b80d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103824051"
---
# <a name="uri-prefixes"></a><span data-ttu-id="944a8-103">Prefixos de URI</span><span class="sxs-lookup"><span data-stu-id="944a8-103">URI prefixes</span></span>

<span data-ttu-id="944a8-104">O prefixo do [*URI de recurso*](windows-remote-management-glossary.md) é diferente dependendo de qual esquema XML descreve o recurso.</span><span class="sxs-lookup"><span data-stu-id="944a8-104">The [*resource URI*](windows-remote-management-glossary.md) prefix is different depending on which XML schema describes the resource.</span></span>

## <a name="prefixes"></a><span data-ttu-id="944a8-105">Prefixos</span><span class="sxs-lookup"><span data-stu-id="944a8-105">Prefixes</span></span>

<span data-ttu-id="944a8-106">Se você acessar uma classe [*cim*](windows-remote-management-glossary.md) 2,1, como o [**\_ DataFile do CIM**](/windows/desktop/CIMWin32Prov/cim-datafile), o prefixo do URI será diferente do prefixo de uma classe CIM 2,9, como o **CIM \_ AdminDomain**.</span><span class="sxs-lookup"><span data-stu-id="944a8-106">If you access a [*CIM*](windows-remote-management-glossary.md) 2.1 class, such as [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), the prefix of the URI differs from the prefix for a CIM 2.9 class, such as **CIM\_AdminDomain**.</span></span> <span data-ttu-id="944a8-107">As classes CIM 2,1 são documentadas na seção [classes CIM](/windows/desktop/WmiSdk/cimclas) de instrumentação de gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="944a8-107">CIM 2.1 classes are documented in the [CIM Classes](/windows/desktop/WmiSdk/cimclas) section of Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="944a8-108">A maioria das [classes WMI](/windows/desktop/WmiSdk/wmi-classes) está no namespace WMI **\\ cimv2 raiz** .</span><span class="sxs-lookup"><span data-stu-id="944a8-108">Most [WMI classes](/windows/desktop/WmiSdk/wmi-classes) are in the **root\\cimv2** WMI namespace.</span></span> <span data-ttu-id="944a8-109">As classes para o provedor de [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)(interface de gerenciamento de plataforma inteligente) da Microsoft estão em **\\ hardware raiz**.</span><span class="sxs-lookup"><span data-stu-id="944a8-109">Classes for the Microsoft Intelligent Platform Management Interface ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) provider are in **root\\hardware**.</span></span>

<span data-ttu-id="944a8-110">A lista a seguir contém os prefixos de URI de recurso para esses esquemas:</span><span class="sxs-lookup"><span data-stu-id="944a8-110">The following list contains the resource URI prefixes for these schemas:</span></span>

-   <span data-ttu-id="944a8-111">Classes WMI ou CIM 2,1 no namespace **raiz \\ cimv2**</span><span class="sxs-lookup"><span data-stu-id="944a8-111">WMI or CIM 2.1 classes in the **root\\cimv2** namespace</span></span>

    <span data-ttu-id="944a8-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span><span class="sxs-lookup"><span data-stu-id="944a8-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span></span>

-   <span data-ttu-id="944a8-113">Classes CIM 2,9 ou classes IPMI</span><span class="sxs-lookup"><span data-stu-id="944a8-113">CIM 2.9 classes or IPMI classes</span></span>

    <span data-ttu-id="944a8-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span><span class="sxs-lookup"><span data-stu-id="944a8-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span></span>

-   <span data-ttu-id="944a8-115">Maneira alternativa de acessar classes de provedor de IPMI</span><span class="sxs-lookup"><span data-stu-id="944a8-115">Alternate way to access IPMI provider classes</span></span>

    <span data-ttu-id="944a8-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span><span class="sxs-lookup"><span data-stu-id="944a8-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span></span>

<span data-ttu-id="944a8-117">Para obter mais informações, consulte [URIs de recurso](resource-uris.md) e [cadeias de caracteres URLPrefix](/windows/desktop/Http/urlprefix-strings).</span><span class="sxs-lookup"><span data-stu-id="944a8-117">For more information, see [Resource URIs](resource-uris.md) and [UrlPrefix Strings](/windows/desktop/Http/urlprefix-strings).</span></span> <span data-ttu-id="944a8-118">Para obter mais informações sobre como gerar um URI para uma classe ou um método WMI, consulte [gerenciamento remoto do Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="944a8-118">For more information about generating a URI for a WMI class or method, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="prefix-aliases"></a><span data-ttu-id="944a8-119">Aliases de prefixo</span><span class="sxs-lookup"><span data-stu-id="944a8-119">Prefix Aliases</span></span>

<span data-ttu-id="944a8-120">Um alias de prefixo é um atalho que representa o prefixo de URI de recurso longo.</span><span class="sxs-lookup"><span data-stu-id="944a8-120">A prefix alias is a shortcut that represents the long resource URI prefix.</span></span> <span data-ttu-id="944a8-121">Você também pode usar aliases na linha de comando do **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="944a8-121">You can also use aliases in the **Winrm** command-line.</span></span> <span data-ttu-id="944a8-122">Para exibir uma lista de aliases disponíveis, digite **aliases de ajuda do WinRM**.</span><span class="sxs-lookup"><span data-stu-id="944a8-122">To view a list of available aliases, type **Winrm help aliases**.</span></span>

<span data-ttu-id="944a8-123">Lembre-se de que um alias não pode ser usado dentro de uma referência de ponto de extremidade (EPR) ao especificar um URI de recurso.</span><span class="sxs-lookup"><span data-stu-id="944a8-123">Be aware that an alias cannot be used inside an endpoint reference (EPR) when specifying a resource URI.</span></span> <span data-ttu-id="944a8-124">Gerenciamento Remoto do Windows não pode expandir o alias quando ele é inserido em XML.</span><span class="sxs-lookup"><span data-stu-id="944a8-124">Windows Remote Management is unable to expand the alias when it is embedded in XML.</span></span>

<span data-ttu-id="944a8-125">No exemplo de código a seguir, o alias do WinRM é usado em um EPR em vez do URI de recurso completo, que é `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` .</span><span class="sxs-lookup"><span data-stu-id="944a8-125">In the following code example, the winrm alias is used in an EPR instead of the complete resource URI, which is `http://schemas.microsoft.com/wbem/wsman/1/config/Listener`.</span></span> <span data-ttu-id="944a8-126">Nesse caso, o WinRM retorna um erro que indica que o serviço não pode processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="944a8-126">In this case, WinRM returns an error that indicates the service cannot process the request.</span></span>


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



<span data-ttu-id="944a8-127">As listas a seguir definem aliases e URIs de recursos para os quais substituem.</span><span class="sxs-lookup"><span data-stu-id="944a8-127">The following lists defined aliases and resource URIs for which they substitute.</span></span>

<dl> <dt>

<span data-ttu-id="944a8-128"><span id="wmi"></span><span id="WMI"></span>esses</span><span class="sxs-lookup"><span data-stu-id="944a8-128"><span id="wmi"></span><span id="WMI"></span>wmi</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span data-ttu-id="944a8-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span><span class="sxs-lookup"><span data-stu-id="944a8-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span data-ttu-id="944a8-130"><span id="cimv2"></span><span id="CIMV2"></span>cimv2</span><span class="sxs-lookup"><span data-stu-id="944a8-130"><span id="cimv2"></span><span id="CIMV2"></span>cimv2</span></span>
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span data-ttu-id="944a8-131"><span id="winrm"></span><span id="WINRM"></span>WinRM</span><span class="sxs-lookup"><span data-stu-id="944a8-131"><span id="winrm"></span><span id="WINRM"></span>winrm</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="944a8-132"><span id="wsman"></span><span id="WSMAN"></span>WSMan</span><span class="sxs-lookup"><span data-stu-id="944a8-132"><span id="wsman"></span><span id="WSMAN"></span>wsman</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="944a8-133"><span id="shell"></span><span id="SHELL"></span>Shell</span><span class="sxs-lookup"><span data-stu-id="944a8-133"><span id="shell"></span><span id="SHELL"></span>shell</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="944a8-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="944a8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="944a8-135">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="944a8-135">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="944a8-136">Gerenciamento Remoto do Windows e WMI</span><span class="sxs-lookup"><span data-stu-id="944a8-136">Windows Remote Management and WMI</span></span>](windows-remote-management-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="944a8-137">URIs do Recurso</span><span class="sxs-lookup"><span data-stu-id="944a8-137">Resource URIs</span></span>](resource-uris.md)
</dt> </dl>
