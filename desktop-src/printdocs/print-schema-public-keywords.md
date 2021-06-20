---
description: Este artigo especifica as palavras-chave públicas que são definidas para o esquema de impressão e seu uso para PrintCapabilities e PrintTicket.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Imprimir palavras-chave públicas do esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0878ced6b011393479657a4fcdd4b7b7f9a2b62a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407139"
---
# <a name="print-schema-public-keywords"></a><span data-ttu-id="8d615-103">Imprimir palavras-chave públicas do esquema</span><span class="sxs-lookup"><span data-stu-id="8d615-103">Print Schema Public Keywords</span></span>

<span data-ttu-id="8d615-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="8d615-104">This topic is not current.</span></span> <span data-ttu-id="8d615-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8d615-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8d615-106">A seção a seguir especifica as palavras-chave públicas que são definidas para o esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="8d615-106">The following section specifies the public keywords which are defined for the Print Schema.</span></span>

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a><span data-ttu-id="8d615-107">Uso de palavras-chave públicas de esquema de impressão para funcionalidades de impressão</span><span class="sxs-lookup"><span data-stu-id="8d615-107">Print Schema Public Keywords Usage for Print Capabilities</span></span>

<span data-ttu-id="8d615-108">Palavras-chave especificadas em Palavras-chave públicas PrintCapabilities PODEM aparecer em um documento Funcionalidades de Impressão.</span><span class="sxs-lookup"><span data-stu-id="8d615-108">Keywords specified under PrintCapabilities Public Keywords MAY appear in a Print Capabilities document.</span></span> <span data-ttu-id="8d615-109">Para obter mais informações sobre como essas palavras-chave interagem com a tecnologia PrintCapabilities, consulte Visão geral [da seção PrintCapabilities.](overview-of-the-printcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="8d615-109">For more information on how these keywords interact with PrintCapabilities technology, please refer to [Overview of the PrintCapabilities](overview-of-the-printcapabilities.md) section.</span></span>

<span data-ttu-id="8d615-110">Palavras-chave públicas específicas para PrintTicket SHOULD NÃO devem aparecer em um documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="8d615-110">Public keywords specific to PrintTicket SHOULD NOT appear in a PrintCapabilities document.</span></span>

## <a name="print-schema-public-keywords-usage-for-printticket"></a><span data-ttu-id="8d615-111">Uso de palavras-chave públicas de esquema de impressão para PrintTicket</span><span class="sxs-lookup"><span data-stu-id="8d615-111">Print Schema Public Keywords Usage for PrintTicket</span></span>

<span data-ttu-id="8d615-112">Palavras-chave especificadas em Palavras-chave públicas printTicket PODEM aparecer em um PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="8d615-112">Keywords specified under PrintTicket Public Keywords MAY appear in a PrintTicket.</span></span> <span data-ttu-id="8d615-113">As palavras-chave PrintTicket são implementadas como um tipo de elemento Property.</span><span class="sxs-lookup"><span data-stu-id="8d615-113">PrintTicket keywords are implemented as a Property element type.</span></span> <span data-ttu-id="8d615-114">Para obter mais informações sobre como essas palavras-chave interagem com a tecnologia PrintTicket, consulte a seção Informações de configuração não relacionadas [a PrintCapabilities.](configuration-information-not-related-to-printcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="8d615-114">For more information on how these keywords interact with PrintTicket technology, please refer to [Configuration Information Not Related to PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) section.</span></span>

<span data-ttu-id="8d615-115">Palavras-chave especificadas em Palavras-chave públicas PrintCapabilities PODEM aparecer em um PrintTicket dependendo da implementação do PrintTicket em um aplicativo e/ou driver.</span><span class="sxs-lookup"><span data-stu-id="8d615-115">Keywords specified under PrintCapabilities Public Keywords MAY appear in a PrintTicket depending on the implementation of the PrintTicket in an application and/or driver.</span></span> <span data-ttu-id="8d615-116">Isso fornece seleções para atributos de dispositivo definidos no documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="8d615-116">This provides selections for device attributes defined in the PrintCapabilities document.</span></span> <span data-ttu-id="8d615-117">Para obter mais informações sobre a interação entre palavras-chave PrintCapabilities e PrintTicket, consulte a seção Finalidade da [PrintTicket.](purpose-of-the-printticket.md)</span><span class="sxs-lookup"><span data-stu-id="8d615-117">For more information on the interaction between PrintCapabilities keywords and the PrintTicket, please refer to [Purpose of the PrintTicket](purpose-of-the-printticket.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d615-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d615-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d615-119">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="8d615-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



