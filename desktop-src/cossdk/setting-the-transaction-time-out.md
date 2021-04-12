---
description: Você pode definir manualmente o tempo limite para as transações usando a ferramenta administrativa serviços de componentes ou pode configurar programaticamente o tempo limite usando as interfaces de administração do COM+.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Definindo a transação Time-Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457140"
---
# <a name="setting-the-transaction-time-out"></a><span data-ttu-id="f94f2-103">Definindo a transação Time-Out</span><span class="sxs-lookup"><span data-stu-id="f94f2-103">Setting the Transaction Time-Out</span></span>

<span data-ttu-id="f94f2-104">Você pode definir manualmente o tempo limite para as transações usando a ferramenta administrativa serviços de componentes ou pode configurar programaticamente o tempo limite usando as interfaces de [Administração do com+](com--administration-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f94f2-104">You can manually set the time-out for transactions by using the Component Services administrative tool, or you can programmatically configure the time-out by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span> <span data-ttu-id="f94f2-105">O tempo limite pode ser configurado no nível do computador local e também para componentes individuais.</span><span class="sxs-lookup"><span data-stu-id="f94f2-105">The time-out can be configured at the local computer level and also for individual components.</span></span>

<span data-ttu-id="f94f2-106">**Para definir o tempo limite da transação para o computador local usando a ferramenta administrativa serviços de componentes**</span><span class="sxs-lookup"><span data-stu-id="f94f2-106">**To set the transaction time-out for the local computer by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="f94f2-107">Na árvore de console, clique com o botão direito do mouse no computador local que você deseja configurar e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="f94f2-107">In the console tree, right-click the local computer you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="f94f2-108">Na caixa de diálogo Propriedades do computador, clique na guia **Opções** .</span><span class="sxs-lookup"><span data-stu-id="f94f2-108">In the computer properties dialog box, click the **Options** tab.</span></span>

3.  <span data-ttu-id="f94f2-109">Em **tempo limite da transação**, insira o tempo limite da transação em segundos.</span><span class="sxs-lookup"><span data-stu-id="f94f2-109">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="f94f2-110">O tempo limite padrão é de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="f94f2-110">The default time-out is 60 seconds.</span></span>

4.  <span data-ttu-id="f94f2-111">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f94f2-111">Click **OK**.</span></span>

<span data-ttu-id="f94f2-112">**Para definir o tempo limite da transação para um componente usando a ferramenta administrativa serviços de componentes**</span><span class="sxs-lookup"><span data-stu-id="f94f2-112">**To set the transaction time-out for a component by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="f94f2-113">Na árvore de console, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="f94f2-113">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="f94f2-114">Na caixa de diálogo Propriedades do componente, clique na guia **Transações** .</span><span class="sxs-lookup"><span data-stu-id="f94f2-114">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="f94f2-115">Marque a caixa rotulada **substituir valor de tempo limite de transação global**.</span><span class="sxs-lookup"><span data-stu-id="f94f2-115">Check the box labeled **Override global transaction timeout value**.</span></span>

    > [!Note]  
    > <span data-ttu-id="f94f2-116">Você não poderá marcar a caixa para substituir o valor de tempo limite da transação global se o **suporte à transação** estiver definido como **desabilitado**, **sem suporte** ou **com suporte**.</span><span class="sxs-lookup"><span data-stu-id="f94f2-116">You cannot check the box to override the global transaction time-out value if the **Transaction support** is set to **Disabled**, **Not Supported**, or **Supported**.</span></span>

     

4.  <span data-ttu-id="f94f2-117">Em **tempo limite da transação**, insira o tempo limite da transação em segundos.</span><span class="sxs-lookup"><span data-stu-id="f94f2-117">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="f94f2-118">O tempo limite padrão é de 0 segundos, o que significa que o componente nunca fará com que a transação expire o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="f94f2-118">The default time-out is 0 seconds, which means that the component will never cause the transaction to time out.</span></span>

5.  <span data-ttu-id="f94f2-119">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f94f2-119">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f94f2-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f94f2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f94f2-121">Gerenciando transações automáticas no COM+</span><span class="sxs-lookup"><span data-stu-id="f94f2-121">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



