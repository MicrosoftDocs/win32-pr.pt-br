---
description: Veja como o autor de um cliente PrintTicket pode usar tipos de elementos para criar um PrintTicket que descreva as intenções de um dispositivo.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Listas de verificação de construção do PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76d47911d0060cc6d06604bfaeaa4abcebd3daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405469"
---
# <a name="printticket-construction-checklists"></a><span data-ttu-id="17eed-103">Listas de verificação de construção do PrintTicket</span><span class="sxs-lookup"><span data-stu-id="17eed-103">PrintTicket Construction Checklists</span></span>

<span data-ttu-id="17eed-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="17eed-104">This topic is not current.</span></span> <span data-ttu-id="17eed-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="17eed-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="17eed-106">Esta seção demonstra como o autor de um cliente PrintTicket pode usar os tipos de elemento definidos na estrutura de esquema de impressão para criar um PrintTicket que descreve as intenções de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="17eed-106">This section demonstrates how the author of a PrintTicket client can use the element types defined in the Print Schema Framework to create a PrintTicket that describes intents for a device.</span></span> <span data-ttu-id="17eed-107">O PrintTicket pode ser genérico (não vinculado a um dispositivo específico) ou pode ser específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="17eed-107">The PrintTicket can be generic (not tied to a specific device), or it can be device-specific.</span></span> <span data-ttu-id="17eed-108">A semântica do PrintTicket é apresentada mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="17eed-108">The semantics of the PrintTicket are presented in greater detail.</span></span> <span data-ttu-id="17eed-109">Além disso, esta seção contém uma visão geral dos conceitos e da terminologia que são abordados em mais detalhes nas seções subsequentes.</span><span class="sxs-lookup"><span data-stu-id="17eed-109">In addition, this section contains an overview of concepts and terminology that are covered in more depth in subsequent sections.</span></span>

<span data-ttu-id="17eed-110">Há duas abordagens fundamentalmente diferentes para construir um PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="17eed-110">There are two fundamentally different approaches to constructing a PrintTicket.</span></span> <span data-ttu-id="17eed-111">Qualquer uma das abordagens pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="17eed-111">Either approach can be used.</span></span>

-   <span data-ttu-id="17eed-112">Direcione o PrintTicket para um dispositivo desconhecido ou genérico [criando um PrintTicket genérico](creating-a-generic-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="17eed-112">Target the PrintTicket to an unknown or generic device by [Creating a Generic PrintTicket](creating-a-generic-printticket.md).</span></span>

    <span data-ttu-id="17eed-113">Se seu objetivo principal é preservar a intenção do usuário final, talvez você queira adotar essa abordagem, construindo e armazenando um PrintTicket genérico não validado com o documento.</span><span class="sxs-lookup"><span data-stu-id="17eed-113">If your primary objective is to preserve the end user's intent, you might want to take this approach, by constructing and storing an unvalidated generic PrintTicket with the document.</span></span>

-   <span data-ttu-id="17eed-114">Direcione o PrintTicket para um dispositivo específico, [criando um Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="17eed-114">Target the PrintTicket to a specific device, by [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span></span>

    <span data-ttu-id="17eed-115">Se você estiver mais interessado em aproveitar todos os recursos oferecidos por um determinado dispositivo, talvez queira adotar essa abordagem criando um PrintTicket para o dispositivo específico e armazenando o PrintTicket validado com o documento.</span><span class="sxs-lookup"><span data-stu-id="17eed-115">If you are more interested in taking advantage of all of the features offered by a particular device, you might want to take this approach, by constructing a PrintTicket for the specific device and storing the validated PrintTicket with the document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17eed-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17eed-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17eed-117">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="17eed-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



