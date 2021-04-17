---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Listas de verificação de construção do PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e742bcd3b94c5016fda6f97e2fb5e20a2cf70f73
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105763244"
---
# <a name="printticket-construction-checklists"></a><span data-ttu-id="ada27-104">Listas de verificação de construção do PrintTicket</span><span class="sxs-lookup"><span data-stu-id="ada27-104">PrintTicket Construction Checklists</span></span>

<span data-ttu-id="ada27-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="ada27-105">This topic is not current.</span></span> <span data-ttu-id="ada27-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ada27-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ada27-107">Esta seção demonstra como o autor de um cliente PrintTicket pode usar os tipos de elemento definidos na estrutura de esquema de impressão para criar um PrintTicket que descreve as intenções de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ada27-107">This section demonstrates how the author of a PrintTicket client can use the element types defined in the Print Schema Framework to create a PrintTicket that describes intents for a device.</span></span> <span data-ttu-id="ada27-108">O PrintTicket pode ser genérico (não vinculado a um dispositivo específico) ou pode ser específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ada27-108">The PrintTicket can be generic (not tied to a specific device), or it can be device-specific.</span></span> <span data-ttu-id="ada27-109">A semântica do PrintTicket é apresentada mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="ada27-109">The semantics of the PrintTicket are presented in greater detail.</span></span> <span data-ttu-id="ada27-110">Além disso, esta seção contém uma visão geral dos conceitos e da terminologia que são abordados em mais detalhes nas seções subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ada27-110">In addition, this section contains an overview of concepts and terminology that are covered in more depth in subsequent sections.</span></span>

<span data-ttu-id="ada27-111">Há duas abordagens fundamentalmente diferentes para construir um PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="ada27-111">There are two fundamentally different approaches to constructing a PrintTicket.</span></span> <span data-ttu-id="ada27-112">Qualquer uma das abordagens pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="ada27-112">Either approach can be used.</span></span>

-   <span data-ttu-id="ada27-113">Direcione o PrintTicket para um dispositivo desconhecido ou genérico [criando um PrintTicket genérico](creating-a-generic-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="ada27-113">Target the PrintTicket to an unknown or generic device by [Creating a Generic PrintTicket](creating-a-generic-printticket.md).</span></span>

    <span data-ttu-id="ada27-114">Se seu objetivo principal é preservar a intenção do usuário final, talvez você queira adotar essa abordagem, construindo e armazenando um PrintTicket genérico não validado com o documento.</span><span class="sxs-lookup"><span data-stu-id="ada27-114">If your primary objective is to preserve the end user's intent, you might want to take this approach, by constructing and storing an unvalidated generic PrintTicket with the document.</span></span>

-   <span data-ttu-id="ada27-115">Direcione o PrintTicket para um dispositivo específico, [criando um Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="ada27-115">Target the PrintTicket to a specific device, by [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span></span>

    <span data-ttu-id="ada27-116">Se você estiver mais interessado em aproveitar todos os recursos oferecidos por um determinado dispositivo, talvez queira adotar essa abordagem criando um PrintTicket para o dispositivo específico e armazenando o PrintTicket validado com o documento.</span><span class="sxs-lookup"><span data-stu-id="ada27-116">If you are more interested in taking advantage of all of the features offered by a particular device, you might want to take this approach, by constructing a PrintTicket for the specific device and storing the validated PrintTicket with the document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ada27-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ada27-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ada27-118">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="ada27-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



