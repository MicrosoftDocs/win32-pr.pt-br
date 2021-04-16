---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: O que é um documento de PrintCapabilities não
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e18082a5e551f3997dad8b9688d84ff2f824a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105765223"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="82931-104">O que é um documento de PrintCapabilities não</span><span class="sxs-lookup"><span data-stu-id="82931-104">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="82931-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="82931-105">This topic is not current.</span></span> <span data-ttu-id="82931-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="82931-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="82931-107">Vale a pena listar algumas das funcionalidades e informações que o documento de PrintCapabilities não pretende fornecer.</span><span class="sxs-lookup"><span data-stu-id="82931-107">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="82931-108">Um documento de PrintCapabilities:</span><span class="sxs-lookup"><span data-stu-id="82931-108">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="82931-109">Não representa dados de valores de multivalor (dependentes de configuração).</span><span class="sxs-lookup"><span data-stu-id="82931-109">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="82931-110">Cada documento de PrintCapabilities é construído para uma configuração específica.</span><span class="sxs-lookup"><span data-stu-id="82931-110">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="82931-111">Nenhuma propriedade ou ScoredProperty no documento pode ter um valor que depende da configuração específica.</span><span class="sxs-lookup"><span data-stu-id="82931-111">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="82931-112">Na versão do esquema inicial, o provedor de PrintCapabilities deve processar o PrintTicket de entrada e criar um documento de PrintCapabilities que contenha valores de propriedade apropriados para a configuração especificada no PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="82931-112">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="82931-113">Não contém informações de restrição.</span><span class="sxs-lookup"><span data-stu-id="82931-113">Does not contain constraint information.</span></span>

    <span data-ttu-id="82931-114">O documento PrintCapabilities não indica quais configurações são permitidas e quais não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="82931-114">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="82931-115">Na versão do esquema inicial, o provedor de PrintCapabilities deve armazenar todas as informações necessárias para validar as configurações, fornecer um método que valida o PrintTicket de entrada e retornar um PrintTicket corrigido caso o PrintTicket especificado viole uma ou mais restrições.</span><span class="sxs-lookup"><span data-stu-id="82931-115">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="82931-116">Não contém informações dinâmicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82931-116">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="82931-117">Há muita sobrecarga envolvida na construção do documento PrintCapabilities para que ele seja usado para manter a alteração rápida de informações de status, como níveis de tinta, papel restante em cada bandeja ou status de emperramento de papel.</span><span class="sxs-lookup"><span data-stu-id="82931-117">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82931-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82931-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82931-119">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="82931-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



