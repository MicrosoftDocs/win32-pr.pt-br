---
description: Você pode habilitar o recurso auto-pronto para qualquer método exposto por um componente para o qual a ativação JIT do COM+ esteja habilitada. Se a ativação JIT estiver desabilitada, o auto-pronto não estará disponível.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Habilitando o auto-pronto para um método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771645"
---
# <a name="enabling-auto-done-for-a-method"></a><span data-ttu-id="1fdde-104">Habilitando o auto-pronto para um método</span><span class="sxs-lookup"><span data-stu-id="1fdde-104">Enabling Auto-Done for a Method</span></span>

<span data-ttu-id="1fdde-105">Você pode habilitar o recurso auto-pronto para qualquer método exposto por um componente para o qual a ativação JIT do COM+ esteja habilitada.</span><span class="sxs-lookup"><span data-stu-id="1fdde-105">You can enable the auto-done feature for any method exposed by a component for which COM+ JIT activation is enabled.</span></span> <span data-ttu-id="1fdde-106">Se a ativação JIT estiver desabilitada, o auto-pronto não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="1fdde-106">If JIT activation is disabled, auto-done is unavailable.</span></span>

<span data-ttu-id="1fdde-107">Você deve habilitar o auto-pronto apenas para um método que foi escrito intencionalmente para tirar proveito dele, pois esse recurso pode potencialmente alterar o comportamento esperado do método.</span><span class="sxs-lookup"><span data-stu-id="1fdde-107">You should enable auto-done only for a method that has intentionally been written to take advantage of it because this feature can potentially change the expected behavior of the method.</span></span>

<span data-ttu-id="1fdde-108">Quando você habilita o auto-pronto, você está alterando o comportamento padrão da ativação JIT e das transações automáticas para esse método.</span><span class="sxs-lookup"><span data-stu-id="1fdde-108">When you enable auto-done, you are changing the default behavior of both JIT activation and automatic transactions for that method.</span></span> <span data-ttu-id="1fdde-109">Talvez você queira usar esse recurso porque ele pode remover a necessidade de declarar explicitamente a consistência e a conclusão.</span><span class="sxs-lookup"><span data-stu-id="1fdde-109">You may want to use this feature because it can remove the necessity to explicitly declare consistency and doneness.</span></span> <span data-ttu-id="1fdde-110">Em vez disso, isso pode ser feito simplesmente retornando um HRESULT quando a conclusão automática está habilitada.</span><span class="sxs-lookup"><span data-stu-id="1fdde-110">This can instead be done by simply returning an HRESULT when auto-done is enabled.</span></span> <span data-ttu-id="1fdde-111">Essencialmente, ao habilitar o auto-pronto, você está instruindo o COM+ a fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1fdde-111">Essentially, when you enable auto-done, you are instructing COM+ to do the following:</span></span>

-   <span data-ttu-id="1fdde-112">Defina o bit Done como true por padrão no contexto no qual o objeto é executado sempre que esse método for chamado.</span><span class="sxs-lookup"><span data-stu-id="1fdde-112">Set the done bit to True by default on the context in which the object runs whenever this method is called.</span></span>
-   <span data-ttu-id="1fdde-113">Inspecione o HRESULT retornado pelo método; Se ele indicar êxito ou falha, defina o bit de consistência de acordo.</span><span class="sxs-lookup"><span data-stu-id="1fdde-113">Inspect the HRESULT returned by the method; if it indicates SUCCESS or FAILURE, set the consistency bit accordingly.</span></span> <span data-ttu-id="1fdde-114">Isso pode resultar em uma chamada automática para [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ou [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), dependendo também do que o método faz internamente.</span><span class="sxs-lookup"><span data-stu-id="1fdde-114">This can result in an automatic call to [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) or [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), depending also on what the method does internally.</span></span>

<span data-ttu-id="1fdde-115">**Para habilitar o auto-pronto para um método**</span><span class="sxs-lookup"><span data-stu-id="1fdde-115">**To enable auto-done for a method**</span></span>

1.  <span data-ttu-id="1fdde-116">No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no método que você deseja configurar e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="1fdde-116">In the details pane of the Component Services administrative tool, right-click the method that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="1fdde-117">Na caixa de diálogo Propriedades do método, clique na guia **geral** .</span><span class="sxs-lookup"><span data-stu-id="1fdde-117">In the method properties dialog box, click the **General** tab.</span></span>

3.  <span data-ttu-id="1fdde-118">Para habilitar o auto-pronto, marque a caixa de seleção **desativar automaticamente este objeto quando este método for retornado** .</span><span class="sxs-lookup"><span data-stu-id="1fdde-118">To enable auto-done, select the **Automatically deactivate this object when this method returns** check box.</span></span> <span data-ttu-id="1fdde-119">Se a caixa de seleção não estiver disponível, você deverá primeiro habilitar a ativação JIT para o componente.</span><span class="sxs-lookup"><span data-stu-id="1fdde-119">If the check box is unavailable, you must first enable JIT Activation for the component.</span></span> <span data-ttu-id="1fdde-120">(Consulte[habilitando a ativação JIT para um componente](enabling-jit-activation-for-a-component.md) para obter instruções detalhadas.)</span><span class="sxs-lookup"><span data-stu-id="1fdde-120">(See[Enabling JIT Activation for a Component](enabling-jit-activation-for-a-component.md) for detailed instructions.)</span></span>

4.  <span data-ttu-id="1fdde-121">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1fdde-121">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fdde-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1fdde-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fdde-123">Conceitos de ativação Just-in-time COM+</span><span class="sxs-lookup"><span data-stu-id="1fdde-123">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="1fdde-124">Habilitando a ativação JIT para um componente</span><span class="sxs-lookup"><span data-stu-id="1fdde-124">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="1fdde-125">Definindo o bit concluído</span><span class="sxs-lookup"><span data-stu-id="1fdde-125">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



