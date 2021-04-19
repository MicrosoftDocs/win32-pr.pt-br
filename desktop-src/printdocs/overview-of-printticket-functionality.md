---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Visão geral da funcionalidade PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a70945fcc18e08615a9674a90a023f4ee12a76e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105754893"
---
# <a name="overview-of-printticket-functionality"></a><span data-ttu-id="f2f57-104">Visão geral da funcionalidade PrintTicket</span><span class="sxs-lookup"><span data-stu-id="f2f57-104">Overview of PrintTicket Functionality</span></span>

<span data-ttu-id="f2f57-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f2f57-105">This topic is not current.</span></span> <span data-ttu-id="f2f57-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f2f57-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f2f57-107">O PrintTicket utiliza um formato baseado em XML para expressar as informações de configuração do dispositivo usando o recurso/opção e as construções de parâmetro da estrutura de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="f2f57-107">The PrintTicket utilizes an XML-based format for expressing device configuration information using the Feature/Option and parameter constructs of the Print Schema Framework.</span></span> <span data-ttu-id="f2f57-108">Isso inclui todos os tipos de elemento padrão, bem como os recursos de extensibilidade da estrutura de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="f2f57-108">This includes all of the standard element types as well as the extensibility capabilities of the Print Schema Framework.</span></span> <span data-ttu-id="f2f57-109">Um PrintTicket é considerado uma descrição independente de como uma única página deve ser processada.</span><span class="sxs-lookup"><span data-stu-id="f2f57-109">A PrintTicket is assumed to be a self-contained description of how a single page is to be processed.</span></span> <span data-ttu-id="f2f57-110">As etapas envolvidas na extração e construção desse PrintTicket a partir de um determinado formato de documento não são abordadas aqui.</span><span class="sxs-lookup"><span data-stu-id="f2f57-110">The steps involved in extracting and constructing such a PrintTicket from a particular document format are not covered here.</span></span>

<span data-ttu-id="f2f57-111">Um PrintTicket pode ser usado para obter um documento de PrintCapabilities que descreve as características do dispositivo para uma configuração específica.</span><span class="sxs-lookup"><span data-stu-id="f2f57-111">A PrintTicket can be used to obtain a PrintCapabilities document describing the characteristics of the device for a particular configuration.</span></span> <span data-ttu-id="f2f57-112">Como alternativa, o PrintTicket pode ser enviado com um conjunto de instruções de renderização para produzir uma página de saída renderizada e processada de acordo com a configuração especificada no PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="f2f57-112">Alternatively, the PrintTicket can be submitted with a set of rendering instructions to produce a page of output rendered and processed according to the configuration specified in the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2f57-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2f57-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2f57-114">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f2f57-114">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



