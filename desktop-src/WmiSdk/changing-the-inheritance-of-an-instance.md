---
description: Você pode encontrar uma situação em que uma instância que foi criada como um filho de uma classe pai deve alterar as classes pai e se tornar o filho de uma classe pai diferente.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Alterando a herança de uma instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828668"
---
# <a name="changing-the-inheritance-of-an-instance"></a><span data-ttu-id="3baa8-103">Alterando a herança de uma instância</span><span class="sxs-lookup"><span data-stu-id="3baa8-103">Changing the Inheritance of an Instance</span></span>

<span data-ttu-id="3baa8-104">Você pode encontrar uma situação em que uma instância que foi criada como um filho de uma classe pai deve alterar as classes pai e se tornar o filho de uma classe pai diferente.</span><span class="sxs-lookup"><span data-stu-id="3baa8-104">You may find a situation where an instance that was created as a child of one parent class must change parent classes and become the child of a different parent class.</span></span> <span data-ttu-id="3baa8-105">Por exemplo, você pode ter uma classe derivada, **ManualService**, descrevendo um serviço manual e uma classe derivada, **autoatendimento**, descrevendo um serviço automático.</span><span class="sxs-lookup"><span data-stu-id="3baa8-105">For example, you may have a derived class, **ManualService**, describing a manual service, and a derived class, **AutoService**, describing an automatic service.</span></span> <span data-ttu-id="3baa8-106">Ambas as classes têm um grande número de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3baa8-106">Both classes have a large number of properties.</span></span> <span data-ttu-id="3baa8-107">Nem todas as propriedades são idênticas.</span><span class="sxs-lookup"><span data-stu-id="3baa8-107">Not all properties are identical.</span></span> <span data-ttu-id="3baa8-108">Para alterar um serviço de manual para automático, você também deve alterar a instância que representa o serviço de **ManualService** para **autoatendimento**.</span><span class="sxs-lookup"><span data-stu-id="3baa8-108">To change a service from manual to automatic, you must also change the instance representing the service from **ManualService** to **AutoService**.</span></span> <span data-ttu-id="3baa8-109">Na versão atual do WMI, você não pode chamar o método [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) com o parâmetro *Pins* apontando para uma instância do **autoatendimento** e as propriedades de chave que descrevem a instância **ManualService** .</span><span class="sxs-lookup"><span data-stu-id="3baa8-109">In the current version of WMI, you cannot call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) method with the *pInst* parameter pointing to an instance of **AutoService** and the key properties describing the **ManualService** instance.</span></span> <span data-ttu-id="3baa8-110">Se você fizer isso, você excluirá implicitamente a instância **ManualService** original.</span><span class="sxs-lookup"><span data-stu-id="3baa8-110">If you do, you implicitly delete the original **ManualService** instance.</span></span> <span data-ttu-id="3baa8-111">Em essência, depois de estabelecer a classe de uma instância, você só pode alterar a classe pai de uma instância excluindo a instância e recriando a instância como uma instância da nova classe pai.</span><span class="sxs-lookup"><span data-stu-id="3baa8-111">In essence, after you establish the class of an instance, you can only change the parent class of an instance by deleting the instance and recreating the instance as an instance of the new parent class.</span></span>

<span data-ttu-id="3baa8-112">O procedimento a seguir descreve como mover uma instância de uma classe para outra classe.</span><span class="sxs-lookup"><span data-stu-id="3baa8-112">The following procedure describes how to move an instance from one class to another class.</span></span>

<span data-ttu-id="3baa8-113">**Para mover uma instância de uma classe para outra classe**</span><span class="sxs-lookup"><span data-stu-id="3baa8-113">**To move an instance from one class to another class**</span></span>

1.  <span data-ttu-id="3baa8-114">Exclua a instância da classe original.</span><span class="sxs-lookup"><span data-stu-id="3baa8-114">Delete the instance from the original class.</span></span>
2.  <span data-ttu-id="3baa8-115">Crie a instância na nova classe.</span><span class="sxs-lookup"><span data-stu-id="3baa8-115">Create the instance under the new class.</span></span>

    <span data-ttu-id="3baa8-116">O WMI não permite que os aplicativos movam uma instância criando-a na nova classe e, em seguida, atualizando-a com a chave da instância original.</span><span class="sxs-lookup"><span data-stu-id="3baa8-116">WMI does not allow applications to move an instance by creating it in the new class and then updating it with the key of the original instance.</span></span>

<span data-ttu-id="3baa8-117">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="3baa8-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



