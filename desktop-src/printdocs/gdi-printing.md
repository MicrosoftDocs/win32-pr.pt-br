---
description: A API de impressão GDI fornece aplicativos com uma interface de impressão independente de dispositivo.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API de impressão GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169462"
---
# <a name="gdi-print-api"></a><span data-ttu-id="1d9bd-103">API de impressão GDI</span><span class="sxs-lookup"><span data-stu-id="1d9bd-103">GDI Print API</span></span>

<span data-ttu-id="1d9bd-104">A API de impressão GDI fornece aplicativos com uma interface de impressão independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d9bd-104">The GDI Print API provides applications with a device-independent printing interface.</span></span> <span data-ttu-id="1d9bd-105">Use essa interface se o aplicativo usar GDI para renderizar texto e elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="1d9bd-105">Use this interface if the application uses GDI to render text and graphics.</span></span>

<span data-ttu-id="1d9bd-106">Se você escrever aplicativos para o Windows Vista ou versões posteriores do Windows, considere usar a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) e a [API de impressão XPS](xps-printing.md) para usar as interfaces gráficas de alto desempenho com suporte nos drivers de impressão XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="1d9bd-106">If you write applications for Windows Vista or later versions of Windows, consider using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and the [XPS Print API](xps-printing.md) to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span>

<span data-ttu-id="1d9bd-107">Esta seção fornece informações sobre os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="1d9bd-107">This section provides information about the following topics.</span></span>



| <span data-ttu-id="1d9bd-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="1d9bd-108">Topic</span></span>                                                                                             | <span data-ttu-id="1d9bd-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d9bd-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d9bd-110">Sobre a API de impressão GDI</span><span class="sxs-lookup"><span data-stu-id="1d9bd-110">About the GDI Print API</span></span>](about-the-gdi-print-api.md)<br/>                                 | <span data-ttu-id="1d9bd-111">Uma visão geral da funcionalidade de impressão GDI.</span><span class="sxs-lookup"><span data-stu-id="1d9bd-111">An overview of the GDI printing functionality.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="1d9bd-112">Usando a API de impressão GDI</span><span class="sxs-lookup"><span data-stu-id="1d9bd-112">Using the GDI Print API</span></span>](using-the-printing-functions.md)<br/>                            | <span data-ttu-id="1d9bd-113">Informações sobre como usar a API de impressão GDI em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1d9bd-113">Information about using the GDI Print API in an application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1d9bd-114">Referência da API de impressão GDI</span><span class="sxs-lookup"><span data-stu-id="1d9bd-114">GDI Print API Reference</span></span>](gdi-print-api-reference.md)<br/>                                 | <span data-ttu-id="1d9bd-115">Descrições detalhadas das funções, estruturas e outros elementos da API de impressão do GDI.</span><span class="sxs-lookup"><span data-stu-id="1d9bd-115">Detailed descriptions of the functions, structures, and other elements of the GDI Print API.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1d9bd-116">Conversor de documento XPS da Microsoft (MXDC)</span><span class="sxs-lookup"><span data-stu-id="1d9bd-116">Microsoft XPS Document Converter (MXDC)</span></span>](microsoft-xps-document-converter--mxdc-.md)<br/> | <span data-ttu-id="1d9bd-117">O [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) é um componente que permite que os aplicativos usem a API de impressão GDI com impressoras que têm um driver de impressão XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="1d9bd-117">The [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) is a component that enables applications to use the GDI Print API with printers that have an XPSDrv Print Driver.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1d9bd-118">Gravador de documento XPS da Microsoft (MXDW)</span><span class="sxs-lookup"><span data-stu-id="1d9bd-118">Microsoft XPS Document Writer (MXDW)</span></span>](microsoft-xps-document-writer.md)<br/>              | <span data-ttu-id="1d9bd-119">O [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) fornece aplicativos com a funcionalidade "salvar como XPS" ou "exportar para XPS".</span><span class="sxs-lookup"><span data-stu-id="1d9bd-119">The [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) provides applications with "save as XPS" or "export to XPS" functionality.</span></span> <span data-ttu-id="1d9bd-120">Aplicativos que não criam conteúdo de documento XPS de forma nativa podem usar o MXDW para criar arquivos de documento XPS sem usar a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d9bd-120">Applications that do not natively create XPS document content can use the MXDW to create XPS document files without using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="1d9bd-121">No entanto, a API de documento XPS fornece um aplicativo com a capacidade de usar as interfaces gráficas de alto desempenho com suporte nos drivers de impressão XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="1d9bd-121">The XPS Document API, however, provides an application with the ability to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span><br/> |



 

<span data-ttu-id="1d9bd-122">O diagrama a seguir mostra a relação da API de impressão GDI com as outras APIs de impressão que um aplicativo pode usar.</span><span class="sxs-lookup"><span data-stu-id="1d9bd-122">The following diagram shows the relationship of the GDI Print API to the other print APIs that an application can use.</span></span>

![um diagrama que mostra a relação da API de impressão GDI com as outras APIs de impressão que um aplicativo Win32 pode usar](images/print-apis-gdi.png)

## <a name="related-topics"></a><span data-ttu-id="1d9bd-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d9bd-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d9bd-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="1d9bd-125">**AddJob**</span></span>](addjob.md)
</dt> <dt>

<span data-ttu-id="1d9bd-126">[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d9bd-126">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1d9bd-127">API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="1d9bd-127">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="1d9bd-128">API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="1d9bd-128">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="1d9bd-129">API de tíquete de impressão</span><span class="sxs-lookup"><span data-stu-id="1d9bd-129">Print Ticket API</span></span>](print-ticket-api.md)
</dt> </dl>

 

