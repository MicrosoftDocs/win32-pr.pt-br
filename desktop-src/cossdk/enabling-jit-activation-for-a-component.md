---
description: Habilitando a ativação JIT para um componente
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Habilitando a ativação JIT para um componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760059"
---
# <a name="enabling-jit-activation-for-a-component"></a><span data-ttu-id="94603-103">Habilitando a ativação JIT para um componente</span><span class="sxs-lookup"><span data-stu-id="94603-103">Enabling JIT Activation for a Component</span></span>

<span data-ttu-id="94603-104">Você deve configurar um componente para ser ativado por JIT somente quando ele for gravado corretamente para dar suporte ao serviço de ativação JIT (just-in-time) do COM+.</span><span class="sxs-lookup"><span data-stu-id="94603-104">You should configure a component to be JIT activated only when it is correctly written to support the COM+ Just-in-Time (JIT) Activation service.</span></span> <span data-ttu-id="94603-105">Se um componente for desativado entre chamadas de método, ele perderá qualquer estado associado.</span><span class="sxs-lookup"><span data-stu-id="94603-105">If a component is deactivated between method calls, it will lose any associated state.</span></span> <span data-ttu-id="94603-106">Devido ao comportamento padrão da ativação JIT, é improvável que isso ocorra quando você não espera, mas deve estar ciente dos requisitos de um componente antes de alterar sua configuração e das expectativas dos clientes que chamarão o componente.</span><span class="sxs-lookup"><span data-stu-id="94603-106">Given the default behavior of JIT Activation, this is unlikely to occur when you don't expect it to, but you should be aware of a component's requirements prior to changing its configuration and of the expectations of clients that will be calling the component.</span></span>

> [!Note]  
> <span data-ttu-id="94603-107">Se um componente estiver configurado para exigir transações, o serviço de ativação JIT do COM+ será habilitado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="94603-107">If a component is configured to require transactions, the COM+ JIT Activation service is enabled automatically.</span></span> <span data-ttu-id="94603-108">Você não pode desabilitá-lo nesse caso.</span><span class="sxs-lookup"><span data-stu-id="94603-108">You cannot disable it in this case.</span></span> <span data-ttu-id="94603-109">Para obter mais detalhes, consulte [Configurando transações](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="94603-109">For more detail, see [Configuring Transactions](configuring-transactions.md).</span></span>

 

<span data-ttu-id="94603-110">Quando você habilita a ativação JIT para um componente, seu atributo de sincronização é definido como obrigatório para esse componente.</span><span class="sxs-lookup"><span data-stu-id="94603-110">When you enable JIT Activation for a component, its synchronization attribute is set to required for that component.</span></span> <span data-ttu-id="94603-111">Nesse caso, você não pode alterar a configuração de sincronização.</span><span class="sxs-lookup"><span data-stu-id="94603-111">You cannot change the synchronization setting in this case.</span></span> <span data-ttu-id="94603-112">Para obter mais detalhes, consulte [dependências de sincronização](synchronization-dependencies.md).</span><span class="sxs-lookup"><span data-stu-id="94603-112">For more detail, see [Synchronization Dependencies](synchronization-dependencies.md).</span></span>

<span data-ttu-id="94603-113">**Para habilitar a ativação JIT**</span><span class="sxs-lookup"><span data-stu-id="94603-113">**To enable JIT Activation**</span></span>

1.  <span data-ttu-id="94603-114">No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="94603-114">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="94603-115">Na caixa de diálogo Propriedades do componente, clique na guia **ativação** .</span><span class="sxs-lookup"><span data-stu-id="94603-115">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="94603-116">Para habilitar a ativação JIT para o componente, marque a caixa de seleção **habilitar ativação Just in time** .</span><span class="sxs-lookup"><span data-stu-id="94603-116">To enable JIT activation for the component, select the **Enable Just In Time Activation** check box.</span></span>

4.  <span data-ttu-id="94603-117">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="94603-117">Click **OK**.</span></span>

<span data-ttu-id="94603-118">Quando você tiver habilitado a ativação JIT para um componente, terá a opção de habilitar o recurso auto-pronto para qualquer método exposto por esse componente.</span><span class="sxs-lookup"><span data-stu-id="94603-118">When you have enabled JIT Activation for a component, you have the option of enabling the auto-done feature for any method exposed by that component.</span></span> <span data-ttu-id="94603-119">Consulte [habilitando auto-pronto para um método](enabling-auto-done-for-a-method.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="94603-119">See [Enabling Auto-Done for a Method](enabling-auto-done-for-a-method.md) for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94603-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94603-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94603-121">Habilitando o auto-pronto para um método</span><span class="sxs-lookup"><span data-stu-id="94603-121">Enabling Auto-Done for a Method</span></span>](enabling-auto-done-for-a-method.md)
</dt> <dt>

[<span data-ttu-id="94603-122">Definindo o bit concluído</span><span class="sxs-lookup"><span data-stu-id="94603-122">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



