---
description: Explica como os serviços de certificados processam solicitações de certificado.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Processando solicitações de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567929"
---
# <a name="processing-certificate-requests"></a><span data-ttu-id="7ff95-103">Processando solicitações de certificado</span><span class="sxs-lookup"><span data-stu-id="7ff95-103">Processing Certificate Requests</span></span>

<span data-ttu-id="7ff95-104">Os serviços de certificados executam as seguintes etapas ao processar uma [*solicitação de certificado*](../secgloss/c-gly.md):</span><span class="sxs-lookup"><span data-stu-id="7ff95-104">Certificate Services performs the following steps when processing a [*certificate request*](../secgloss/c-gly.md):</span></span>

1.  <span data-ttu-id="7ff95-105">Solicitar recebimento.</span><span class="sxs-lookup"><span data-stu-id="7ff95-105">Request reception.</span></span>

    <span data-ttu-id="7ff95-106">A [*solicitação de certificado*](../secgloss/c-gly.md) é enviada pelo cliente para um aplicativo intermediário, que o formata em uma \# solicitação de formato PKCS 10 e a envia para o mecanismo do servidor.</span><span class="sxs-lookup"><span data-stu-id="7ff95-106">The [*certificate request*](../secgloss/c-gly.md) is sent by the client to an intermediary application, which formats it into a PKCS \#10 format request and submits it to the server engine.</span></span>

2.  <span data-ttu-id="7ff95-107">Solicitar aprovação.</span><span class="sxs-lookup"><span data-stu-id="7ff95-107">Request approval.</span></span>

    <span data-ttu-id="7ff95-108">O mecanismo de servidor chama o [módulo de política](policy-modules.md), que consulta as propriedades da solicitação, decide se a solicitação está autorizada ou não e define as propriedades opcionais do certificado.</span><span class="sxs-lookup"><span data-stu-id="7ff95-108">The server engine calls the [Policy Module](policy-modules.md), which queries request properties, decides whether the request is authorized or not, and sets optional certificate properties.</span></span>

3.  <span data-ttu-id="7ff95-109">Formação do certificado.</span><span class="sxs-lookup"><span data-stu-id="7ff95-109">Certificate formation.</span></span>

    <span data-ttu-id="7ff95-110">Se a solicitação for aprovada, o mecanismo do servidor usará a solicitação e todas as propriedades solicitadas pelo módulo de política e criará um certificado completo.</span><span class="sxs-lookup"><span data-stu-id="7ff95-110">If the request is approved, the server engine takes the request, and any properties requested by the Policy Module, and builds a complete certificate.</span></span>

4.  <span data-ttu-id="7ff95-111">Publicação de certificado.</span><span class="sxs-lookup"><span data-stu-id="7ff95-111">Certificate publication.</span></span>

    <span data-ttu-id="7ff95-112">O mecanismo de servidor armazena o certificado concluído no banco de dados de serviços de certificados e notifica o aplicativo intermediário do status da solicitação.</span><span class="sxs-lookup"><span data-stu-id="7ff95-112">The server engine stores the completed certificate in the Certificate Services database and notifies the intermediary application of the request status.</span></span> <span data-ttu-id="7ff95-113">Se o [módulo de saída](exit-modules.md) tiver sido solicitado, o mecanismo do servidor irá notificá-lo de um evento de emissão de certificado.</span><span class="sxs-lookup"><span data-stu-id="7ff95-113">If the [exit module](exit-modules.md) has so requested, the server engine will notify it of a certificate issuance event.</span></span> <span data-ttu-id="7ff95-114">Isso permite que o módulo de saída execute outras operações, como publicar o certificado em um repositório de certificado externo (por exemplo, um serviço de diretório).</span><span class="sxs-lookup"><span data-stu-id="7ff95-114">This allows the exit module to perform further operations such as publishing the certificate to an external certificate repository (for example, a directory service).</span></span> <span data-ttu-id="7ff95-115">Enquanto isso, o intermediário Obtém o certificado publicado dos serviços de certificados e o passa de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="7ff95-115">Meanwhile, the intermediary gets the published certificate from Certificate Services and passes it back to the client.</span></span>

<span data-ttu-id="7ff95-116">A ilustração a seguir mostra como uma [*solicitação de certificado*](../secgloss/c-gly.md) é processada pelos serviços de certificados.</span><span class="sxs-lookup"><span data-stu-id="7ff95-116">The following illustration shows how a [*certificate request*](../secgloss/c-gly.md) is processed by Certificate Services.</span></span>

![processando uma solicitação de certificado](images/certflow.png)

 

 
