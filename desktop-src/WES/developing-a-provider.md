---
title: Desenvolvendo um provedor
description: Para gravar os eventos que você define em seu manifesto, use as funções incluídas na API de rastreamento de eventos (ETW). Para obter detalhes sobre como escrever um provedor, consulte fornecendo eventos.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084826"
---
# <a name="developing-a-provider"></a><span data-ttu-id="1d56f-104">Desenvolvendo um provedor</span><span class="sxs-lookup"><span data-stu-id="1d56f-104">Developing a Provider</span></span>

<span data-ttu-id="1d56f-105">Para gravar os eventos que você define em seu manifesto, use as funções incluídas na API de [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="1d56f-105">To write the events that you define in your manifest, you use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span> <span data-ttu-id="1d56f-106">Para obter detalhes sobre como escrever um provedor, consulte [fornecendo eventos](/windows/desktop/ETW/providing-events).</span><span class="sxs-lookup"><span data-stu-id="1d56f-106">For details on writing a provider, see [Providing Events](/windows/desktop/ETW/providing-events).</span></span>

<span data-ttu-id="1d56f-107">Depois de gravar o provedor, use a ferramenta WevtUtil.exe para registrar o provedor e o esquema.</span><span class="sxs-lookup"><span data-stu-id="1d56f-107">After writing the provider, use the WevtUtil.exe tool to register the provider and schema.</span></span> <span data-ttu-id="1d56f-108">Para obter detalhes sobre como usar WevtUtil, consulte [ferramentas de log de eventos do Windows](windows-event-log-tools.md).</span><span class="sxs-lookup"><span data-stu-id="1d56f-108">For details on using WevtUtil, see [Windows Event Log Tools](windows-event-log-tools.md).</span></span> <span data-ttu-id="1d56f-109">O seguinte mostra como usar WevtUtil para registrar um provedor e remover o registro.</span><span class="sxs-lookup"><span data-stu-id="1d56f-109">The following shows how to use WevtUtil to register a provider and to remove the registration.</span></span>


```cmd
wevtutil im provider.man

wevtutil um provider.man
```