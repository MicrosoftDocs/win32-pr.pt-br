---
description: Quando um objeto é ativado em um determinado contexto, as chamadas subsequentes para ou dele, dentro do contexto, são manipuladas de forma diferente do que as chamadas no limite de contexto.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Interceptação de chamadas de contexto cruzado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296101"
---
# <a name="interception-of-cross-context-calls"></a><span data-ttu-id="db2ff-103">Interceptação de chamadas de contexto cruzado</span><span class="sxs-lookup"><span data-stu-id="db2ff-103">Interception of Cross-Context Calls</span></span>

<span data-ttu-id="db2ff-104">Quando um objeto é ativado em um determinado contexto, as chamadas subsequentes para ou dele, dentro do contexto, são manipuladas de forma diferente do que as chamadas no limite de contexto.</span><span class="sxs-lookup"><span data-stu-id="db2ff-104">When an object is activated in a given context, subsequent calls to or from it, within the context, are handled differently than calls across the context boundary.</span></span> <span data-ttu-id="db2ff-105">Chamadas entre o limite de contexto são manipuladas com proxies leves.</span><span class="sxs-lookup"><span data-stu-id="db2ff-105">Calls across the context boundary are handled with lightweight proxies.</span></span> <span data-ttu-id="db2ff-106">Esses proxies tratam de qualquer mediação necessária para ajustar o ambiente de tempo de execução de um que acomoda o chamador para um que acomode o receptor.</span><span class="sxs-lookup"><span data-stu-id="db2ff-106">These proxies handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span> <span data-ttu-id="db2ff-107">Esse processo é conhecido como *interceptação*.</span><span class="sxs-lookup"><span data-stu-id="db2ff-107">This process is known as *interception*.</span></span>

<span data-ttu-id="db2ff-108">A interceptação de chamada entre contexto é necessária porque os objetos em contextos diferentes têm requisitos de tempo de execução diferentes — isso é precisamente o motivo para contextos.</span><span class="sxs-lookup"><span data-stu-id="db2ff-108">Cross-context call interception is necessary because objects in different contexts have different run-time requirements—this is precisely the reason for contexts.</span></span> <span data-ttu-id="db2ff-109">O COM+ intercepta todas as referências de objeto que você passa como parâmetros de método e as converte automaticamente em proxies para que elas sejam utilizáveis no novo contexto.</span><span class="sxs-lookup"><span data-stu-id="db2ff-109">COM+ intercepts any object references that you pass as method parameters and automatically converts them to proxies so that they are usable in the new context.</span></span>

<span data-ttu-id="db2ff-110">Se você compartilhar referências de objeto entre limites de contexto por outros meios — por exemplo, em variáveis globais — você deve sempre usar [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="db2ff-110">If you share object references across context boundaries by other means—for example, in global variables—you should always use [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> <span data-ttu-id="db2ff-111">Essas funções podem converter uma referência de objeto em um proxy utilizável em um contexto diferente.</span><span class="sxs-lookup"><span data-stu-id="db2ff-111">These functions can translate an object reference into a proxy usable in a different context.</span></span> <span data-ttu-id="db2ff-112">Nunca compartilhe uma referência de objeto bruto entre limites de contexto.</span><span class="sxs-lookup"><span data-stu-id="db2ff-112">Never share a raw object reference across context boundaries.</span></span>

<span data-ttu-id="db2ff-113">O comportamento de chamadas entre o contexto pode ter consequências indesejadas no caso de objetos expondo interfaces que não podem ser empacotadas.</span><span class="sxs-lookup"><span data-stu-id="db2ff-113">The behavior of calls across context can have unwanted consequences in the case of objects exposing interfaces that cannot be marshaled.</span></span> <span data-ttu-id="db2ff-114">Nessa circunstância, é provável que você queira insistir que o objeto que não pode ser empacotado seja ativado somente no contexto de seu chamador e nunca em seu próprio contexto.</span><span class="sxs-lookup"><span data-stu-id="db2ff-114">In this circumstance, you are likely to want to insist that the object that cannot be marshaled be activated only in the context of its caller and never in its own context.</span></span> <span data-ttu-id="db2ff-115">Você pode fazer isso selecionando a opção **deve ser ativada no contexto do chamador** na guia **ativação** da página **Propriedades** do componente.</span><span class="sxs-lookup"><span data-stu-id="db2ff-115">You can do this by selecting the **Must be activated in caller's context** option on the **Activation** tab of the component **Properties** page.</span></span> <span data-ttu-id="db2ff-116">(Consulte [impondo a ativação no contexto do chamador](enforcing-activation-in-the-caller-s-context.md) para obter instruções passo a passo.)</span><span class="sxs-lookup"><span data-stu-id="db2ff-116">(See [Enforcing Activation in the Caller's Context](enforcing-activation-in-the-caller-s-context.md) for step-by-step instructions.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="db2ff-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db2ff-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db2ff-118">Ativação de contexto</span><span class="sxs-lookup"><span data-stu-id="db2ff-118">Context activation</span></span>](context-activation.md)
</dt> </dl>

 

 
