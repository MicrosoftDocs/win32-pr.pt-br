---
description: O namespace WMI é um objeto de programação que define o escopo de um conjunto de classes e instâncias. As classes do provedor WMI devem ser definidas dentro de um namespace.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Criando hierarquias dentro do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165337"
---
# <a name="creating-hierarchies-within-wmi"></a><span data-ttu-id="acd72-104">Criando hierarquias dentro do WMI</span><span class="sxs-lookup"><span data-stu-id="acd72-104">Creating Hierarchies Within WMI</span></span>

<span data-ttu-id="acd72-105">O [*namespace WMI*](gloss-n.md) é um objeto de programação que define o escopo de um conjunto de classes e instâncias.</span><span class="sxs-lookup"><span data-stu-id="acd72-105">[*WMI namespace*](gloss-n.md) is a programming object that defines the scope for a set of classes and instances.</span></span> <span data-ttu-id="acd72-106">As classes do provedor WMI devem ser definidas dentro de um namespace.</span><span class="sxs-lookup"><span data-stu-id="acd72-106">WMI provider classes must be defined inside a namespace.</span></span>

<span data-ttu-id="acd72-107">Os namespaces descrevem diferentes ambientes gerenciados, como o ambiente SMS.</span><span class="sxs-lookup"><span data-stu-id="acd72-107">Namespaces describe different managed environments, such as the SMS environment.</span></span> <span data-ttu-id="acd72-108">Como as classes e instâncias de um esquema definem os componentes de um ambiente gerenciado, cada novo esquema requer um novo namespace.</span><span class="sxs-lookup"><span data-stu-id="acd72-108">Because the classes and instances of a schema define the components of a managed environment, each new schema requires a new namespace.</span></span> <span data-ttu-id="acd72-109">Por exemplo, o \\ namespace raiz cimv2 contém as classes e instâncias definidas no esquema Win32, bem como as classes de modelo CIM pai (CIM) das quais o esquema Win32 herda.</span><span class="sxs-lookup"><span data-stu-id="acd72-109">For example, the root\\cimv2 namespace contains the classes and instances defined in the Win32 schema as well as the parent Common Information Model (CIM) classes from which the Win32 schema inherits.</span></span> <span data-ttu-id="acd72-110">As classes CIM são definidas pela[DMTF](https://www.dmtf.org/home)(Distributed Management Task Force).</span><span class="sxs-lookup"><span data-stu-id="acd72-110">CIM classes are defined by the Distributed Management Task Force ([DMTF](https://www.dmtf.org/home)).</span></span>

> [!Note]  
> <span data-ttu-id="acd72-111">Para garantir que todas as suas definições de classe WMI para objetos gerenciados sejam restauradas no [*repositório WMI*](gloss-w.md) se o WMI tiver uma falha e for reiniciado, use a instrução de pré-processador de [**\# AutoRecuperação pragma**](pragma-autorecover.md) no seu arquivo [*formato MOF (MOF)*](gloss-m.md) .</span><span class="sxs-lookup"><span data-stu-id="acd72-111">To ensure that all of your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format (MOF)*](gloss-m.md) file.</span></span>

 

<span data-ttu-id="acd72-112">O WMI define um namespace como uma instância da classe de sistema de [**\_ \_ namespace**](--namespace.md) ou qualquer classe derivada do **\_ \_ namespace**.</span><span class="sxs-lookup"><span data-stu-id="acd72-112">WMI defines a namespace as an instance of the [**\_\_Namespace**](--namespace.md) system class or any class that derives from **\_\_Namespace**.</span></span> <span data-ttu-id="acd72-113">A classe de sistema **\_ \_ namespace** tem uma única propriedade chamada **Name**, que deve ser exclusiva dentro do escopo do namespace pai.</span><span class="sxs-lookup"><span data-stu-id="acd72-113">The **\_\_Namespace** system class has a single property called **Name**, which must be unique within the scope of the parent namespace.</span></span> <span data-ttu-id="acd72-114">A propriedade **Name** também deve conter uma cadeia de caracteres que comece com uma letra.</span><span class="sxs-lookup"><span data-stu-id="acd72-114">The **Name** property must also contain a string that begins with a letter.</span></span> <span data-ttu-id="acd72-115">Todos os outros caracteres na cadeia de caracteres podem ser letras, dígitos ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="acd72-115">All other characters in the string can be letters, digits, or underscores.</span></span> <span data-ttu-id="acd72-116">Todos os caracteres não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="acd72-116">All characters are case-insensitive.</span></span>

<span data-ttu-id="acd72-117">Além de determinar o nome exclusivo para um namespace filho, o namespace pai WMI pode proteger as instâncias estáticas de suas classes contra a modificação acidental por outros provedores.</span><span class="sxs-lookup"><span data-stu-id="acd72-117">In addition to determining the unique name for a child namespace, the parent WMI namespace can protect the static instances of your classes from accidental modification by other providers.</span></span> <span data-ttu-id="acd72-118">Por exemplo, você pode achar conveniente aninhar um novo namespace em um namespace existente para outro provedor.</span><span class="sxs-lookup"><span data-stu-id="acd72-118">For example, you may find it convenient to nest a new namespace under an existing namespace for another provider.</span></span> <span data-ttu-id="acd72-119">No entanto, o provedor original pode tentar atualizar todas as instâncias de classe para que correspondam a um novo esquema.</span><span class="sxs-lookup"><span data-stu-id="acd72-119">However, the original provider may try to update all class instances to match up with a new schema.</span></span> <span data-ttu-id="acd72-120">Ao fazer isso, o provedor original pode excluir todos os subfilhos em um namespace.</span><span class="sxs-lookup"><span data-stu-id="acd72-120">In doing so, the original provider may delete all sub-children in a namespace.</span></span> <span data-ttu-id="acd72-121">Embora isso possa ser uma ação apropriada para o namespace de destino, ele pode afetar instâncias de classe não relacionadas em um namespace filho (ou seja, suas próprias classes de provedor).</span><span class="sxs-lookup"><span data-stu-id="acd72-121">While this may be an appropriate action for the target namespace, it may affect unrelated class instances in a child namespace (i.e., your own provider classes).</span></span>

<span data-ttu-id="acd72-122">Portanto, geralmente é recomendável que você crie e Registre seu namespace como separado dos namespaces que você não controla diretamente.</span><span class="sxs-lookup"><span data-stu-id="acd72-122">Therefore, it is generally recommended that you create and register your namespace as separate from namespaces that you do not directly control.</span></span> <span data-ttu-id="acd72-123">Isso é especialmente verdadeiro se suas classes derivarem somente de classes CIM gerais ou de outras classes de sua empresa.</span><span class="sxs-lookup"><span data-stu-id="acd72-123">This is especially true if your classes derive only from general CIM classes or other classes from your company.</span></span> <span data-ttu-id="acd72-124">O namespace pode estar no namespace **raiz** , como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="acd72-124">Your namespace can be under the **Root** namespace, such as the following:</span></span>

<span data-ttu-id="acd72-125">**Raiz/myCompany/MyProduct**</span><span class="sxs-lookup"><span data-stu-id="acd72-125">**Root/myCompany/myProduct**</span></span>

<span data-ttu-id="acd72-126">Por outro lado, se a sua nova classe derivar da classe de outro provedor, talvez seja necessário armazenar sua classe em um subnamespace desse provedor.</span><span class="sxs-lookup"><span data-stu-id="acd72-126">In contrast, if your new class derives from the class of another provider, you may need to store your class in a sub-namespace of that provider.</span></span> <span data-ttu-id="acd72-127">Observe que isso expõe sua nova classe à exclusão acidental pelo provedor original.</span><span class="sxs-lookup"><span data-stu-id="acd72-127">Note that this exposes your new class to accidental deletion by the original provider.</span></span>

<span data-ttu-id="acd72-128">O WMI fornece várias maneiras diferentes de criar um namespace:</span><span class="sxs-lookup"><span data-stu-id="acd72-128">WMI provides several different ways to create a namespace:</span></span>

-   [<span data-ttu-id="acd72-129">Criando um namespace filho com código MOF</span><span class="sxs-lookup"><span data-stu-id="acd72-129">Creating a Child Namespace with MOF Code</span></span>](creating-a-child-namespace-with-mof-code.md)
-   [<span data-ttu-id="acd72-130">Criando um namespace irmão com código MOF</span><span class="sxs-lookup"><span data-stu-id="acd72-130">Creating a Sibling Namespace with MOF Code</span></span>](creating-a-sibling-namespace-with-mof-code.md)
-   [<span data-ttu-id="acd72-131">Criando um namespace com a API do WMI</span><span class="sxs-lookup"><span data-stu-id="acd72-131">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a><span data-ttu-id="acd72-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="acd72-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acd72-133">Criando classes formato MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="acd72-133">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



