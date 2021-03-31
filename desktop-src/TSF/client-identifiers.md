---
title: Identificadores de cliente
description: Identificadores de cliente
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- TSF (estrutura de serviços de texto), identificadores de cliente
- TSF (estrutura de serviços de texto), identificadores de cliente
- serviços de texto, identificadores de cliente
- Aplicativos habilitados para TSF, identificadores de cliente
- identificadores de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de15b208d2fbc6c6ea5c2a1114eb5cb23ff12ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916089"
---
# <a name="client-identifiers"></a><span data-ttu-id="207b5-108">Identificadores de cliente</span><span class="sxs-lookup"><span data-stu-id="207b5-108">Client Identifiers</span></span>

## <a name="applications"></a><span data-ttu-id="207b5-109">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="207b5-109">Applications</span></span>

<span data-ttu-id="207b5-110">Um aplicativo obtém seu identificador de cliente chamando [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span><span class="sxs-lookup"><span data-stu-id="207b5-110">An application obtains its client identifier by calling [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span>

## <a name="text-services"></a><span data-ttu-id="207b5-111">Serviços de texto</span><span class="sxs-lookup"><span data-stu-id="207b5-111">Text Services</span></span>

<span data-ttu-id="207b5-112">Um serviço de texto obtém seu identificador de cliente quando o método Text Service [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) é chamado.</span><span class="sxs-lookup"><span data-stu-id="207b5-112">A text service obtains its client identifier when the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method is called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="207b5-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="207b5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="207b5-114">ITfThreadMgr:: ativar</span><span class="sxs-lookup"><span data-stu-id="207b5-114">ITfThreadMgr::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[<span data-ttu-id="207b5-115">ITfTextInputProcessor:: ativar</span><span class="sxs-lookup"><span data-stu-id="207b5-115">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




