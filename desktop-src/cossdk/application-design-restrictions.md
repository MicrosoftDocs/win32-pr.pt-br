---
description: Alguns aplicativos são criados de forma a impedir que várias instâncias do aplicativo sejam instaladas em um computador.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Restrições de design de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768811"
---
# <a name="application-design-restrictions"></a><span data-ttu-id="b34ed-103">Restrições de design de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b34ed-103">Application Design Restrictions</span></span>

<span data-ttu-id="b34ed-104">Alguns aplicativos são criados de forma a impedir que várias instâncias do aplicativo sejam instaladas em um computador.</span><span class="sxs-lookup"><span data-stu-id="b34ed-104">Some applications are designed in a way that prevents multiple instances of the application from being installed on a computer.</span></span> <span data-ttu-id="b34ed-105">Com essa limitação, um aplicativo não pode usar o recurso de partições.</span><span class="sxs-lookup"><span data-stu-id="b34ed-105">With such a limitation, an application cannot make use of the partitions feature.</span></span> <span data-ttu-id="b34ed-106">Os seguintes recursos de design de aplicativo podem precisar ser modificados antes que as partições possam ser usadas para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b34ed-106">The following application design features might need to be modified before partitions can be used for that application.</span></span>

## <a name="tables-and-arrays"></a><span data-ttu-id="b34ed-107">Tabelas e matrizes</span><span class="sxs-lookup"><span data-stu-id="b34ed-107">Tables and Arrays</span></span>

<span data-ttu-id="b34ed-108">Alguns aplicativos criam tabelas de banco de dados, tabelas na memória ou matrizes que usam um CLSID como uma chave de registro exclusiva.</span><span class="sxs-lookup"><span data-stu-id="b34ed-108">Some applications create database tables, in-memory tables, or arrays that use a CLSID as a unique registry key.</span></span> <span data-ttu-id="b34ed-109">Em um computador sem partições, essa chave do registro normalmente é Computer/CLSID (um CLSID por computador).</span><span class="sxs-lookup"><span data-stu-id="b34ed-109">On a computer without partitions, this registry key is typically computer/CLSID (one CLSID per computer).</span></span>

<span data-ttu-id="b34ed-110">Por outro lado, em um computador com partições, essa chave do registro é ID de computador/partição/ID do aplicativo/CLSID (várias instâncias de um CLSID por computador).</span><span class="sxs-lookup"><span data-stu-id="b34ed-110">Conversely, on a computer with partitions, this registry key is computer/partition ID/application ID/CLSID (multiple instances of a CLSID per computer).</span></span> <span data-ttu-id="b34ed-111">Como o recurso de partições permite que várias instâncias de um CLSID existam em um computador, os aplicativos que contêm elementos de design que exigem um CLSID exclusivo por computador podem ser afetados negativamente.</span><span class="sxs-lookup"><span data-stu-id="b34ed-111">Because the partitions feature allows multiple instances of a CLSID to exist on a computer, applications that contain design elements that require a unique CLSID per computer might be adversely affected.</span></span>

## <a name="global-resources"></a><span data-ttu-id="b34ed-112">Recursos Globais</span><span class="sxs-lookup"><span data-stu-id="b34ed-112">Global Resources</span></span>

<span data-ttu-id="b34ed-113">Alguns aplicativos usam recursos globais, como memória compartilhada, arquivos de dados e entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="b34ed-113">Some applications use global resources such as shared memory, data files, and registry entries.</span></span> <span data-ttu-id="b34ed-114">Isso pode causar problemas se várias instâncias desse aplicativo estiverem sendo executadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="b34ed-114">This could cause problems if multiple instances of such an application are executing simultaneously.</span></span>

<span data-ttu-id="b34ed-115">Por exemplo, se um componente usa memória compartilhada para interagir com outros componentes, o componente precisará ser modificado para que cada instância do componente aloque sua própria memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="b34ed-115">For example, if a component uses shared memory for interacting with other components, the component will need to be modified so that each instance of the component allocates its own shared memory.</span></span>

## <a name="type-libraries"></a><span data-ttu-id="b34ed-116">Bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="b34ed-116">Type Libraries</span></span>

<span data-ttu-id="b34ed-117">As bibliotecas de tipos fornecem informações sobre interfaces e métodos de um componente.</span><span class="sxs-lookup"><span data-stu-id="b34ed-117">Type libraries provide information about a component's interfaces and methods.</span></span> <span data-ttu-id="b34ed-118">Essas informações são usadas para várias finalidades, incluindo as seguintes:</span><span class="sxs-lookup"><span data-stu-id="b34ed-118">This information is used for several purposes, including the following:</span></span>

-   <span data-ttu-id="b34ed-119">Marshaling de dados entre componentes quando são feitas chamadas de função</span><span class="sxs-lookup"><span data-stu-id="b34ed-119">Marshaling data between components when function calls are made</span></span>
-   <span data-ttu-id="b34ed-120">Ajudando os componentes em fila COM+ e os serviços de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="b34ed-120">Helping the COM+ Queued Components and COM+ Events services</span></span>
-   <span data-ttu-id="b34ed-121">Fornecendo as informações corretas em um editor de Visual Basic da Microsoft</span><span class="sxs-lookup"><span data-stu-id="b34ed-121">Providing the correct information within a Microsoft Visual Basic editor</span></span>

<span data-ttu-id="b34ed-122">As referências a uma biblioteca de tipos são instaladas no registro de um computador.</span><span class="sxs-lookup"><span data-stu-id="b34ed-122">References to a type library are installed in the registry of a computer.</span></span> <span data-ttu-id="b34ed-123">Ao desenvolver aplicativos que serão invocados em partições, é importante que a versão mais recente de uma biblioteca de tipos seja instalada no registro.</span><span class="sxs-lookup"><span data-stu-id="b34ed-123">When developing applications that will be invoked from within partitions, it is important that the latest version of a type library is installed in the registry.</span></span> <span data-ttu-id="b34ed-124">Isso garante que o editor de Visual Basic que está sendo usado receberá informações precisas sobre os métodos disponíveis para esse componente.</span><span class="sxs-lookup"><span data-stu-id="b34ed-124">This ensures that the Visual Basic editor being used will get accurate information about the methods available for that component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b34ed-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b34ed-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b34ed-126">Componentes e partições em fila COM+</span><span class="sxs-lookup"><span data-stu-id="b34ed-126">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="b34ed-127">Implementação de partição</span><span class="sxs-lookup"><span data-stu-id="b34ed-127">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="b34ed-128">Registrando e ativando componentes em partições</span><span class="sxs-lookup"><span data-stu-id="b34ed-128">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="b34ed-129">O que são partições COM+?</span><span class="sxs-lookup"><span data-stu-id="b34ed-129">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



