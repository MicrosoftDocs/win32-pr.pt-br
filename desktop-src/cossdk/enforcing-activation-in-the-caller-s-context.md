---
description: Impondo a ativação no contexto de chamadores
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Impondo a ativação no contexto de chamadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760426"
---
# <a name="enforcing-activation-in-the-callers-context"></a><span data-ttu-id="08a15-103">Impondo a ativação no contexto do chamador</span><span class="sxs-lookup"><span data-stu-id="08a15-103">Enforcing Activation in the Caller's Context</span></span>

<span data-ttu-id="08a15-104">Você pode controlar se um objeto é ativado em seu próprio contexto.</span><span class="sxs-lookup"><span data-stu-id="08a15-104">You can control whether an object gets activated in its own context.</span></span> <span data-ttu-id="08a15-105">Quando você usa a ferramenta administrativa serviços de componentes para exigir a ativação de componentes no contexto do chamador, ocorre o seguinte quando o COM+ ativa uma instância do componente em um contexto:</span><span class="sxs-lookup"><span data-stu-id="08a15-105">When you use the Component Services administrative tool to require component activation in the caller's context, the following occurs when COM+ activates an instance of the component in a context:</span></span>

-   <span data-ttu-id="08a15-106">O objeto é ativado no contexto do criador, se possível.</span><span class="sxs-lookup"><span data-stu-id="08a15-106">The object is activated in the creator's context if possible.</span></span>
-   <span data-ttu-id="08a15-107">A ativação do objeto falhará se exigir seu próprio contexto; \_ \_ A tentativa co e \_ de criar o \_ contexto de \_ \_ cliente externo \_ é retornada.</span><span class="sxs-lookup"><span data-stu-id="08a15-107">Object activation fails if it requires its own context; CO\_E\_ATTEMPT\_TO\_CREATE\_OUTSIDE\_CLIENT\_CONTEXT is returned.</span></span>

<span data-ttu-id="08a15-108">Se o objeto requer ou não seu próprio contexto depende de sua configuração relativa ao estado atual das propriedades de contexto do chamador.</span><span class="sxs-lookup"><span data-stu-id="08a15-108">Whether or not the object requires its own context depends on its configuration relative to the current state of the caller's context properties.</span></span> <span data-ttu-id="08a15-109">Para obter mais detalhes, consulte [contextos com+](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="08a15-109">For more detail, see [COM+ Contexts](com--contexts.md).</span></span>

<span data-ttu-id="08a15-110">Você desejaria controlar a ativação com esse nível de multa se algum aspecto do seu objeto não funcionar corretamente se ele tiver seu próprio contexto.</span><span class="sxs-lookup"><span data-stu-id="08a15-110">You would want to control activation at that fine a level if some aspect of your object would not function properly if it has its own context.</span></span> <span data-ttu-id="08a15-111">Por exemplo, se o componente não oferecer suporte a marshaling e tiver seu próprio contexto, todas as chamadas para ele falharão porque as chamadas de contexto cruzado são interceptadas e um Marshal leve realizado.</span><span class="sxs-lookup"><span data-stu-id="08a15-111">For example, if the component does not support marshaling and it has its own context, any calls to it will fail because cross-context calls are intercepted and a lightweight marshal performed.</span></span>

<span data-ttu-id="08a15-112">**Para impor a ativação no contexto do chamador**</span><span class="sxs-lookup"><span data-stu-id="08a15-112">**To enforce activation in the caller's context**</span></span>

1.  <span data-ttu-id="08a15-113">No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no componente (localizado na pasta **componentes** de qualquer aplicativo com+ selecionado) para o qual você está definindo as propriedades de ativação e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="08a15-113">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) for which you are setting activation properties and then click **Properties**.</span></span>

2.  <span data-ttu-id="08a15-114">Na caixa de diálogo Propriedades do componente, clique na guia **ativação** .</span><span class="sxs-lookup"><span data-stu-id="08a15-114">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="08a15-115">Selecione a caixa de seleção **deve ser ativada no contexto de chamadores** .</span><span class="sxs-lookup"><span data-stu-id="08a15-115">Select the **Must be activated in the callers context** check box.</span></span>

4.  <span data-ttu-id="08a15-116">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="08a15-116">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08a15-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08a15-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08a15-118">Conceitos de ativação Just-in-time COM+</span><span class="sxs-lookup"><span data-stu-id="08a15-118">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="08a15-119">Impondo ativação no contexto padrão</span><span class="sxs-lookup"><span data-stu-id="08a15-119">Enforcing Activation in the Default Context</span></span>](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



