---
description: Fornece uma interface para o spooler de impressão. Os aplicativos podem usar essa API para enviar documentos XPS para uma impressora.
ms.assetid: df06ddcb-e573-461c-99a3-8f108fe2c143
title: API de impressão XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c53322a8ae6a03c3ac4bb71fc680f719999546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814437"
---
# <a name="xps-print-api"></a><span data-ttu-id="a8c23-104">API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="a8c23-104">XPS Print API</span></span>

<span data-ttu-id="a8c23-105">\[Não há suporte para a API de impressão XPS e elas podem ser alteradas ou não disponíveis no futuro.</span><span class="sxs-lookup"><span data-stu-id="a8c23-105">\[The XPS Print API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="a8c23-106">Em vez disso, os aplicativos cliente devem usar a [API de pacote de documentos de impressão](./tailored-app-printing-api.md) .\]</span><span class="sxs-lookup"><span data-stu-id="a8c23-106">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="a8c23-107">Fornece uma interface para o spooler de impressão.</span><span class="sxs-lookup"><span data-stu-id="a8c23-107">Provides an interface to the print spooler.</span></span> <span data-ttu-id="a8c23-108">Os aplicativos podem usar essa API para enviar documentos XPS para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="a8c23-108">Applications can use this API to send XPS documents to a printer.</span></span>

<span data-ttu-id="a8c23-109">Esta seção contém informações sobre os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8c23-109">This section contains information about the following topics.</span></span>

<dl>

[<span data-ttu-id="a8c23-110">Sobre a API de impressão do XPS</span><span class="sxs-lookup"><span data-stu-id="a8c23-110">About the XPS Print API</span></span>](about-xps-print-api.md)  
[<span data-ttu-id="a8c23-111">Usando a API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="a8c23-111">Using the XPS Print API</span></span>](using-the-xps-print-api.md)  
[<span data-ttu-id="a8c23-112">Referência da API de impressão do XPS</span><span class="sxs-lookup"><span data-stu-id="a8c23-112">XPS Print API Reference</span></span>](xpsprint-interfaces.md)  
</dl>

<span data-ttu-id="a8c23-113">Os aplicativos nativos do Windows que criam documentos XPS, como usando a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)), podem usar a API de impressão XPS para enviar conteúdo de documento XPS para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="a8c23-113">Native Windows applications that create XPS documents, such as by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)), can use the XPS Print API to send XPS document content to a printer.</span></span>

<span data-ttu-id="a8c23-114">O diagrama a seguir mostra a relação da API de impressão XPS com as outras APIs de impressão que um aplicativo nativo do Windows pode usar.</span><span class="sxs-lookup"><span data-stu-id="a8c23-114">The following diagram shows the relationship of the XPS Print API to the other Print APIs that a native Windows application can use.</span></span>

![um diagrama que mostra a relação da API de impressão XPS com as outras APIs de impressão que um aplicativo nativo do Windows pode usar](images/print-apis-xps.png)

## <a name="related-topics"></a><span data-ttu-id="a8c23-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8c23-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8c23-117">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="a8c23-117">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="a8c23-118">API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="a8c23-118">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="a8c23-119">API de tíquete de impressão</span><span class="sxs-lookup"><span data-stu-id="a8c23-119">Print Ticket API</span></span>](print-ticket-api.md)
</dt> <dt>

[<span data-ttu-id="a8c23-120">API de impressão GDI</span><span class="sxs-lookup"><span data-stu-id="a8c23-120">GDI Print API</span></span>](gdi-printing.md)
</dt> </dl>

 

 
