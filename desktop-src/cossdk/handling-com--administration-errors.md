---
description: Manipulando erros de administração COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Manipulando erros de administração COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780702"
---
# <a name="handling-com-administration-errors"></a><span data-ttu-id="aec4a-103">Manipulando erros de administração COM+</span><span class="sxs-lookup"><span data-stu-id="aec4a-103">Handling COM+ Administration Errors</span></span>

<span data-ttu-id="aec4a-104">Os erros gerados ao usar os objetos COMAdmin são relatados de duas maneiras, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="aec4a-104">Errors that are generated when using the COMAdmin objects are reported in two ways, as follows:</span></span>

-   <span data-ttu-id="aec4a-105">Usando códigos de erro específicos para a biblioteca COMAdmin.</span><span class="sxs-lookup"><span data-stu-id="aec4a-105">Using error codes specific to the COMAdmin library.</span></span>
-   <span data-ttu-id="aec4a-106">Usando informações de erro estendidas disponíveis em uma coleção de [**errorInfo**](errorinfo.md) especial.</span><span class="sxs-lookup"><span data-stu-id="aec4a-106">Using extended error information available in a special [**ErrorInfo**](errorinfo.md) collection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aec4a-107">Códigos de erro</span><span class="sxs-lookup"><span data-stu-id="aec4a-107">Error Codes</span></span>

<span data-ttu-id="aec4a-108">Você lida com códigos de erro de administração como faria COM qualquer mensagem de erro COM.</span><span class="sxs-lookup"><span data-stu-id="aec4a-108">You handle administration error codes as you would any COM error message.</span></span> <span data-ttu-id="aec4a-109">No Microsoft Visual C++, esses códigos são retornados como valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aec4a-109">In Microsoft Visual C++, these codes are returned as **HRESULT** values.</span></span> <span data-ttu-id="aec4a-110">No Microsoft Visual Basic, eles são lançados como exceções que você pode capturar.</span><span class="sxs-lookup"><span data-stu-id="aec4a-110">In Microsoft Visual Basic, they are thrown as exceptions that you can catch.</span></span> <span data-ttu-id="aec4a-111">Para programadores do C++, os códigos de erro da administração COM+ são definidos no Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="aec4a-111">For C++ programmers, the COM+ administration error codes are defined in Winerror.h.</span></span> <span data-ttu-id="aec4a-112">Para os programadores Visual Basic, eles estão disponíveis por meio do IDE do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="aec4a-112">For Visual Basic programmers, they are available through the Visual Basic IDE.</span></span>

## <a name="errorinfo-collection"></a><span data-ttu-id="aec4a-113">Coleção ErrorInfo</span><span class="sxs-lookup"><span data-stu-id="aec4a-113">ErrorInfo Collection</span></span>

<span data-ttu-id="aec4a-114">Quando ocorre um erro, sinalizado por algum tipo de código de falha, informações mais detalhadas podem estar disponíveis, dependendo da natureza do erro.</span><span class="sxs-lookup"><span data-stu-id="aec4a-114">When an error occurs, signaled by some kind of failure code, more detailed information may be available, depending on the nature of the error.</span></span> <span data-ttu-id="aec4a-115">Os objetos COMAdmin fornecem informações estendidas em circunstâncias em que a causa exata da falha é difícil de determinar sem um relatório detalhado, como com várias operações de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="aec4a-115">The COMAdmin objects provide extended information in circumstances where the precise cause of the failure is difficult to determine without a detailed report, such as with multiple read and write operations.</span></span>

<span data-ttu-id="aec4a-116">Por exemplo, quando você usa métodos como [**populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) em um objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , você pode ler ou gravar dados para cada item na coleção.</span><span class="sxs-lookup"><span data-stu-id="aec4a-116">For example, when you use methods such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, you can be reading or writing data for every item in the collection.</span></span> <span data-ttu-id="aec4a-117">Podem ocorrer erros complicados e podem ser difíceis de diagnosticar com base em um único código de erro numérico.</span><span class="sxs-lookup"><span data-stu-id="aec4a-117">Complicated errors can occur, and they can be difficult to diagnose based on a single numeric error code.</span></span> <span data-ttu-id="aec4a-118">Portanto, a biblioteca COMAdmin faz informações de erro estendidas por meio de uma coleção especial.</span><span class="sxs-lookup"><span data-stu-id="aec4a-118">Therefore, the COMAdmin Library makes extended error information through a special collection.</span></span>

<span data-ttu-id="aec4a-119">Quando informações de erro estendidas estão disponíveis, elas são colocadas na coleção [**errorInfo**](errorinfo.md) que está relacionada à coleção original que tinha o erro.</span><span class="sxs-lookup"><span data-stu-id="aec4a-119">When extended error information is available, it is placed in the [**ErrorInfo**](errorinfo.md) collection that is related to the original collection that had the error.</span></span> <span data-ttu-id="aec4a-120">Para recuperar o relatório de erros, obtenha a coleção **errorInfo** relacionada à coleção original e examine os itens que ela contém.</span><span class="sxs-lookup"><span data-stu-id="aec4a-120">To retrieve the error report, get the **ErrorInfo** collection that is related to the original collection and examine the items it contains.</span></span> <span data-ttu-id="aec4a-121">Você pode recuperar a coleção **errorInfo** usando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) em [**COMAdminCatalogCollection**](comadmincatalogcollection.md), deixando o segundo parâmetro em branco, em que você normalmente especificaria a propriedade de chave de um item pai.</span><span class="sxs-lookup"><span data-stu-id="aec4a-121">You can retrieve the **ErrorInfo** collection by using [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on [**COMAdminCatalogCollection**](comadmincatalogcollection.md), leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

<span data-ttu-id="aec4a-122">Quando receber um erro, você deverá obter imediatamente e preencher a coleção [**errorInfo**](errorinfo.md) para a coleção que falhou, sem executar nenhuma outra operação nessa coleção.</span><span class="sxs-lookup"><span data-stu-id="aec4a-122">When you get an error, you must immediately get and populate the [**ErrorInfo**](errorinfo.md) collection for the collection that failed, without performing any other operations on that collection.</span></span> <span data-ttu-id="aec4a-123">Caso contrário, a coleção **errorInfo** será redefinida e não detalhará essa falha.</span><span class="sxs-lookup"><span data-stu-id="aec4a-123">Otherwise, the **ErrorInfo** collection is reset and does not detail that failure.</span></span>

<span data-ttu-id="aec4a-124">Os itens na coleção [**errorInfo**](errorinfo.md) expõem as propriedades especiais de relatório de erros MajorRef e MinorRef, que detalham a causa específica do erro.</span><span class="sxs-lookup"><span data-stu-id="aec4a-124">The items in the [**ErrorInfo**](errorinfo.md) collection expose the special error-reporting properties MajorRef and MinorRef, which detail the particular cause of the error.</span></span> <span data-ttu-id="aec4a-125">Para obter mais informações, consulte **errorInfo**.</span><span class="sxs-lookup"><span data-stu-id="aec4a-125">For more information, see **ErrorInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aec4a-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aec4a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec4a-127">Operações de administração COM+ em transações</span><span class="sxs-lookup"><span data-stu-id="aec4a-127">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="aec4a-128">Exemplo introdutório usando o catálogo de administração do COM+</span><span class="sxs-lookup"><span data-stu-id="aec4a-128">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="aec4a-129">Visão geral dos objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="aec4a-129">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="aec4a-130">Recuperando coleções no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="aec4a-130">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="aec4a-131">Definindo propriedades e salvando alterações no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="aec4a-131">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



