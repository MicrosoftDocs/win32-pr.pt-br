---
description: Você pode definir manualmente o nível de isolamento da transação de componentes usando a ferramenta administrativa serviços de componentes ou pode configurar programaticamente o nível de isolamento da transação para um componente usando as interfaces de administração do COM+.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Configurar o nível de isolamento da transação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646485"
---
# <a name="setting-the-transaction-isolation-level"></a><span data-ttu-id="d7e39-103">Configurar o nível de isolamento da transação</span><span class="sxs-lookup"><span data-stu-id="d7e39-103">Setting the Transaction Isolation Level</span></span>

<span data-ttu-id="d7e39-104">Você pode definir manualmente o nível de isolamento da transação de componentes usando a ferramenta administrativa serviços de componentes ou pode configurar programaticamente o nível de isolamento da transação para um componente usando as [interfaces de administração do com+](com--administration-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d7e39-104">You can manually set the transaction isolation level of components by using the Component Services administrative tool, or you can programmatically configure the transaction isolation level for a component by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span>

<span data-ttu-id="d7e39-105">Para obter mais informações sobre níveis de isolamento de transação, consulte [Configuring TRANSACTION ISOLATION Levels](configuring-transaction-isolation-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d7e39-105">For more on transaction isolation levels, see [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md).</span></span>

<span data-ttu-id="d7e39-106">**Para definir o nível de isolamento da transação usando a ferramenta administrativa serviços de componentes**</span><span class="sxs-lookup"><span data-stu-id="d7e39-106">**To set the transaction isolation level by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="d7e39-107">Na árvore de console, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="d7e39-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="d7e39-108">Na caixa de diálogo Propriedades do componente, clique na guia **Transações** .</span><span class="sxs-lookup"><span data-stu-id="d7e39-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="d7e39-109">Em **nível de isolamento da transação**, selecione o valor desejado na caixa suspensa.</span><span class="sxs-lookup"><span data-stu-id="d7e39-109">Under **Transaction Isolation Level**, select the value you want from the drop-down box.</span></span> <span data-ttu-id="d7e39-110">O valor padrão para todos os componentes é **serializado**.</span><span class="sxs-lookup"><span data-stu-id="d7e39-110">The default value for all components is **Serialized**.</span></span>

    > [!Note]  
    > <span data-ttu-id="d7e39-111">Se **desabilitado** ou **sem suporte** for selecionado em **suporte a transações**, você não poderá definir o nível de isolamento da transação.</span><span class="sxs-lookup"><span data-stu-id="d7e39-111">If either **Disabled** or **Not Supported** is selected under **Transaction support**, you cannot set the transaction isolation level.</span></span>

     

4.  <span data-ttu-id="d7e39-112">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7e39-112">Click **OK**.</span></span>

<span data-ttu-id="d7e39-113">Você deve repetir este procedimento para cada componente.</span><span class="sxs-lookup"><span data-stu-id="d7e39-113">You must repeat this procedure for each component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7e39-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7e39-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7e39-115">Configurando níveis de isolamento da transação</span><span class="sxs-lookup"><span data-stu-id="d7e39-115">Configuring Transaction Isolation Levels</span></span>](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



