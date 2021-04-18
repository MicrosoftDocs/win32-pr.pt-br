---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilidades de consumidores do documento de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105787727"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a><span data-ttu-id="3f1d9-104">Responsabilidades de consumidores do documento de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="3f1d9-104">Responsibilities of Consumers of the PrintCapabilities Document</span></span>

<span data-ttu-id="3f1d9-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-105">This topic is not current.</span></span> <span data-ttu-id="3f1d9-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3f1d9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3f1d9-107">Os consumidores de documentos de PrintCapabilities têm determinadas obrigações que devem ser suspensos antes que possam usar um documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-107">Consumers of PrintCapabilities documents have certain obligations they must uphold before they can use a PrintCapabilities document.</span></span> <span data-ttu-id="3f1d9-108">Os requisitos a seguir se aplicam aos clientes de um documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-108">The following requirements apply to clients of a PrintCapabilities document.</span></span>

-   <span data-ttu-id="3f1d9-109">Eles não devem rejeitar ou não processar nenhum recurso de PrintCapabilities sintaticamente válido; ou seja, qualquer documento de PrintCapabilities que esteja de acordo com o esquema de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-109">They must not reject or fail to process any syntactically valid PrintCapabilities; that is, any PrintCapabilities document that conforms to the PrintCapabilities Schema.</span></span>

-   <span data-ttu-id="3f1d9-110">Eles devem ser capazes de contornar a presença inesperada ou a ausência de conteúdo definido de modo privado.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-110">They must be able to work around the unexpected presence or absence of privately-defined content.</span></span> <span data-ttu-id="3f1d9-111">Isso inclui conteúdo definido de modo privado que aparece em instâncias de elementos de impressão definidos pelo esquema.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-111">This includes privately-defined content that appears within instances of Print Schema-defined elements.</span></span>

-   <span data-ttu-id="3f1d9-112">Eles devem ser capazes de contornar o conteúdo de esquema de impressão opcional que está ausente.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-112">They must be able to work around optional Print Schema content that is absent.</span></span>

-   <span data-ttu-id="3f1d9-113">Eles devem estar cientes de quando solicitar um novo documento.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-113">They must be aware of when to request a new document.</span></span>

    -   <span data-ttu-id="3f1d9-114">Os valores das instâncias de propriedade são dependentes de configuração (portanto, dependente de instantâneo).</span><span class="sxs-lookup"><span data-stu-id="3f1d9-114">Values of Property instances are configuration-dependent (hence, snapshot-dependent).</span></span> <span data-ttu-id="3f1d9-115">Você deve atualizar o instantâneo ao acessar uma instância de propriedade.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-115">You must update the snapshot when you access a Property instance.</span></span>

    -   <span data-ttu-id="3f1d9-116">As instâncias Feature, Option e ScoredProperty que devem ser copiadas para um PrintTicket são por definição estática.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-116">Feature, Option and ScoredProperty instances that are to be copied to a PrintTicket are by definition static.</span></span> <span data-ttu-id="3f1d9-117">Ou seja, eles não são (e não devem ser) dependentes da configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-117">That is, they are not (and must not be) dependent on the device configuration.</span></span> <span data-ttu-id="3f1d9-118">Se você acessar qualquer instância desses tipos, não será necessário obter um novo documento de PrintCapabilities quando a configuração for alterada.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-118">If you access any instances of these types, you do not need to obtain a new PrintCapabilities document when the configuration changes.</span></span>

-   <span data-ttu-id="3f1d9-119">Os consumidores de PrintCapabilities que são clientes da interface do usuário (IU) devem ser capazes de usar informações em um documento de PrintCapabilities para construir uma interface do usuário e construir um PrintTicket válido a partir das seleções do usuário.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-119">Consumers of PrintCapabilities that are user interface (UI) clients must be able to use information in a PrintCapabilities document to construct a user interface and to construct a valid PrintTicket from the user selections.</span></span> <span data-ttu-id="3f1d9-120">Isso inclui saber quais instâncias de ParameterInit devem ser especificadas e validar as instâncias especificadas.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-120">This includes knowing which ParameterInit instances must be specified, and validating those instances that are specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f1d9-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f1d9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f1d9-122">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="3f1d9-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



