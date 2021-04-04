---
title: Gerenciador de threads
description: O Gerenciador de threads é o componente base do Gerenciador do TSF.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- TSF (estrutura de serviços de texto), Gerenciador de thread
- TSF (estrutura de serviços de texto), Gerenciador de threads
- serviços de texto, Gerenciador de threads
- Aplicativos habilitados para TSF, Gerenciador de threads
- Gerenciador de threads
- Gerenciador de TSF
- notificações de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007795"
---
# <a name="thread-manager"></a><span data-ttu-id="5995b-110">Gerenciador de threads</span><span class="sxs-lookup"><span data-stu-id="5995b-110">Thread Manager</span></span>

<span data-ttu-id="5995b-111">O Gerenciador de threads é o componente base do Gerenciador do TSF.</span><span class="sxs-lookup"><span data-stu-id="5995b-111">The thread manager is the base component of the TSF manager.</span></span> <span data-ttu-id="5995b-112">O Gerenciador de threads executa tarefas comuns relacionadas aos aplicativos e aos serviços de texto (clientes).</span><span class="sxs-lookup"><span data-stu-id="5995b-112">The thread manager performs common tasks related to both applications and text services (clients).</span></span> <span data-ttu-id="5995b-113">Essas tarefas incluem, entre outros, a ativação e a desativação de serviços de texto do TSF, a criação de gerenciadores de documentos e a manutenção da relação apropriada entre os documentos e o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="5995b-113">These tasks include, but are not limited to, the activation and deactivation of TSF text services, the creation of document managers, and maintenance of the proper relationship between documents and the input focus.</span></span> <span data-ttu-id="5995b-114">O Gerenciador de threads é definido pela interface [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) .</span><span class="sxs-lookup"><span data-stu-id="5995b-114">The thread manager is defined by the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface.</span></span>

<span data-ttu-id="5995b-115">A maioria das interfaces e dos objetos fornecidos pelo Gerenciador de TSF pode ser obtida usando os métodos fornecidos pela interface do Gerenciador de threads.</span><span class="sxs-lookup"><span data-stu-id="5995b-115">The majority of the interfaces and objects provided by the TSF manager can be obtained using the methods that the thread manager interface provides.</span></span>

## <a name="applications"></a><span data-ttu-id="5995b-116">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="5995b-116">Applications</span></span>

<span data-ttu-id="5995b-117">Um aplicativo cria um objeto do Gerenciador de threads chamando [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com CLSID \_ TFThreadMgr.</span><span class="sxs-lookup"><span data-stu-id="5995b-117">An application creates a thread manager object by calling [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_TFThreadMgr.</span></span>

## <a name="text-services"></a><span data-ttu-id="5995b-118">Serviços de texto</span><span class="sxs-lookup"><span data-stu-id="5995b-118">Text Services</span></span>

<span data-ttu-id="5995b-119">Um serviço de texto Obtém um objeto do Gerenciador de threads no método Text Service [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) .</span><span class="sxs-lookup"><span data-stu-id="5995b-119">A text service obtains a thread manager object in the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span>

## <a name="event-notifications"></a><span data-ttu-id="5995b-120">Notificações de eventos</span><span class="sxs-lookup"><span data-stu-id="5995b-120">Event Notifications</span></span>

<span data-ttu-id="5995b-121">O Gerenciador de threads também fornece notificação de eventos aos clientes.</span><span class="sxs-lookup"><span data-stu-id="5995b-121">The thread manager also provides event notification to clients.</span></span> <span data-ttu-id="5995b-122">No TSF, as notificações de eventos são fornecidas por meio de um coletor de eventos, que é um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="5995b-122">In TSF, event notifications are provided by means of an event sink, which is a COM object.</span></span> <span data-ttu-id="5995b-123">Para receber notificações do Gerenciador de threads, um cliente implementa um objeto [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) e instala o coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="5995b-123">To receive notifications from the thread manager, a client implements an [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) object and installs the event sink.</span></span> <span data-ttu-id="5995b-124">O coletor de eventos é instalado consultando o Gerenciador de thread para \_ ITfSource de IID e chamando [ITfSource:: ADVISESINK](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) com IID \_ ITfThreadMgrEventSink.</span><span class="sxs-lookup"><span data-stu-id="5995b-124">The event sink is installed by querying the thread manager for IID\_ITfSource and calling [ITfSource::AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfThreadMgrEventSink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5995b-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5995b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5995b-126">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="5995b-126">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="5995b-127">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="5995b-127">CoCreateInstance</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="5995b-128">ITfTextInputProcessor:: ativar</span><span class="sxs-lookup"><span data-stu-id="5995b-128">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="5995b-129">ITfThreadMgrEventSink</span><span class="sxs-lookup"><span data-stu-id="5995b-129">ITfThreadMgrEventSink</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[<span data-ttu-id="5995b-130">ITfSource:: AdviseSink</span><span class="sxs-lookup"><span data-stu-id="5995b-130">ITfSource::AdviseSink</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 