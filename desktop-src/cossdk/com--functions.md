---
description: A seguir estão as funções COM+.
ms.assetid: fdeb70ff-17ae-4ee4-a8b1-7fffb65ba2b2
title: Funções COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f7ce33e729a12c37ff1f2dcef516ab13d9b69a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105793973"
---
# <a name="com-functions"></a><span data-ttu-id="d0ec9-103">Funções COM+</span><span class="sxs-lookup"><span data-stu-id="d0ec9-103">COM+ Functions</span></span>

<span data-ttu-id="d0ec9-104">A seguir estão as funções COM+.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-104">The following are the COM+ functions.</span></span>



| <span data-ttu-id="d0ec9-105">Função</span><span class="sxs-lookup"><span data-stu-id="d0ec9-105">Function</span></span>                                                                 | <span data-ttu-id="d0ec9-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0ec9-106">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0ec9-107">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-107">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)                             | <span data-ttu-id="d0ec9-108">Cria uma atividade para realizar trabalho em lote síncrono ou assíncrono e que possa usar serviços COM+ sem a necessidade de criar um componente COM+.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-108">Creates an activity to do synchronous or asynchronous batch work that can use COM+ services without needing to create a COM+ component.</span></span> |
| [<span data-ttu-id="d0ec9-109">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-109">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)                     | <span data-ttu-id="d0ec9-110">Usado para inserir o código que pode usar os serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-110">Used to enter code that can then use COM+ services.</span></span>                                                                                     |
| [<span data-ttu-id="d0ec9-111">**CoGetDefaultContext**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-111">**CoGetDefaultContext**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetdefaultcontext)                       | <span data-ttu-id="d0ec9-112">Recupera uma referência para o contexto padrão do apartamento especificado.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-112">Retrieves a reference to the default context of the specified apartment.</span></span>                                                                |
| [<span data-ttu-id="d0ec9-113">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-113">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)                     | <span data-ttu-id="d0ec9-114">Usado para deixar o código que usa serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-114">Used to leave code that uses COM+ services.</span></span>                                                                                             |
| <span data-ttu-id="d0ec9-115">**ComPlusCompleteCbbSetup**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-115">**ComPlusCompleteCbbSetup**</span></span>               | <span data-ttu-id="d0ec9-116">Conclui uma migração de catálogo no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-116">Completes a catalog migration on the destination computer.</span></span>                                                                              |
| <span data-ttu-id="d0ec9-117">**GetComPlusPackageInstallStatus**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-117">**GetComPlusPackageInstallStatus**</span></span> | <span data-ttu-id="d0ec9-118">Indica se o CLR (Common Language Runtime) de 64 bits está instalado.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-118">Indicates whether the 64-bit Common Language Runtime (CLR) is installed.</span></span>                                                                |
| [<span data-ttu-id="d0ec9-119">**GetDispenserManager**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-119">**GetDispenserManager**</span></span>](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager)                       | <span data-ttu-id="d0ec9-120">Recupera a interface [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) do Gerenciador do dispensador.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-120">Retrieves the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>                                             |
| [<span data-ttu-id="d0ec9-121">**GetManagedExtensions**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-121">**GetManagedExtensions**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getmanagedextensions)                     | <span data-ttu-id="d0ec9-122">Determina se a versão instalada do COM+ dá suporte a recursos especiais fornecidos para gerenciar componentes atendidos (objetos gerenciados).</span><span class="sxs-lookup"><span data-stu-id="d0ec9-122">Determines whether the installed version of COM+ supports special features provided to manage serviced components (managed objects).</span></span>    |
| [<span data-ttu-id="d0ec9-123">**GetObjectContext**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-123">**GetObjectContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)                             | <span data-ttu-id="d0ec9-124">Recupera uma referência ao contexto associado ao objeto COM+ atual.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-124">Retrieves a reference to the context that is associated with the current COM+ object.</span></span>                                                   |
| [<span data-ttu-id="d0ec9-125">**MTSCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-125">**MTSCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-mtscreateactivity)                           | <span data-ttu-id="d0ec9-126">Cria uma atividade em um apartamento de thread único para fazer o trabalho em lote síncrono ou assíncrono.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-126">Creates an activity in a single-threaded apartment to do synchronous or asynchronous batch work.</span></span>                                        |
| [<span data-ttu-id="d0ec9-127">**RecycleSurrogate**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-127">**RecycleSurrogate**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)                             | <span data-ttu-id="d0ec9-128">Recicla o processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-128">Recycles the calling process.</span></span>                                                                                                           |
| [<span data-ttu-id="d0ec9-129">**SafeRef**</span><span class="sxs-lookup"><span data-stu-id="d0ec9-129">**SafeRef**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef)                                               | <span data-ttu-id="d0ec9-130">Substituí Não use.</span><span class="sxs-lookup"><span data-stu-id="d0ec9-130">Obsolete; do not use.</span></span>                                                                                                                   |



 

 

 



