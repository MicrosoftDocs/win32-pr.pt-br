---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 2c1d912e-464e-48d2-ba4f-c0b9a811b25e
title: Guia de início rápido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f3933cb59e270dd8ef2eff8d295d33ab1f9203
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104298004"
---
# <a name="quick-starter-guide"></a><span data-ttu-id="a4974-104">Guia de início rápido</span><span class="sxs-lookup"><span data-stu-id="a4974-104">Quick Starter Guide</span></span>

<span data-ttu-id="a4974-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a4974-105">This topic is not current.</span></span> <span data-ttu-id="a4974-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a4974-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a4974-107">Esta página foi projetada para dar a você um início rápido para implementar PrintTicket e PrintCapabilities para seu aplicativo ou driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4974-107">This page is designed to give you a quick start to implement PrintTicket and PrintCapabilities for your application or device driver.</span></span> <span data-ttu-id="a4974-108">Embora incentivamos que você leia a especificação do esquema de impressão de forma completa, esta página ajudará a dar um rápido começo nas principais áreas às quais você deve prestar atenção.</span><span class="sxs-lookup"><span data-stu-id="a4974-108">Although we encourage that you read the Print Schema specification in full, this page will help give you a jump start in key areas you should pay attention to.</span></span>

1) <span data-ttu-id="a4974-109">Leia as [tecnologias de Schema-Related de impressão](print-schema-related-technologies.md) para fornecer uma visão geral das tecnologias de PrintTicket e de recursos de impressão</span><span class="sxs-lookup"><span data-stu-id="a4974-109">Read the [Print Schema-Related Technologies](print-schema-related-technologies.md) to give you an overview of PrintTicket and Print Capabilities technologies</span></span>

2) <span data-ttu-id="a4974-110">Verifique se você tem um entendimento sobre o [Resumo dos tipos de elementos](summary-of-element-types.md) que são usados para expressar tecnologias relacionadas ao esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="a4974-110">Ensure that you have a grasp on the [Summary of Element Types](summary-of-element-types.md) which are used to express Print Schema related technologies.</span></span>

3) <span data-ttu-id="a4974-111">Os documentos e PrintTickets de PrintCapabilities são definidos em três níveis de [prefixo de escopo](scoping-prefix.md) , trabalho, documento e página.</span><span class="sxs-lookup"><span data-stu-id="a4974-111">PrintCapabilities documents and PrintTickets are defined at three [Scoping Prefix](scoping-prefix.md) levels, Job, Document and Page.</span></span>

4) <span data-ttu-id="a4974-112">Ler sobre os diferentes [atributos XML](xml-attributes.md) que são usados em diferentes tipos de elementos de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a4974-112">Read over the different [XML Attributes](xml-attributes.md) which are used within different Print Schema element types</span></span>

5) <span data-ttu-id="a4974-113">Examine a [lista de verificação de construção de documentos de PrintCapabilities](printcapabilities-document-construction-checklist.md) e também o exemplo de documento de [PrintCapabilities](printcapabilities-document-example.md) fornecido</span><span class="sxs-lookup"><span data-stu-id="a4974-113">Review the [PrintCapabilities Document Construction Checklist](printcapabilities-document-construction-checklist.md) and also the provided [PrintCapabilities Document Example](printcapabilities-document-example.md)</span></span>

6) <span data-ttu-id="a4974-114">Examine as [listas de verificação de construção do PrintTicket](printticket-construction-checklists.md) e também o [exemplo de PrintTicket](printticket-example.md) fornecido</span><span class="sxs-lookup"><span data-stu-id="a4974-114">Review the [PrintTicket Construction Checklists](printticket-construction-checklists.md) and also the provided [PrintTicket Example](printticket-example.md)</span></span>

7) <span data-ttu-id="a4974-115">Os provedores de PrintTicket também devem examinar a [lista de verificação de validação do PrintTicket](printticket-validation-checklist.md) para garantir a conformidade com a especificação do esquema de</span><span class="sxs-lookup"><span data-stu-id="a4974-115">PrintTicket providers should also review the [PrintTicket Validation Checklist](printticket-validation-checklist.md) to ensure conformance with the PrintSchema specification</span></span>

8) <span data-ttu-id="a4974-116">Examine os [elementos configuráveis do usuário](user-configurable-elements.md) e as [definições de parâmetros](parameter-definitions.md) chaves do esquema de impressão pública que podem aparecer em um documento de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="a4974-116">Review both [User Configurable Elements](user-configurable-elements.md) and [Parameter Definitions](parameter-definitions.md) public Print Schema keywords which may appear in a PrintCapabilities document</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4974-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4974-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4974-118">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a4974-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



