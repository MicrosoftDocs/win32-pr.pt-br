---
description: Esta visão geral da funcionalidade PrintTicket descreve o formato para expressar informações de configuração do dispositivo e o uso de um PrintTicket.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Visão geral da funcionalidade PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408539"
---
# <a name="overview-of-printticket-functionality"></a><span data-ttu-id="c35d1-103">Visão geral da funcionalidade PrintTicket</span><span class="sxs-lookup"><span data-stu-id="c35d1-103">Overview of PrintTicket Functionality</span></span>

<span data-ttu-id="c35d1-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="c35d1-104">This topic is not current.</span></span> <span data-ttu-id="c35d1-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c35d1-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c35d1-106">O PrintTicket utiliza um formato baseado em XML para expressar informações de configuração do dispositivo usando os constructos de recurso/opção e parâmetro da Estrutura de Esquema de Impressão.</span><span class="sxs-lookup"><span data-stu-id="c35d1-106">The PrintTicket utilizes an XML-based format for expressing device configuration information using the Feature/Option and parameter constructs of the Print Schema Framework.</span></span> <span data-ttu-id="c35d1-107">Isso inclui todos os tipos de elementos padrão, bem como os recursos de extensibilidade da Estrutura de Esquema de Impressão.</span><span class="sxs-lookup"><span data-stu-id="c35d1-107">This includes all of the standard element types as well as the extensibility capabilities of the Print Schema Framework.</span></span> <span data-ttu-id="c35d1-108">Um PrintTicket é assumido como uma descrição independente de como uma única página deve ser processada.</span><span class="sxs-lookup"><span data-stu-id="c35d1-108">A PrintTicket is assumed to be a self-contained description of how a single page is to be processed.</span></span> <span data-ttu-id="c35d1-109">As etapas envolvidas na extração e na construção desse printTicket de um formato de documento específico não são abordadas aqui.</span><span class="sxs-lookup"><span data-stu-id="c35d1-109">The steps involved in extracting and constructing such a PrintTicket from a particular document format are not covered here.</span></span>

<span data-ttu-id="c35d1-110">Um PrintTicket pode ser usado para obter um documento PrintCapabilities que descreve as características do dispositivo para uma configuração específica.</span><span class="sxs-lookup"><span data-stu-id="c35d1-110">A PrintTicket can be used to obtain a PrintCapabilities document describing the characteristics of the device for a particular configuration.</span></span> <span data-ttu-id="c35d1-111">Como alternativa, o PrintTicket pode ser enviado com um conjunto de instruções de renderização para produzir uma página de saída renderizada e processada de acordo com a configuração especificada no PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="c35d1-111">Alternatively, the PrintTicket can be submitted with a set of rendering instructions to produce a page of output rendered and processed according to the configuration specified in the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c35d1-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c35d1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c35d1-113">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="c35d1-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



