---
description: Os consumidores de documentos PrintCapabilities têm determinadas obrigações que devem cumprir antes de usar um documento PrintCapabilities.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilidades dos consumidores do documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec123509515de32b88c7352dcf0fc2c2b54504ff
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404939"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a><span data-ttu-id="a67fb-103">Responsabilidades dos consumidores do documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="a67fb-103">Responsibilities of Consumers of the PrintCapabilities Document</span></span>

<span data-ttu-id="a67fb-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a67fb-104">This topic is not current.</span></span> <span data-ttu-id="a67fb-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a67fb-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a67fb-106">Os consumidores de documentos PrintCapabilities têm determinadas obrigações que devem cumprir antes de usar um documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a67fb-106">Consumers of PrintCapabilities documents have certain obligations they must uphold before they can use a PrintCapabilities document.</span></span> <span data-ttu-id="a67fb-107">Os requisitos a seguir se aplicam aos clientes de um documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a67fb-107">The following requirements apply to clients of a PrintCapabilities document.</span></span>

-   <span data-ttu-id="a67fb-108">Eles não devem rejeitar ou não processar nenhum PrintCapabilities sintaticamente válido; ou seja, qualquer documento PrintCapabilities que esteja em conformidade com o esquema PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a67fb-108">They must not reject or fail to process any syntactically valid PrintCapabilities; that is, any PrintCapabilities document that conforms to the PrintCapabilities Schema.</span></span>

-   <span data-ttu-id="a67fb-109">Eles devem ser capazes de resolver a presença inesperada ou a ausência de conteúdo definido de forma privada.</span><span class="sxs-lookup"><span data-stu-id="a67fb-109">They must be able to work around the unexpected presence or absence of privately-defined content.</span></span> <span data-ttu-id="a67fb-110">Isso inclui conteúdo definido de forma privada que aparece em instâncias de elementos definidos pelo esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="a67fb-110">This includes privately-defined content that appears within instances of Print Schema-defined elements.</span></span>

-   <span data-ttu-id="a67fb-111">Eles devem ser capazes de resolver o conteúdo opcional do esquema de impressão que está ausente.</span><span class="sxs-lookup"><span data-stu-id="a67fb-111">They must be able to work around optional Print Schema content that is absent.</span></span>

-   <span data-ttu-id="a67fb-112">Eles devem estar cientes de quando solicitar um novo documento.</span><span class="sxs-lookup"><span data-stu-id="a67fb-112">They must be aware of when to request a new document.</span></span>

    -   <span data-ttu-id="a67fb-113">Os valores de Instâncias de propriedade dependem da configuração (portanto, dependentes de instantâneo).</span><span class="sxs-lookup"><span data-stu-id="a67fb-113">Values of Property instances are configuration-dependent (hence, snapshot-dependent).</span></span> <span data-ttu-id="a67fb-114">Você deve atualizar o instantâneo ao acessar uma instância de Propriedade.</span><span class="sxs-lookup"><span data-stu-id="a67fb-114">You must update the snapshot when you access a Property instance.</span></span>

    -   <span data-ttu-id="a67fb-115">As instâncias Feature, Option e ScoredProperty que devem ser copiadas para um PrintTicket são estáticas por definição.</span><span class="sxs-lookup"><span data-stu-id="a67fb-115">Feature, Option and ScoredProperty instances that are to be copied to a PrintTicket are by definition static.</span></span> <span data-ttu-id="a67fb-116">Ou seja, eles não são (e não devem ser) dependentes da configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a67fb-116">That is, they are not (and must not be) dependent on the device configuration.</span></span> <span data-ttu-id="a67fb-117">Se você acessar qualquer instância desses tipos, não precisará obter um novo documento PrintCapabilities quando a configuração for mudada.</span><span class="sxs-lookup"><span data-stu-id="a67fb-117">If you access any instances of these types, you do not need to obtain a new PrintCapabilities document when the configuration changes.</span></span>

-   <span data-ttu-id="a67fb-118">Os consumidores de PrintCapabilities que são clientes de interface do usuário devem ser capazes de usar informações em um documento PrintCapabilities para construir uma interface do usuário e construir um PrintTicket válido com base nas seleções do usuário.</span><span class="sxs-lookup"><span data-stu-id="a67fb-118">Consumers of PrintCapabilities that are user interface (UI) clients must be able to use information in a PrintCapabilities document to construct a user interface and to construct a valid PrintTicket from the user selections.</span></span> <span data-ttu-id="a67fb-119">Isso inclui saber quais instâncias ParameterInit devem ser especificadas e validar as instâncias especificadas.</span><span class="sxs-lookup"><span data-stu-id="a67fb-119">This includes knowing which ParameterInit instances must be specified, and validating those instances that are specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a67fb-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a67fb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a67fb-121">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a67fb-121">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



