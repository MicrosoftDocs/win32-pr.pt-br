---
description: Outra maneira de criar um namespace é usar o código formato MOF (MOF) para criar um namespace irmão. Um namespace irmão é um namespace que não existe como um filho do namespace atual.
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: Criando um namespace irmão com código MOF
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4fcbf6e16ad51ab9a0df63e3497735b07cd6afc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750567"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a><span data-ttu-id="e670e-104">Criando um namespace irmão com código MOF</span><span class="sxs-lookup"><span data-stu-id="e670e-104">Creating a Sibling Namespace with MOF Code</span></span>

<span data-ttu-id="e670e-105">Outra maneira de criar um namespace é usar o código formato MOF (MOF) para criar um namespace irmão.</span><span class="sxs-lookup"><span data-stu-id="e670e-105">Another way of creating a namespace is to use Managed Object Format (MOF) code to create a sibling namespace.</span></span> <span data-ttu-id="e670e-106">Um namespace irmão é um namespace que não existe como um filho do namespace atual.</span><span class="sxs-lookup"><span data-stu-id="e670e-106">A sibling namespace is a namespace that does not exist as a child of the current namespace.</span></span>

<span data-ttu-id="e670e-107">O procedimento a seguir descreve como criar um namespace irmão com código MOF.</span><span class="sxs-lookup"><span data-stu-id="e670e-107">The following procedure describes how to create a sibling namespace with MOF code.</span></span>

<span data-ttu-id="e670e-108">**Para criar um namespace irmão com código MOF**</span><span class="sxs-lookup"><span data-stu-id="e670e-108">**To create a sibling namespace with MOF code**</span></span>

1.  <span data-ttu-id="e670e-109">Insira o comando de [**\# namespace pragma**](pragma-namespace.md) em seu código MOF antes da declaração do namespace.</span><span class="sxs-lookup"><span data-stu-id="e670e-109">Insert the [**\#pragma namespace**](pragma-namespace.md) command into your MOF code prior to the namespace declaration.</span></span>

    <span data-ttu-id="e670e-110">O comando [**\# pragma namespace**](pragma-namespace.md) instrui o WMI onde criar as instâncias seguindo a diretiva.</span><span class="sxs-lookup"><span data-stu-id="e670e-110">The [**\#pragma namespace**](pragma-namespace.md) command instructs WMI where to create the instances following the directive.</span></span>

2.  <span data-ttu-id="e670e-111">Crie uma instância da classe [**\_ \_ namespace**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="e670e-111">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>
3.  <span data-ttu-id="e670e-112">Compile seu código com o utilitário [Mofcomp](mofcomp.md) ou a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="e670e-112">Compile your code with the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="e670e-113">Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="e670e-113">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="e670e-114">O exemplo de código MOF a seguir descreve como criar um namespace como um irmão para o namespace "raiz \\ CIMv2".</span><span class="sxs-lookup"><span data-stu-id="e670e-114">The following MOF code example describes how to create a namespace as a sibling to the "Root\\CIMv2" namespace.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 



