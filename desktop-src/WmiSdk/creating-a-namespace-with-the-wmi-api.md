---
description: Outra maneira de criar um namespace é usar a API do WMI para criar o namespace de forma programática.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Criando um namespace com a API do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815471"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a><span data-ttu-id="14895-103">Criando um namespace com a API do WMI</span><span class="sxs-lookup"><span data-stu-id="14895-103">Creating a Namespace with the WMI API</span></span>

<span data-ttu-id="14895-104">Outra maneira de criar um namespace é usar a API do WMI para criar o namespace de forma programática.</span><span class="sxs-lookup"><span data-stu-id="14895-104">Another way of creating a namespace is to use the WMI API to create the namespace programmatically.</span></span> <span data-ttu-id="14895-105">A vantagem de criar um namespace de forma programática é que você pode criar o namespace de dentro de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14895-105">The advantage to creating a namespace programmatically is that you can create the namespace from within an application.</span></span> <span data-ttu-id="14895-106">No entanto, o uso da API do WMI é mais complexo do que usar o código formato MOF (MOF) e não é possível compartilhar facilmente seus namespaces com outros desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="14895-106">However, using the WMI API is more complex than using Managed Object Format (MOF) code, and you cannot as easily share your namespaces with other developers.</span></span>

<span data-ttu-id="14895-107">O procedimento a seguir descreve como criar um namespace usando a API do WMI.</span><span class="sxs-lookup"><span data-stu-id="14895-107">The following procedure describes how to create a namespace using the WMI API.</span></span>

<span data-ttu-id="14895-108">**Para criar um namespace usando a API do WMI**</span><span class="sxs-lookup"><span data-stu-id="14895-108">**To create a namespace using the WMI API**</span></span>

1.  <span data-ttu-id="14895-109">Use [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar um ponteiro para um objeto [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que aponta para a classe de sistema de [**\_ \_ namespace**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="14895-109">Use [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a pointer to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) object that points to the [**\_\_Namespace**](--namespace.md) system class.</span></span>
2.  <span data-ttu-id="14895-110">Defina uma instância da classe de sistema de [**\_ \_ namespace**](--namespace.md) com uma chamada para [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span><span class="sxs-lookup"><span data-stu-id="14895-110">Define an instance of the [**\_\_Namespace**](--namespace.md) system class with a call to [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span></span>
3.  <span data-ttu-id="14895-111">Defina a propriedade **Name** da instância do [**\_ \_ namespace**](--namespace.md) com uma chamada para [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="14895-111">Set the **Name** property of the [**\_\_Namespace**](--namespace.md) instance with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>
4.  <span data-ttu-id="14895-112">Crie o namespace com uma chamada para [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span><span class="sxs-lookup"><span data-stu-id="14895-112">Create the namespace with a call to [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span></span>

    <span data-ttu-id="14895-113">O parâmetro *Pins* de [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) deve apontar para a nova instância.</span><span class="sxs-lookup"><span data-stu-id="14895-113">The *pInst* parameter of [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) should point to the new instance.</span></span>

 

 



