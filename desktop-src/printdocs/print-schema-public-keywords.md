---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Imprimir palavras-chave públicas do esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3e8fb9a46bbed2b135f4e81456dd65e79be830
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105751603"
---
# <a name="print-schema-public-keywords"></a><span data-ttu-id="a7c20-104">Imprimir palavras-chave públicas do esquema</span><span class="sxs-lookup"><span data-stu-id="a7c20-104">Print Schema Public Keywords</span></span>

<span data-ttu-id="a7c20-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a7c20-105">This topic is not current.</span></span> <span data-ttu-id="a7c20-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a7c20-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a7c20-107">A seção a seguir especifica as palavras-chave públicas que são definidas para o esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="a7c20-107">The following section specifies the public keywords which are defined for the Print Schema.</span></span>

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a><span data-ttu-id="a7c20-108">Imprimir o uso de palavras-chave públicas do esquema para recursos de impressão</span><span class="sxs-lookup"><span data-stu-id="a7c20-108">Print Schema Public Keywords Usage for Print Capabilities</span></span>

<span data-ttu-id="a7c20-109">Palavras-chave especificadas em palavras-chave públicas de PrintCapabilities podem aparecer em um documento de recursos de impressão.</span><span class="sxs-lookup"><span data-stu-id="a7c20-109">Keywords specified under PrintCapabilities Public Keywords MAY appear in a Print Capabilities document.</span></span> <span data-ttu-id="a7c20-110">Para obter mais informações sobre como essas palavras-chave interagem com a tecnologia PrintCapabilities, consulte [visão geral da seção PrintCapabilities](overview-of-the-printcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="a7c20-110">For more information on how these keywords interact with PrintCapabilities technology, please refer to [Overview of the PrintCapabilities](overview-of-the-printcapabilities.md) section.</span></span>

<span data-ttu-id="a7c20-111">Palavras-chave públicas específicas do PrintTicket não devem aparecer em um documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a7c20-111">Public keywords specific to PrintTicket SHOULD NOT appear in a PrintCapabilities document.</span></span>

## <a name="print-schema-public-keywords-usage-for-printticket"></a><span data-ttu-id="a7c20-112">Imprimir o uso de palavras-chave públicas do esquema para PrintTicket</span><span class="sxs-lookup"><span data-stu-id="a7c20-112">Print Schema Public Keywords Usage for PrintTicket</span></span>

<span data-ttu-id="a7c20-113">Palavras-chave especificadas em palavras-chave públicas PrintTicket podem aparecer em um PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="a7c20-113">Keywords specified under PrintTicket Public Keywords MAY appear in a PrintTicket.</span></span> <span data-ttu-id="a7c20-114">As palavras-chave PrintTicket são implementadas como um tipo de elemento de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a7c20-114">PrintTicket keywords are implemented as a Property element type.</span></span> <span data-ttu-id="a7c20-115">Para obter mais informações sobre como essas palavras-chave interagem com a tecnologia PrintTicket, consulte [informações de configuração não relacionadas à seção PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="a7c20-115">For more information on how these keywords interact with PrintTicket technology, please refer to [Configuration Information Not Related to PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) section.</span></span>

<span data-ttu-id="a7c20-116">Palavras-chave especificadas em palavras-chave públicas de PrintCapabilities podem aparecer em um PrintTicket, dependendo da implementação do PrintTicket em um aplicativo e/ou driver.</span><span class="sxs-lookup"><span data-stu-id="a7c20-116">Keywords specified under PrintCapabilities Public Keywords MAY appear in a PrintTicket depending on the implementation of the PrintTicket in an application and/or driver.</span></span> <span data-ttu-id="a7c20-117">Isso fornece seleções para atributos de dispositivo definidos no documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a7c20-117">This provides selections for device attributes defined in the PrintCapabilities document.</span></span> <span data-ttu-id="a7c20-118">Para obter mais informações sobre a interação entre as palavras-chave de PrintCapabilities e o PrintTicket, consulte a [finalidade da seção PrintTicket](purpose-of-the-printticket.md) .</span><span class="sxs-lookup"><span data-stu-id="a7c20-118">For more information on the interaction between PrintCapabilities keywords and the PrintTicket, please refer to [Purpose of the PrintTicket](purpose-of-the-printticket.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7c20-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7c20-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7c20-120">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a7c20-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



