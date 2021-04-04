---
title: Cadeia de vinculação
description: Devido ao número de objetos acessíveis a partir de um serviço de diretório, podem ocorrer colisões de nomenclatura.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- Cadeia de vinculação ADSI
- ADSI do ADsPath, descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917669"
---
# <a name="binding-string"></a><span data-ttu-id="735e3-105">Cadeia de vinculação</span><span class="sxs-lookup"><span data-stu-id="735e3-105">Binding String</span></span>

<span data-ttu-id="735e3-106">Devido ao número de objetos acessíveis a partir de um serviço de diretório, podem ocorrer colisões de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="735e3-106">Due to the number of objects accessible from a directory service, naming collisions can occur.</span></span> <span data-ttu-id="735e3-107">A cadeia de caracteres de associação, que é comumente conhecida como ADsPath, permite que você especifique um objeto específico sem causar uma colisão de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="735e3-107">The binding string, which is commonly referred to as the ADsPath, enables you to specify a particular object without causing a naming collision.</span></span> <span data-ttu-id="735e3-108">Isso pode ser aplicado a um único provedor de serviços de diretório ou a vários provedores de serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="735e3-108">This can be applied for a single directory service provider or across multiple directory service providers.</span></span>

<span data-ttu-id="735e3-109">Um ADsPath é uma cadeia de caracteres que identifica exclusivamente um objeto ADSI em um serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="735e3-109">An ADsPath is a string that uniquely identifies an ADSI object on a directory service.</span></span> <span data-ttu-id="735e3-110">Como os objetos ADSI existem dentro do contexto do namespace do serviço de diretório subjacente, parte da sintaxe de um nome ADsPath é específica do provedor.</span><span class="sxs-lookup"><span data-stu-id="735e3-110">Because ADSI objects exist within the context of the namespace of the underlying directory service, part of the syntax of an ADsPath name is provider-specific.</span></span>

<span data-ttu-id="735e3-111">A tabela a seguir lista os provedores ADSI fornecidos por padrão.</span><span class="sxs-lookup"><span data-stu-id="735e3-111">The following table lists the ADSI providers provided by default.</span></span>



| <span data-ttu-id="735e3-112">Provedor</span><span class="sxs-lookup"><span data-stu-id="735e3-112">Provider</span></span>         | <span data-ttu-id="735e3-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="735e3-113">Description</span></span>                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="735e3-114">WinNT</span><span class="sxs-lookup"><span data-stu-id="735e3-114">WinNT</span></span><br/> | <span data-ttu-id="735e3-115">Usado para se comunicar com os controladores de domínio do Windows.</span><span class="sxs-lookup"><span data-stu-id="735e3-115">Used to communicate with Windows domain controllers.</span></span> <span data-ttu-id="735e3-116">Para obter mais informações sobre o ADsPath WinNT, consulte o [ADsPath do Winnt](winnt-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="735e3-116">For more information about the WinNT ADsPath, see [WinNT ADsPath](winnt-adspath.md).</span></span><br/>           |
| <span data-ttu-id="735e3-117">LDAP</span><span class="sxs-lookup"><span data-stu-id="735e3-117">LDAP</span></span><br/>  | <span data-ttu-id="735e3-118">Usado para se comunicar com servidores LDAP, como Active Directory.</span><span class="sxs-lookup"><span data-stu-id="735e3-118">Used to communicate with LDAP servers, such as Active Directory.</span></span> <span data-ttu-id="735e3-119">Para obter mais informações sobre o ADsPath LDAP, consulte o [ADsPath LDAP](ldap-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="735e3-119">For more information about the LDAP ADsPath, see [LDAP ADsPath](ldap-adspath.md).</span></span><br/>  |
| <span data-ttu-id="735e3-120">Banner</span><span class="sxs-lookup"><span data-stu-id="735e3-120">ADs</span></span><br/>   | <span data-ttu-id="735e3-121">Fornece uma implementação de [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) que pode ser usada para enumerar todos os provedores ADSI instalados no cliente.</span><span class="sxs-lookup"><span data-stu-id="735e3-121">Provides an [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) implementation that can be used to enumerate all of the ADSI providers installed on the client.</span></span><br/> |



 

<span data-ttu-id="735e3-122">Use esses nomes de provedor para acessar o namespace do provedor padrão.</span><span class="sxs-lookup"><span data-stu-id="735e3-122">Use these provider names to access the default provider namespace.</span></span> <span data-ttu-id="735e3-123">Por exemplo, se você associar ao LDAP, a ADSI ligará a um contêiner que contém o objeto de domínio conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="735e3-123">For example, if you bind to LDAP, ADSI binds to a container that contains the domain object currently logged on.</span></span> <span data-ttu-id="735e3-124">Se você associar ao WinNT, a ADSI será vinculada a um contêiner que contém objetos que se correlacionam a todos os domínios na rede.</span><span class="sxs-lookup"><span data-stu-id="735e3-124">If you bind to WinNT, ADSI binds to a container that holds objects that correlate to all domains on the network.</span></span>

<span data-ttu-id="735e3-125">Os elementos iniciais da cadeia de caracteres ADsPath são o identificador programático (progID) do provedor ADSI, seguido por "://", seguido pela sintaxe ditada pelo namespace do provedor.</span><span class="sxs-lookup"><span data-stu-id="735e3-125">The initial elements of the ADsPath string are the programmatic identifier (progID) of the ADSI provider, followed by "://", followed by syntax dictated by the provider namespace.</span></span> <span data-ttu-id="735e3-126">A cadeia de caracteres progID pode ou não diferenciar maiúsculas de minúsculas, dependendo do provedor.</span><span class="sxs-lookup"><span data-stu-id="735e3-126">The progID string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="735e3-127">As cadeias de caracteres progID para os provedores listados acima diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="735e3-127">The progID strings for the providers listed above are case-sensitive.</span></span>

<span data-ttu-id="735e3-128">A cadeia de caracteres de caminho pode ou não diferenciar maiúsculas de minúsculas, dependendo do provedor.</span><span class="sxs-lookup"><span data-stu-id="735e3-128">The path string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="735e3-129">As cadeias de caracteres de caminho para os provedores listados acima não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="735e3-129">The path strings for the providers listed above are not case-sensitive.</span></span>

<span data-ttu-id="735e3-130">Veja a seguir exemplos de ADsPaths.</span><span class="sxs-lookup"><span data-stu-id="735e3-130">The following are examples of ADsPaths.</span></span>

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

<span data-ttu-id="735e3-131">Para localizar todos os provedores instalados em seu computador, associe-se ao provedor ADs, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="735e3-131">To find all providers installed on your computer, bind to the ADs provider as shown in the following code example.</span></span>


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



<span data-ttu-id="735e3-132">Usando o provedor LDAP, você pode especificar o ADsPath em um formulário DN (nome diferenciado) X. 500, começando com a marca CN ou pode especificar seu inverso hierárquico, começando com a marca o.</span><span class="sxs-lookup"><span data-stu-id="735e3-132">Using the LDAP provider, you can specify the ADsPath either in an X.500 distinguished name (DN) form, starting with the CN tag, or you can specify its hierarchical inverse, starting with the O tag.</span></span> <span data-ttu-id="735e3-133">O formulário que você usa no ADsPath inicial determina a ordem das marcas.</span><span class="sxs-lookup"><span data-stu-id="735e3-133">The form you use in the initial ADsPath determines the order of the tags.</span></span>

<span data-ttu-id="735e3-134">A tabela a seguir lista os caracteres especiais ADsPath.</span><span class="sxs-lookup"><span data-stu-id="735e3-134">The following table lists ADsPath special characters.</span></span>



| <span data-ttu-id="735e3-135">Nome</span><span class="sxs-lookup"><span data-stu-id="735e3-135">Name</span></span>                      | <span data-ttu-id="735e3-136">Caractere</span><span class="sxs-lookup"><span data-stu-id="735e3-136">Character</span></span>           | <span data-ttu-id="735e3-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="735e3-137">Description</span></span>                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="735e3-138">Aspas duplas</span><span class="sxs-lookup"><span data-stu-id="735e3-138">Double quote</span></span><br/>   | <span data-ttu-id="735e3-139">"</span><span class="sxs-lookup"><span data-stu-id="735e3-139">"</span></span><br/>        | <span data-ttu-id="735e3-140">Usado para citar qualquer parte do ADsPath que possa conter um caractere especial para que a cadeia de caracteres seja interpretada literalmente.</span><span class="sxs-lookup"><span data-stu-id="735e3-140">Used to quote any part of the ADsPath that may contain a special character so that the string is interpreted literally.</span></span> <span data-ttu-id="735e3-141">Por exemplo, "CN = Nome/prefixo".</span><span class="sxs-lookup"><span data-stu-id="735e3-141">For example, "CN=Name/Prefix".</span></span><br/>                                     |
| <span data-ttu-id="735e3-142">Barra invertida</span><span class="sxs-lookup"><span data-stu-id="735e3-142">Backslash</span></span><br/>      | \\<br/>       | <span data-ttu-id="735e3-143">Usado para preceder caracteres especiais para significar que eles devem ser usados como literais.</span><span class="sxs-lookup"><span data-stu-id="735e3-143">Used to precede special characters to signify they should be used as literals.</span></span> <span data-ttu-id="735e3-144">Para obter mais informações e uma lista de caracteres especiais, consulte [nomes distintos](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="735e3-144">For more information and a list of special characters, see [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span><br/> |
| <span data-ttu-id="735e3-145">Caractere</span><span class="sxs-lookup"><span data-stu-id="735e3-145">Slash</span></span><br/>          | /<br/>        | <span data-ttu-id="735e3-146">Separador de componentes.</span><span class="sxs-lookup"><span data-stu-id="735e3-146">Component separator.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="735e3-147">Colchetes angulares</span><span class="sxs-lookup"><span data-stu-id="735e3-147">Angle brackets</span></span><br/> | <><br/> | <span data-ttu-id="735e3-148">Delimite um ADsPath dentro de outra convenção de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="735e3-148">Delimit an ADsPath within another naming convention.</span></span><br/>                                                                                                                                       |



 

<span data-ttu-id="735e3-149">Para delimitar um ADsPath em uma especificação de pesquisa ou como parte de uma URL, use o colchete angular esquerdo e direito (< >).</span><span class="sxs-lookup"><span data-stu-id="735e3-149">To delimit an ADsPath in a search specification or as part of a URL, use the left and right angle bracket (< >).</span></span> <span data-ttu-id="735e3-150">Por exemplo, " &lt; winnt://mydomain/UserAccount &gt; ".</span><span class="sxs-lookup"><span data-stu-id="735e3-150">For example, "&lt;WinNT://MyDomain/UserAccount&gt;".</span></span>

<span data-ttu-id="735e3-151">Alguns provedores ADSI podem ter as restrições de sintaxe adicionadas devido a requisitos de namespace.</span><span class="sxs-lookup"><span data-stu-id="735e3-151">Some ADSI providers may have added syntax restrictions due to namespace requirements.</span></span>

## <a name="active-directory-binding-options"></a><span data-ttu-id="735e3-152">Opções de associação de Active Directory</span><span class="sxs-lookup"><span data-stu-id="735e3-152">Active Directory Binding Options</span></span>

<span data-ttu-id="735e3-153">Active Directory fornece a capacidade de associar a um objeto usando vários outros tipos de cadeias de caracteres de associação, como um GUID (identificador global exclusivo) de COM ou um SID (identificador de segurança).</span><span class="sxs-lookup"><span data-stu-id="735e3-153">Active Directory provides the ability to bind to an object using several other types of binding strings, such as a COM globally unique identifier (GUID) or a security identifier (SID).</span></span> <span data-ttu-id="735e3-154">Para obter mais informações, consulte [Binding to Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="735e3-154">For more information, see [Binding to Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span></span>

 

