---
title: Manipuladores de objetos
description: Manipuladores de objetos
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7294ddd48d2acaa010ad15c0e2497fd33c7f071
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822382"
---
# <a name="object-handlers"></a><span data-ttu-id="ca930-103">Manipuladores de objetos</span><span class="sxs-lookup"><span data-stu-id="ca930-103">Object Handlers</span></span>

<span data-ttu-id="ca930-104">Se um aplicativo de servidor OLE for um servidor local, o que significa que ele é executado em seu próprio espaço de processo, a comunicação entre o contêiner e o servidor deve ocorrer entre limites de processo.</span><span class="sxs-lookup"><span data-stu-id="ca930-104">If an OLE server application is a local server, meaning that it runs in its own process space, communication between container and server must occur across process boundaries.</span></span> <span data-ttu-id="ca930-105">Como esse processo é caro, o OLE depende de um objeto substituto carregado no espaço de processo do contêiner para agir em nome de um aplicativo de servidor local.</span><span class="sxs-lookup"><span data-stu-id="ca930-105">Because this process is expensive, OLE relies on a surrogate object loaded into the container's process space to act on behalf of a local server application.</span></span> <span data-ttu-id="ca930-106">Esse objeto alternativo, conhecido como *manipulador de objetos*, solicitações de contêiner de serviços que não exigem a atenção do aplicativo de servidor, como solicitações de desenho.</span><span class="sxs-lookup"><span data-stu-id="ca930-106">This surrogate object, known as an *object handler*, services container requests that do not require the attention of the server application, such as requests for drawing.</span></span> <span data-ttu-id="ca930-107">Quando um contêiner solicita algo que o manipulador de objetos não pode fornecer, o manipulador se comunica com o aplicativo de servidor usando o mecanismo de comunicação fora do processo do COM.</span><span class="sxs-lookup"><span data-stu-id="ca930-107">When a container requests something that the object handler cannot provide, the handler communicates with the server application using COM's out-of-process communication mechanism.</span></span>

<span data-ttu-id="ca930-108">Um manipulador de objeto é exclusivo de uma classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="ca930-108">An object handler is unique to an object class.</span></span> <span data-ttu-id="ca930-109">Quando você cria uma instância de um manipulador para uma classe, não pode usá-la para outra.</span><span class="sxs-lookup"><span data-stu-id="ca930-109">When you create an instance of a handler for one class, you cannot use it for another.</span></span> <span data-ttu-id="ca930-110">Quando usado para um documento composto, o manipulador de objetos implementa as estruturas de dados do lado do contêiner quando os objetos de uma determinada classe são acessados remotamente.</span><span class="sxs-lookup"><span data-stu-id="ca930-110">When used for a compound document, the object handler implements the container-side data structures when objects of a particular class are accessed remotely.</span></span>

<span data-ttu-id="ca930-111">O OLE fornece um manipulador de objeto padrão que os aplicativos de servidor local podem usar.</span><span class="sxs-lookup"><span data-stu-id="ca930-111">OLE provides a default object handler that local server applications can use.</span></span> <span data-ttu-id="ca930-112">Para aplicativos que exigem comportamentos especiais, os desenvolvedores podem implementar um manipulador personalizado que substitui o manipulador padrão ou o usa para fornecer determinados comportamentos padrão.</span><span class="sxs-lookup"><span data-stu-id="ca930-112">For applications that require special behaviors, developers can implement a custom handler that either replaces the default handler or uses it to provide certain default behaviors.</span></span>

<span data-ttu-id="ca930-113">Um manipulador de objeto é uma DLL que contém vários componentes de interação.</span><span class="sxs-lookup"><span data-stu-id="ca930-113">An object handler is a DLL containing several interacting components.</span></span> <span data-ttu-id="ca930-114">Esses componentes incluem partes de comunicação remota para gerenciar a comunicação entre o manipulador e seu aplicativo de servidor, um cache para armazenar os dados de um objeto, juntamente com informações sobre como esses dados devem ser formatados e exibidos e um objeto de controle que coordena as atividades dos outros componentes da DLL.</span><span class="sxs-lookup"><span data-stu-id="ca930-114">These components include remoting pieces to manage communication between the handler and its server application, a cache for storing an object's data, along with information on how that data should be formatted and displayed, and a controlling object that coordinates the activities of the DLL's other components.</span></span> <span data-ttu-id="ca930-115">Além disso, se um objeto for um link, a DLL também incluirá um componente de vinculação ou *objeto vinculado*, que controla o nome e o local da origem do link.</span><span class="sxs-lookup"><span data-stu-id="ca930-115">In addition, if an object is a link, the DLL also includes a linking component, or *linked object*, which keeps track of the name and location of the link source.</span></span>

<span data-ttu-id="ca930-116">O *cache* contém dados e informações de apresentação suficientes para que o manipulador exiba um objeto carregado, mas não em execução, em seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="ca930-116">The *cache* contains data and presentation information sufficient for the handler to display a loaded, but not running, object in its container.</span></span> <span data-ttu-id="ca930-117">O OLE fornece uma implementação do cache usado pelo manipulador de objetos padrão do OLE e o objeto de link.</span><span class="sxs-lookup"><span data-stu-id="ca930-117">OLE provides an implementation of the cache used by OLE's default object handler and the link object.</span></span> <span data-ttu-id="ca930-118">O cache armazena dados em formatos necessários para o manipulador de objeto atender às solicitações de desenho de contêiner.</span><span class="sxs-lookup"><span data-stu-id="ca930-118">The cache stores data in formats needed by the object handler to satisfy container draw requests.</span></span> <span data-ttu-id="ca930-119">Quando os dados de um objeto são alterados, o objeto envia uma notificação ao cache para que uma atualização possa ocorrer.</span><span class="sxs-lookup"><span data-stu-id="ca930-119">When an object's data changes, the object sends a notification to the cache so that an update can occur.</span></span> <span data-ttu-id="ca930-120">Para obter mais informações sobre o cache, consulte [Exibir cache](view-caching.md).</span><span class="sxs-lookup"><span data-stu-id="ca930-120">For more information on the cache, see [View Caching](view-caching.md).</span></span>

<span data-ttu-id="ca930-121">Para obter mais informações, consulte o tópico a seguir:</span><span class="sxs-lookup"><span data-stu-id="ca930-121">For more information, see the following topic:</span></span>

-   [<span data-ttu-id="ca930-122">O manipulador padrão e os manipuladores personalizados</span><span class="sxs-lookup"><span data-stu-id="ca930-122">The Default Handler and Custom Handlers</span></span>](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="ca930-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca930-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca930-124">Documentos compostos</span><span class="sxs-lookup"><span data-stu-id="ca930-124">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




