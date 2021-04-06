---
title: contêineres e servidores
description: contêineres e servidores
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51b2cd46057c9216a1f9e29b93e1381a4d3062a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823012"
---
# <a name="containers-and-servers"></a><span data-ttu-id="46ce3-103">contêineres e servidores</span><span class="sxs-lookup"><span data-stu-id="46ce3-103">Containers and Servers</span></span>

<span data-ttu-id="46ce3-104">Os aplicativos de documentos compostos são de dois tipos básicos: aplicativos de contêiner e aplicativos de servidor.</span><span class="sxs-lookup"><span data-stu-id="46ce3-104">Compound document applications are of two basic types: container applications and server applications.</span></span> <span data-ttu-id="46ce3-105">Os aplicativos de contêiner OLE fornecem aos usuários a capacidade de criar, editar, salvar e recuperar documentos compostos.</span><span class="sxs-lookup"><span data-stu-id="46ce3-105">OLE container applications provide users with the ability to create, edit, save, and retrieve compound documents.</span></span> <span data-ttu-id="46ce3-106">Os aplicativos de servidor OLE fornecem aos usuários meios para criar documentos e outras representações de dados que podem ser contidas como links ou incorporações em aplicativos de contêiner.</span><span class="sxs-lookup"><span data-stu-id="46ce3-106">OLE server applications provide users with the means to create documents and other data representations that can be contained as either links or embeddings in container applications.</span></span> <span data-ttu-id="46ce3-107">Um aplicativo OLE pode ser um aplicativo de contêiner, um aplicativo de servidor ou ambos.</span><span class="sxs-lookup"><span data-stu-id="46ce3-107">An OLE application can be a container application, a server application, or both.</span></span>

<span data-ttu-id="46ce3-108">Os aplicativos de servidor OLE também diferem se eles são implementados como *servidores em processo* ou *servidores locais*.</span><span class="sxs-lookup"><span data-stu-id="46ce3-108">OLE server applications also differ in whether they are implemented as *in-process servers* or *local servers*.</span></span> <span data-ttu-id="46ce3-109">Um servidor em processo é uma DLL (biblioteca de vínculo dinâmico) que é executada no espaço de processo do aplicativo de contêiner.</span><span class="sxs-lookup"><span data-stu-id="46ce3-109">An in-process server is a dynamic link library (DLL) that runs in the container application's process space.</span></span> <span data-ttu-id="46ce3-110">Você pode executar um servidor em processo somente de dentro do aplicativo de contêiner.</span><span class="sxs-lookup"><span data-stu-id="46ce3-110">You can run an in-process server only from within the container application.</span></span>

> [!Note]  
> <span data-ttu-id="46ce3-111">Versões futuras do OLE habilitarão a vinculação e a inserção nos limites do computador, de modo que um aplicativo de contêiner em um computador poderá usar um objeto de documento composto fornecido por um *servidor remoto* em execução em outro computador.</span><span class="sxs-lookup"><span data-stu-id="46ce3-111">Future releases of OLE will enable linking and embedding across computer boundaries, so that a container application on one computer will be able to use a compound document object provided by a *remote server* running on another computer.</span></span> <span data-ttu-id="46ce3-112">Do ponto de vista de um aplicativo de contêiner, qualquer aplicativo de servidor OLE executado em seu próprio espaço de processo, seja no mesmo computador ou em um computador remoto, é um *servidor processÂ*.</span><span class="sxs-lookup"><span data-stu-id="46ce3-112">From a container application's point of view, any OLE server application that runs in its own process space, whether on the same computer or a remote computer, is an *out-of-processÂ server*.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="46ce3-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46ce3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46ce3-114">Documentos compostos</span><span class="sxs-lookup"><span data-stu-id="46ce3-114">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="46ce3-115">Servidores em processo</span><span class="sxs-lookup"><span data-stu-id="46ce3-115">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




