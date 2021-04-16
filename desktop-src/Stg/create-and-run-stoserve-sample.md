---
title: Criar e executar exemplo de StoServe
description: O exemplo de cliente e outros exemplos relacionados devem ser compilados antes que você possa executar o cliente.
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754098"
---
# <a name="create-and-run-stoserve-sample"></a><span data-ttu-id="3782a-103">Criar e executar exemplo de StoServe</span><span class="sxs-lookup"><span data-stu-id="3782a-103">Create and Run StoServe Sample</span></span>

<span data-ttu-id="3782a-104">O exemplo de cliente e outros exemplos relacionados devem ser compilados antes que você possa executar o cliente.</span><span class="sxs-lookup"><span data-stu-id="3782a-104">The client sample and other related samples must be compiled before you can run the client.</span></span> <span data-ttu-id="3782a-105">Para obter mais detalhes sobre como criar os exemplos, consulte [como criar exemplos](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="3782a-105">For more details on building the samples, see [How to Build Samples](how-to-build-samples.md).</span></span> <span data-ttu-id="3782a-106">Se você já tiver criado os exemplos apropriados, STOCLIEN.EXE será o executável do cliente a ser executado para o exemplo **StoServe** .</span><span class="sxs-lookup"><span data-stu-id="3782a-106">If you have already built the appropriate samples, STOCLIEN.EXE is the client executable to run for the **StoServe** sample.</span></span>

## <a name="code-tour"></a><span data-ttu-id="3782a-107">Tour pelo código</span><span class="sxs-lookup"><span data-stu-id="3782a-107">Code Tour</span></span>

<span data-ttu-id="3782a-108">A tabela a seguir lista os arquivos pertinentes ao exemplo de **StoServe** .</span><span class="sxs-lookup"><span data-stu-id="3782a-108">The following table lists the files pertinent to the **StoServe** sample.</span></span>



| <span data-ttu-id="3782a-109">Arquivos</span><span class="sxs-lookup"><span data-stu-id="3782a-109">Files</span></span>        | <span data-ttu-id="3782a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3782a-110">Description</span></span>                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3782a-111">STOSERVE.TXT</span><span class="sxs-lookup"><span data-stu-id="3782a-111">STOSERVE.TXT</span></span> | <span data-ttu-id="3782a-112">Descrição de exemplo breve</span><span class="sxs-lookup"><span data-stu-id="3782a-112">Short sample description</span></span>                                                                                                  |
| <span data-ttu-id="3782a-113">MAKEFILE</span><span class="sxs-lookup"><span data-stu-id="3782a-113">MAKEFILE</span></span>     | <span data-ttu-id="3782a-114">O makefile genérico para criar o STOSERVE.DLL exemplo de código desta lição.</span><span class="sxs-lookup"><span data-stu-id="3782a-114">The generic makefile for building the STOSERVE.DLL code sample of this lesson.</span></span>                                            |
| <span data-ttu-id="3782a-115">STOSERVE. T</span><span class="sxs-lookup"><span data-stu-id="3782a-115">STOSERVE.H</span></span>   | <span data-ttu-id="3782a-116">O arquivo de inclusão para declarar como importado ou definir como exportado as funções de serviço no STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="3782a-116">The include file for declaring as imported or defining as exported the service functions in STOSERVE.DLL.</span></span>                 |
| <span data-ttu-id="3782a-117">STOSERVE. CPP</span><span class="sxs-lookup"><span data-stu-id="3782a-117">STOSERVE.CPP</span></span> | <span data-ttu-id="3782a-118">O arquivo de implementação principal para STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="3782a-118">The main implementation file for STOSERVE.DLL.</span></span> <span data-ttu-id="3782a-119">Tem DllMain e as funções de servidor COM (por exemplo, DllGetClassObject).</span><span class="sxs-lookup"><span data-stu-id="3782a-119">Has DllMain and the COM server functions (for example, DllGetClassObject).</span></span> |
| <span data-ttu-id="3782a-120">STOSERVE. PARTICULAR</span><span class="sxs-lookup"><span data-stu-id="3782a-120">STOSERVE.DEF</span></span> | <span data-ttu-id="3782a-121">O arquivo de definição de módulo.</span><span class="sxs-lookup"><span data-stu-id="3782a-121">The module definition file.</span></span> <span data-ttu-id="3782a-122">Exporta funções de invólucro de servidor.</span><span class="sxs-lookup"><span data-stu-id="3782a-122">Exports server housing functions.</span></span>                                                             |
| <span data-ttu-id="3782a-123">STOSERVE. RC</span><span class="sxs-lookup"><span data-stu-id="3782a-123">STOSERVE.RC</span></span>  | <span data-ttu-id="3782a-124">O arquivo de definição de recurso de DLL para o executável.</span><span class="sxs-lookup"><span data-stu-id="3782a-124">The DLL resource definition file for the executable.</span></span>                                                                      |
| <span data-ttu-id="3782a-125">STOSERVE. ICO</span><span class="sxs-lookup"><span data-stu-id="3782a-125">STOSERVE.ICO</span></span> | <span data-ttu-id="3782a-126">O recurso de ícone para o executável.</span><span class="sxs-lookup"><span data-stu-id="3782a-126">The icon resource for the executable.</span></span>                                                                                     |
| <span data-ttu-id="3782a-127">Servidor. T</span><span class="sxs-lookup"><span data-stu-id="3782a-127">SERVER.H</span></span>     | <span data-ttu-id="3782a-128">O arquivo de inclusão do objeto C++ de controle de servidor.</span><span class="sxs-lookup"><span data-stu-id="3782a-128">The include file for the server control C++ object.</span></span>                                                                       |
| <span data-ttu-id="3782a-129">Servidor. CPP</span><span class="sxs-lookup"><span data-stu-id="3782a-129">SERVER.CPP</span></span>   | <span data-ttu-id="3782a-130">O arquivo de implementação do objeto C++ de controle de servidor.</span><span class="sxs-lookup"><span data-stu-id="3782a-130">The implementation file for the server control C++ object.</span></span>                                                                |
| <span data-ttu-id="3782a-131">Padrões. T</span><span class="sxs-lookup"><span data-stu-id="3782a-131">FACTORY.H</span></span>    | <span data-ttu-id="3782a-132">O arquivo de inclusão para objetos COM da fábrica de classes do servidor.</span><span class="sxs-lookup"><span data-stu-id="3782a-132">The include file for the server's class factory COM objects.</span></span>                                                              |
| <span data-ttu-id="3782a-133">Padrões. CPP</span><span class="sxs-lookup"><span data-stu-id="3782a-133">FACTORY.CPP</span></span>  | <span data-ttu-id="3782a-134">O arquivo de implementação para as fábricas de classe do servidor.</span><span class="sxs-lookup"><span data-stu-id="3782a-134">The implementation file for the server's class factories.</span></span>                                                                 |
| <span data-ttu-id="3782a-135">Connect. T</span><span class="sxs-lookup"><span data-stu-id="3782a-135">CONNECT.H</span></span>    | <span data-ttu-id="3782a-136">O arquivo de inclusão para as classes enumerador de ponto de conexão, ponto de conexão e enumerador de conexão.</span><span class="sxs-lookup"><span data-stu-id="3782a-136">The include file for the connection point enumerator, connection point, and connection enumerator classes.</span></span>                |
| <span data-ttu-id="3782a-137">Connect. CPP</span><span class="sxs-lookup"><span data-stu-id="3782a-137">CONNECT.CPP</span></span>  | <span data-ttu-id="3782a-138">O arquivo de implementação para os objetos enumerador de ponto de conexão, ponto de conexão e enumerador de conexão.</span><span class="sxs-lookup"><span data-stu-id="3782a-138">The implementation file for the connection point enumerator, connection point, and connection enumerator objects.</span></span>         |
| <span data-ttu-id="3782a-139">Documentos. T</span><span class="sxs-lookup"><span data-stu-id="3782a-139">PAPER.H</span></span>      | <span data-ttu-id="3782a-140">O arquivo de inclusão para a classe de objeto COM do copaper.</span><span class="sxs-lookup"><span data-stu-id="3782a-140">The include file for the COPaper COM object class.</span></span>                                                                        |
| <span data-ttu-id="3782a-141">Documentos. CPP</span><span class="sxs-lookup"><span data-stu-id="3782a-141">PAPER.CPP</span></span>    | <span data-ttu-id="3782a-142">O arquivo de implementação para a classe de objeto COM de copapel e os pontos de conexão.</span><span class="sxs-lookup"><span data-stu-id="3782a-142">The implementation file for the COPaper COM object class and the connection points.</span></span>                                       |
| <span data-ttu-id="3782a-143">STOSERVE. DSP</span><span class="sxs-lookup"><span data-stu-id="3782a-143">STOSERVE.DSP</span></span> | <span data-ttu-id="3782a-144">Microsoft Visual Studio arquivo de projeto.</span><span class="sxs-lookup"><span data-stu-id="3782a-144">Microsoft Visual Studio Project file.</span></span>                                                                                     |



 

<span data-ttu-id="3782a-145">Os principais tópicos abordados neste Tour de código são:</span><span class="sxs-lookup"><span data-stu-id="3782a-145">The major topics covered in this code tour are:</span></span>

-   <span data-ttu-id="3782a-146">Os métodos de interface [**IPaper**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="3782a-146">The [**IPaper**](ipaper-methods.md) interface methods.</span></span>
-   <span data-ttu-id="3782a-147">Uso do copaper da interface [**IPaperSink**](ipapersink-methods.md) para notificações do cliente.</span><span class="sxs-lookup"><span data-stu-id="3782a-147">COPaper's use of the [**IPaperSink**](ipapersink-methods.md) interface for client notifications.</span></span>
-   <span data-ttu-id="3782a-148">[**Estruturas**](structures---stoserve.md) em StoServe.</span><span class="sxs-lookup"><span data-stu-id="3782a-148">[**Structures**](structures---stoserve.md) in StoServe.</span></span>
-   <span data-ttu-id="3782a-149">[Considerações sobre Unicode](unicode-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="3782a-149">[Unicode considerations](unicode-considerations.md).</span></span>

 

 




