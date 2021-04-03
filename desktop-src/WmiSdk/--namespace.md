---
description: Representa um namespace WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: Classe __Namespace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 9f396b588f372f26a808e97593ffcc30eac9b3ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836948"
---
# <a name="__namespace-class"></a><span data-ttu-id="fc672-103">\_\_Classe de namespace</span><span class="sxs-lookup"><span data-stu-id="fc672-103">\_\_Namespace class</span></span>

<span data-ttu-id="fc672-104">A classe de sistema **\_ \_ namespace** representa um namespace WMI.</span><span class="sxs-lookup"><span data-stu-id="fc672-104">The **\_\_Namespace** system class represents a WMI namespace.</span></span>

<span data-ttu-id="fc672-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fc672-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fc672-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="fc672-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc672-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc672-107">Syntax</span></span>

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="fc672-108">Membros</span><span class="sxs-lookup"><span data-stu-id="fc672-108">Members</span></span>

<span data-ttu-id="fc672-109">A classe **\_ \_ namespace** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fc672-109">The **\_\_Namespace** class has these types of members:</span></span>

-   [<span data-ttu-id="fc672-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc672-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc672-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc672-111">Properties</span></span>

<span data-ttu-id="fc672-112">A classe **\_ \_ namespace** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fc672-112">The **\_\_Namespace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc672-113">**Nome**</span><span class="sxs-lookup"><span data-stu-id="fc672-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc672-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc672-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc672-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fc672-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc672-116">Qualificadores: [ **chave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fc672-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fc672-117">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="fc672-117">Namespace name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc672-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc672-118">Remarks</span></span>

<span data-ttu-id="fc672-119">A classe de **\_ \_ namespace** é derivada de [**\_ \_ SystemClass**](--systemclass.md), que não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="fc672-119">The **\_\_Namespace** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="fc672-120">Você pode usar o **\_ \_ namespace** para identificar, criar e excluir namespaces filho no namespace de trabalho atual para o qual você tem um objeto [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="fc672-120">You can use **\_\_Namespace** to identify, create, and delete child namespaces within the current working namespace for which you have an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) object.</span></span> <span data-ttu-id="fc672-121">A criação de uma nova instância do **\_ \_ namespace** em qualquer namespace de trabalho cria um namespace filho dentro do namespace de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fc672-121">Creating a new instance of **\_\_Namespace** within any working namespace creates a child namespace within the working namespace.</span></span> <span data-ttu-id="fc672-122">Por outro lado, a exclusão de uma instância do **\_ \_ namespace** remove o namespace filho do namespace de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fc672-122">Conversely, deleting an instance of **\_\_Namespace** removes the child namespace from the working namespace.</span></span> <span data-ttu-id="fc672-123">Observe que a exclusão de um namespace filho também exclui todas as suas classes e instâncias.</span><span class="sxs-lookup"><span data-stu-id="fc672-123">Note that deleting a child namespace also deletes all of its classes and instances.</span></span>

<span data-ttu-id="fc672-124">Enumerar instâncias dessa classe dentro de qualquer namespace de trabalho fornece os namespaces filho disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fc672-124">Enumerating instances of this class within any working namespace gives the available child namespaces.</span></span>

<span data-ttu-id="fc672-125">Por exemplo, dentro do \\ namespace raiz há duas instâncias de **\_ \_ namespace**.</span><span class="sxs-lookup"><span data-stu-id="fc672-125">For example, within the \\root namespace are two instances of **\_\_Namespace**.</span></span> <span data-ttu-id="fc672-126">Uma tem sua propriedade **Name** definida como "padrão", a outra tem o **nome** definido como "Cimv2".</span><span class="sxs-lookup"><span data-stu-id="fc672-126">One has its **Name** property set to "Default," the other has **Name** set to "Cimv2."</span></span> <span data-ttu-id="fc672-127">Essas instâncias representam os \\ \\ namespaces raiz padrão \\ e \\ cimv2 raiz, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fc672-127">These instances represent the \\root\\default, and \\root\\cimv2 namespaces, respectively.</span></span>

## <a name="examples"></a><span data-ttu-id="fc672-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc672-128">Examples</span></span>

<span data-ttu-id="fc672-129">O exemplo de VBScript [listar todos os namespaces WMI](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) na galeria do TechNet usa uma chamada recursiva para listar todas as instâncias da \_ \_ classe namespace em um sistema.</span><span class="sxs-lookup"><span data-stu-id="fc672-129">The [List All WMI Namespaces](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) VBScript example on the TechNet Gallery uses a recursive call to list all instances of the \_\_Namespace class on a system.</span></span>

<span data-ttu-id="fc672-130">O exemplo de código a seguir recupera todos os namespaces no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc672-130">The following code sample retrieves all namespaces in PowerShell.</span></span>


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



<span data-ttu-id="fc672-131">O exemplo de código a seguir melhora o exemplo anterior e adiciona informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="fc672-131">The following code sample improves on the previous sample, and adds in additional information.</span></span>


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a><span data-ttu-id="fc672-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc672-132">Requirements</span></span>



| <span data-ttu-id="fc672-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc672-133">Requirement</span></span> | <span data-ttu-id="fc672-134">Valor</span><span class="sxs-lookup"><span data-stu-id="fc672-134">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fc672-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc672-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fc672-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc672-136">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fc672-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc672-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fc672-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc672-138">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="fc672-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc672-139">Namespace</span></span><br/>                | <span data-ttu-id="fc672-140">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="fc672-140">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="fc672-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc672-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc672-142">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="fc672-142">**\_\_SystemClass**</span></span>](--systemclass.md)
</dt> <dt>

[<span data-ttu-id="fc672-143">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="fc672-143">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




