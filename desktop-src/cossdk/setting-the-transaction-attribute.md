---
description: Você pode definir os atributos de transação manualmente usando a ferramenta administrativa serviços de componentes ou pode adicionar suporte programático a transações ao escrever seu componente.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Configurando o atributo de transação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0690a50f79c77a18b089cec1865dfbb9e7f428
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089493"
---
# <a name="setting-the-transaction-attribute"></a><span data-ttu-id="8c1f5-103">Configurando o atributo de transação</span><span class="sxs-lookup"><span data-stu-id="8c1f5-103">Setting the Transaction Attribute</span></span>

<span data-ttu-id="8c1f5-104">Você pode definir os atributos de transação manualmente usando a ferramenta administrativa serviços de componentes ou pode adicionar suporte programático a transações ao escrever seu componente.</span><span class="sxs-lookup"><span data-stu-id="8c1f5-104">You can set transaction attributes manually by using the Component Services administrative tool, or you can add programmatic support for transactions when you write your component.</span></span>

<span data-ttu-id="8c1f5-105">Para obter mais informações sobre valores de atributo de transação, consulte [Configuring Transactions](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="8c1f5-105">For more on transaction attribute values, see [Configuring Transactions](configuring-transactions.md).</span></span>

<span data-ttu-id="8c1f5-106">**Para definir o valor do atributo usando a ferramenta administrativa serviços de componentes**</span><span class="sxs-lookup"><span data-stu-id="8c1f5-106">**To set the attribute value by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="8c1f5-107">Na árvore de console, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="8c1f5-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="8c1f5-108">Na caixa de diálogo Propriedades do componente, clique na guia **Transações** .</span><span class="sxs-lookup"><span data-stu-id="8c1f5-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="8c1f5-109">Em **suporte a transações**, selecione a opção para o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="8c1f5-109">Under **Transaction support**, select the option for the value you want.</span></span> <span data-ttu-id="8c1f5-110">**Não há suporte** para o valor padrão de todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="8c1f5-110">The default value for all components is **Not Supported**.</span></span>

4.  <span data-ttu-id="8c1f5-111">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c1f5-111">Click **OK**.</span></span>

<span data-ttu-id="8c1f5-112">Você deve repetir este procedimento para cada componente.</span><span class="sxs-lookup"><span data-stu-id="8c1f5-112">You must repeat this procedure for each component.</span></span>

## <a name="to-set-the-attribute-value-programmatically"></a><span data-ttu-id="8c1f5-113">Para definir o valor do atributo programaticamente</span><span class="sxs-lookup"><span data-stu-id="8c1f5-113">To set the attribute value programmatically</span></span>

<span data-ttu-id="8c1f5-114">Os programadores que usam o Microsoft Visual Basic podem definir o atributo de transação com **MTSTransactionMode**, uma propriedade de módulo de classe para projetos DLL do ActiveX.</span><span class="sxs-lookup"><span data-stu-id="8c1f5-114">Programmers using Microsoft Visual Basic can set the transaction attribute with **MTSTransactionMode**, a class module property for ActiveX DLL projects.</span></span> <span data-ttu-id="8c1f5-115">Visual Basic mapeia sua seleção para o valor equivalente de atributo de transação COM+ e publica o valor na biblioteca de tipos do componente.</span><span class="sxs-lookup"><span data-stu-id="8c1f5-115">Visual Basic maps your selection to the equivalent COM+ transaction attribute value and publishes the value in your component's type library.</span></span>

<span data-ttu-id="8c1f5-116">A tabela a seguir mapeia cada valor constante **MTSTransactionMode** para seu valor de transação com+ equivalente.</span><span class="sxs-lookup"><span data-stu-id="8c1f5-116">The following table maps each **MTSTransactionMode** constant value to its equivalent COM+ transaction value.</span></span>



| <span data-ttu-id="8c1f5-117">Constante MTSTransactionMode</span><span class="sxs-lookup"><span data-stu-id="8c1f5-117">MTSTransactionMode constant</span></span>         | <span data-ttu-id="8c1f5-118">Valor da transação COM+</span><span class="sxs-lookup"><span data-stu-id="8c1f5-118">COM+ transaction value</span></span>             |
|-------------------------------------|------------------------------------|
| <span data-ttu-id="8c1f5-119">NotAnMTSObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c1f5-119">NotAnMTSObject (default)</span></span><br/> | <span data-ttu-id="8c1f5-120">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="8c1f5-120">Disabled</span></span><br/>                |
| <span data-ttu-id="8c1f5-121">Transtransações</span><span class="sxs-lookup"><span data-stu-id="8c1f5-121">NoTransactions</span></span><br/>           | <span data-ttu-id="8c1f5-122">Sem suporte (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c1f5-122">Not Supported (default)</span></span><br/> |
| <span data-ttu-id="8c1f5-123">RequiresTransaction</span><span class="sxs-lookup"><span data-stu-id="8c1f5-123">RequiresTransaction</span></span> <br/>     | <span data-ttu-id="8c1f5-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8c1f5-124">Required</span></span><br/>                |
| <span data-ttu-id="8c1f5-125">UsesTransaction</span><span class="sxs-lookup"><span data-stu-id="8c1f5-125">UsesTransaction</span></span> <br/>         | <span data-ttu-id="8c1f5-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8c1f5-126">Supported</span></span><br/>               |
| <span data-ttu-id="8c1f5-127">RequiresNewTransaction</span><span class="sxs-lookup"><span data-stu-id="8c1f5-127">RequiresNewTransaction</span></span> <br/>  | <span data-ttu-id="8c1f5-128">Requer novo</span><span class="sxs-lookup"><span data-stu-id="8c1f5-128">Requires New</span></span><br/>            |



 

<span data-ttu-id="8c1f5-129">A propriedade **MTSTransactionMode** também pode ser acessada programaticamente usando a API da biblioteca de administração do com+.</span><span class="sxs-lookup"><span data-stu-id="8c1f5-129">The **MTSTransactionMode** property can also be accessed programmatically by using the COM+ Administration Library API.</span></span>

 

 




