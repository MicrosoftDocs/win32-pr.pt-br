---
description: A API de tíquete de impressão fornece permite que os aplicativos gerenciem e convertam os tíquetes de impressão.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: API de tíquete de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104011966"
---
# <a name="print-ticket-api"></a><span data-ttu-id="be4e6-103">API de tíquete de impressão</span><span class="sxs-lookup"><span data-stu-id="be4e6-103">Print Ticket API</span></span>

<span data-ttu-id="be4e6-104">A API de tíquete de impressão fornece permite que os aplicativos gerenciem e convertam os tíquetes de impressão.</span><span class="sxs-lookup"><span data-stu-id="be4e6-104">The Print Ticket API provides enables applications to manage and convert print tickets.</span></span>

<span data-ttu-id="be4e6-105">Um tíquete de impressão é um componente de documento XPS que contém as configurações de impressora preferenciais para uma página em um documento, ou para um documento inteiro ou para um trabalho de impressão que contenha um ou mais documentos.</span><span class="sxs-lookup"><span data-stu-id="be4e6-105">A print ticket is an XPS document component that contains the preferred printer settings for a page in a document, or for an entire document, or for a print job that contains one or more documents.</span></span> <span data-ttu-id="be4e6-106">Observe que os tíquetes de impressão só são encontrados em documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="be4e6-106">Note that print tickets are only found in XPS documents.</span></span>

<span data-ttu-id="be4e6-107">Antes que a impressora possa usar o tíquete de impressão, o tíquete de impressão deve ser validado em relação às características da impressora, que são definidas nos recursos de impressão da impressora.</span><span class="sxs-lookup"><span data-stu-id="be4e6-107">Before the printer can use the print ticket, the print ticket must be validated against the printer's characteristics, which are defined in the printer's Print Capabilities.</span></span> <span data-ttu-id="be4e6-108">O aplicativo executa essa validação chamando a API de tíquete de impressão.</span><span class="sxs-lookup"><span data-stu-id="be4e6-108">The application performs that validation by calling the Print Ticket API.</span></span>

<span data-ttu-id="be4e6-109">Os PrintTicket e PrintCapabilities são descritos usando elementos do esquema de impressão, que é definido pela [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="be4e6-109">The PrintTicket and PrintCapabilities are described by using elements of the Print Schema, which is defined by the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="be4e6-110">Este tópico contém informações sobre os seguintes elementos de API:</span><span class="sxs-lookup"><span data-stu-id="be4e6-110">This topic contains information about the following API elements:</span></span>

-   [<span data-ttu-id="be4e6-111">Funções da API de tíquete de impressão</span><span class="sxs-lookup"><span data-stu-id="be4e6-111">Print Ticket API Functions</span></span>](print-ticket-api-functions.md)
-   [<span data-ttu-id="be4e6-112">Enumerações de API de tíquete de impressão</span><span class="sxs-lookup"><span data-stu-id="be4e6-112">Print Ticket API Enumerations</span></span>](print-ticket-api-enumerations.md)

<span data-ttu-id="be4e6-113">O diagrama a seguir mostra a relação da API de tíquete de impressão com as outras APIs de impressão que um aplicativo nativo do Windows pode usar.</span><span class="sxs-lookup"><span data-stu-id="be4e6-113">The following diagram shows the relationship of the Print Ticket API to the other Print APIs that a native Windows application can use.</span></span>

![um diagrama que mostra a relação da API de tíquete de impressão com outras APIs de impressão que um aplicativo nativo do Windows pode usar](images/print-apis-pt.png)

## <a name="related-topics"></a><span data-ttu-id="be4e6-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="be4e6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be4e6-116">API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="be4e6-116">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="be4e6-117">API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="be4e6-117">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="be4e6-118">API de impressão GDI</span><span class="sxs-lookup"><span data-stu-id="be4e6-118">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="be4e6-119">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="be4e6-119">Print Schema Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[<span data-ttu-id="be4e6-120">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="be4e6-120">XML Paper Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



