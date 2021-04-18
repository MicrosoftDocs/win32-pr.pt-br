---
description: Ao contrário da exclusão de uma instância dinâmica, a exclusão de uma classe é um procedimento simples.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Excluindo uma classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798378"
---
# <a name="deleting-a-class"></a><span data-ttu-id="8f8d1-103">Excluindo uma classe</span><span class="sxs-lookup"><span data-stu-id="8f8d1-103">Deleting a Class</span></span>

<span data-ttu-id="8f8d1-104">Ao contrário da exclusão de uma instância dinâmica, a exclusão de uma classe é um procedimento simples.</span><span class="sxs-lookup"><span data-stu-id="8f8d1-104">Unlike deleting a dynamic instance, deleting a class is a simple procedure.</span></span> <span data-ttu-id="8f8d1-105">No entanto, conforme discutido anteriormente, as classes base ou derivadas raramente são excluídas.</span><span class="sxs-lookup"><span data-stu-id="8f8d1-105">However, as discussed earlier, base or derived classes are rarely deleted.</span></span> <span data-ttu-id="8f8d1-106">Em vez disso, uma instância é mais comumente excluída.</span><span class="sxs-lookup"><span data-stu-id="8f8d1-106">Instead, an instance is more commonly deleted.</span></span> <span data-ttu-id="8f8d1-107">A [API de script para WMI](scripting-api-for-wmi.md) usa os mesmos métodos para excluir um objeto de classe ou uma instância.</span><span class="sxs-lookup"><span data-stu-id="8f8d1-107">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span> <span data-ttu-id="8f8d1-108">Para obter mais informações, consulte [excluindo uma instância](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="8f8d1-108">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span> <span data-ttu-id="8f8d1-109">Para obter informações sobre como remover classes e instâncias do repositório do WMI, consulte o comando de pré-processador do [**pragma DeleteClass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="8f8d1-109">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="8f8d1-110">A [API com para WMI](com-api-for-wmi.md) tem métodos diferentes para excluir uma instância e excluir um objeto.</span><span class="sxs-lookup"><span data-stu-id="8f8d1-110">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="8f8d1-111">O procedimento a seguir descreve como excluir uma classe base ou classe derivada.</span><span class="sxs-lookup"><span data-stu-id="8f8d1-111">The following procedure describes how to delete a base class or derived class.</span></span>

<span data-ttu-id="8f8d1-112">**Para excluir uma classe base ou classe derivada**</span><span class="sxs-lookup"><span data-stu-id="8f8d1-112">**To delete a base class or derived class**</span></span>

-   <span data-ttu-id="8f8d1-113">Chame o método [**IWbemServices::D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) ou [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) .</span><span class="sxs-lookup"><span data-stu-id="8f8d1-113">Call either the [**IWbemServices::DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) or [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) method.</span></span>

    <span data-ttu-id="8f8d1-114">Como o nome sugere, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) exclui uma instância assincronamente enquanto [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) exclui uma instância de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="8f8d1-114">As the name suggests, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) deletes an instance asynchronously while [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) deletes an instance synchronously.</span></span> <span data-ttu-id="8f8d1-115">Para usar o **DeleteClassAsync**, você também deve implementar um objeto [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="8f8d1-115">To use **DeleteClassAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="8f8d1-116">Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8f8d1-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="8f8d1-117">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8f8d1-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



