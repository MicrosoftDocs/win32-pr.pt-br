---
description: Além de classes e instâncias, o WMI permite que você modifique um método. O principal motivo para você querer modificar um método é se você alterou a implementação de um método em um provedor. Para obter mais informações, consulte escrevendo um provedor de método.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Modificando um método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370555"
---
# <a name="modifying-a-method"></a><span data-ttu-id="b0dc1-105">Modificando um método</span><span class="sxs-lookup"><span data-stu-id="b0dc1-105">Modifying a Method</span></span>

<span data-ttu-id="b0dc1-106">Além de classes e instâncias, o WMI permite que você modifique um método.</span><span class="sxs-lookup"><span data-stu-id="b0dc1-106">In addition to classes and instances, WMI allows you to modify a method.</span></span> <span data-ttu-id="b0dc1-107">O principal motivo para você querer modificar um método é se você alterou a implementação de um método em um provedor.</span><span class="sxs-lookup"><span data-stu-id="b0dc1-107">The main reason you would want to modify a method is if you changed the implementation of a method in a provider.</span></span> <span data-ttu-id="b0dc1-108">Para obter mais informações, consulte [escrevendo um provedor de método](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b0dc1-108">For more information, see [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="b0dc1-109">Modificar um método não é uma operação que possa ser feita no script.</span><span class="sxs-lookup"><span data-stu-id="b0dc1-109">Modifying a method is not an operation that can be done in script.</span></span>

<span data-ttu-id="b0dc1-110">O procedimento a seguir descreve como modificar um método programaticamente.</span><span class="sxs-lookup"><span data-stu-id="b0dc1-110">The following procedure describes how to modify a method programmatically.</span></span>

<span data-ttu-id="b0dc1-111">**Para modificar um método programaticamente**</span><span class="sxs-lookup"><span data-stu-id="b0dc1-111">**To modify a method programmatically**</span></span>

1.  <span data-ttu-id="b0dc1-112">Recupere a definição de classe com uma chamada para [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span><span class="sxs-lookup"><span data-stu-id="b0dc1-112">Retrieve the class definition with a call to [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span></span>

    <span data-ttu-id="b0dc1-113">Os dois parâmetros de saída, *ppInSignature* e *ppOutSignature*, contêm a classe in-Parameter e a classe out-Parameter, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b0dc1-113">The two out parameters, *ppInSignature* and *ppOutSignature*, contain the in-parameter class and the out-parameter class, respectively.</span></span> <span data-ttu-id="b0dc1-114">O valor de retorno é agrupado na classe out-Parameter como uma propriedade e deve ser chamado **ReturnValue**.</span><span class="sxs-lookup"><span data-stu-id="b0dc1-114">The return value is bundled into the out-parameter class as a property, and should be named **ReturnValue**.</span></span>

2.  <span data-ttu-id="b0dc1-115">Recupere e modifique os parâmetros com chamadas para [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)ou [**IWbemClassObject::D xcluir**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span><span class="sxs-lookup"><span data-stu-id="b0dc1-115">Retrieve and modify the parameters with calls to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put), or [**IWbemClassObject::Delete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span></span>
3.  <span data-ttu-id="b0dc1-116">Coloque a nova versão do método novamente na classe pai com uma chamada para [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="b0dc1-116">Place your new version of the method back into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="b0dc1-117">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="b0dc1-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



