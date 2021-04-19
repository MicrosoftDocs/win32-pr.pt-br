---
description: Um provedor não é necessário para dar suporte a operações de instância parcial. No entanto, um provedor deve dar suporte a toda a semântica de uma operação de instância parcial, processar uma instância completa ou retornar \_ um \_ parâmetro WBEM E sem suporte \_ .
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Suporte a operações de Partial-Instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf656688ffbcc6981c6a3e55dc480570ad0f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786149"
---
# <a name="supporting-partial-instance-operations"></a><span data-ttu-id="73838-104">Suporte a operações de Partial-Instance</span><span class="sxs-lookup"><span data-stu-id="73838-104">Supporting Partial-Instance Operations</span></span>

<span data-ttu-id="73838-105">Um provedor não é necessário para dar suporte a operações de instância parcial.</span><span class="sxs-lookup"><span data-stu-id="73838-105">A provider is not required to support any partial-instance operations.</span></span> <span data-ttu-id="73838-106">No entanto, um provedor deve dar suporte a toda a semântica de uma operação de instância parcial, processar uma instância completa ou retornar um **\_ \_ \_ parâmetro WBEM E sem suporte**.</span><span class="sxs-lookup"><span data-stu-id="73838-106">However, a provider must either support all the semantics of a partial-instance operation, process a complete instance, or return **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="73838-107">Ao criar um provedor que dá suporte a operações de instância parcial, você deve observar as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="73838-107">When creating a provider that supports partial-instance operations, you must observe the following rules:</span></span>

-   <span data-ttu-id="73838-108">Reutilize o mesmo objeto de contexto que o WMI envia para o provedor.</span><span class="sxs-lookup"><span data-stu-id="73838-108">Reuse the same context object that WMI sends to the provider.</span></span> <span data-ttu-id="73838-109">O WMI usa o \_ \_ \_ \_ valor nomeado "obter \_ solicitação de cliente ext" para evitar deadlocks e remove esse cliente antes de encaminhar o objeto de contexto para um provedor.</span><span class="sxs-lookup"><span data-stu-id="73838-109">WMI uses the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value to prevent deadlocks and removes this client before forwarding the context object to a provider.</span></span>
-   <span data-ttu-id="73838-110">Para chamadas reentrantes no WMI que não exigem uma operação de instância parcial, certifique-se de repassar o mesmo objeto de contexto sem modificações.</span><span class="sxs-lookup"><span data-stu-id="73838-110">For reentrant calls back into WMI that do not require a partial-instance operation, ensure to pass back the same context object without any modifications.</span></span> <span data-ttu-id="73838-111">O WMI recebe o objeto de contexto sem o \_ \_ \_ valor nomeado "Get ext \_ cliente \_ Request" definido e exclui todos os valores nomeados associados a operações de instância parcial do objeto de contexto antes de passá-lo para outros provedores.</span><span class="sxs-lookup"><span data-stu-id="73838-111">WMI receives the context object without the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value set and deletes all named values associated with partial-instance operations from the context object before passing it to other providers.</span></span> <span data-ttu-id="73838-112">Não alterar o objeto de contexto impede que outros provedores recebam operações de recuperação de instância parcial destinadas a um objeto diferente e não relacionado.</span><span class="sxs-lookup"><span data-stu-id="73838-112">Not changing the context object blocks other providers from receiving partial-instance retrieval operations intended for a different, unrelated object.</span></span>
-   <span data-ttu-id="73838-113">Para executar uma operação reentrante na instância parcial ao realizar uma solicitação, defina o \_ \_ \_ \_ valor nomeado e a propriedade "obter solicitação de cliente ext \_ " ausente.</span><span class="sxs-lookup"><span data-stu-id="73838-113">To perform a reentrant partial-instance operation while carrying out a request, set the missing "\_\_GET\_EXT\_CLIENT\_REQUEST" named value and property clear.</span></span> <span data-ttu-id="73838-114">Opcionalmente, você pode modificar as propriedades no \_ \_ \_ valor nomeado "obter \_ Propriedades ext" antes de enviar o objeto de contexto de volta ao WMI com a chamada reentrante.</span><span class="sxs-lookup"><span data-stu-id="73838-114">Optionally, you can modify the properties in the "\_\_GET\_EXT\_PROPERTIES" named value before sending the context object back into WMI with the reentrant call.</span></span>
-   <span data-ttu-id="73838-115">Não acesse o objeto de contexto depois de devolvê-lo ao WMI durante uma chamada reentrante. outros provedores podem modificar as listas de propriedades ou outros valores durante a reentrância.</span><span class="sxs-lookup"><span data-stu-id="73838-115">Do not access the context object after you return it to WMI during a reentrant call; other providers may modify the property lists or other values during reentrancy.</span></span> <span data-ttu-id="73838-116">Você pode examinar ou modificar o objeto de contexto somente pela duração da chamada de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) implementada.</span><span class="sxs-lookup"><span data-stu-id="73838-116">You can examine or modify the context object only for the duration of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call that you implement.</span></span>

 

 



