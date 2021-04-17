---
description: A interface IX509SCEPEnrollment expõe os métodos a seguir.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Métodos IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779957"
---
# <a name="ix509scepenrollment-methods"></a><span data-ttu-id="81216-103">Métodos IX509SCEPEnrollment</span><span class="sxs-lookup"><span data-stu-id="81216-103">IX509SCEPEnrollment Methods</span></span>

<span data-ttu-id="81216-104">A interface [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expõe os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="81216-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="81216-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="81216-105">In this section</span></span>



| <span data-ttu-id="81216-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="81216-106">Topic</span></span>                                                                                                              | <span data-ttu-id="81216-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="81216-107">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81216-108">**Método CreateRequestMessage**</span><span class="sxs-lookup"><span data-stu-id="81216-108">**CreateRequestMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | <span data-ttu-id="81216-109">Crie uma mensagem de solicitação PKCS10 com uma senha de desafio.</span><span class="sxs-lookup"><span data-stu-id="81216-109">Create a PKCS10 request message with a challenge password.</span></span> <span data-ttu-id="81216-110">A mensagem de solicitação está em um PKCS7 envelopado criptografado com o certificado de criptografia do servidor SCEP e assinado pelo certificado de autenticação do servidor.</span><span class="sxs-lookup"><span data-stu-id="81216-110">The request message is in an enveloped PKCS7 encrypted with the SCEP server encryption certificate and signed by the server signing certificate.</span></span><br/> |
| [<span data-ttu-id="81216-111">**Método CreateRetrieveCertificateMessage**</span><span class="sxs-lookup"><span data-stu-id="81216-111">**CreateRetrieveCertificateMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | <span data-ttu-id="81216-112">Recupere um certificado emitido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="81216-112">Retrieve a previously issued certificate.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="81216-113">**Método CreateRetrievePendingMessage**</span><span class="sxs-lookup"><span data-stu-id="81216-113">**CreateRetrievePendingMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | <span data-ttu-id="81216-114">Crie uma mensagem para sondagem de certificado (registro manual).</span><span class="sxs-lookup"><span data-stu-id="81216-114">Create a message for certificate polling (manual enrollment).</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="81216-115">**Método DeleteRequest**</span><span class="sxs-lookup"><span data-stu-id="81216-115">**DeleteRequest method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | <span data-ttu-id="81216-116">Exclua quaisquer certificados ou chaves criadas para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="81216-116">Delete any certificates or keys created for the request.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="81216-117">**Método Initialize**</span><span class="sxs-lookup"><span data-stu-id="81216-117">**Initialize method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | <span data-ttu-id="81216-118">Inicialize a instância em preparação para uma nova solicitação.</span><span class="sxs-lookup"><span data-stu-id="81216-118">Initialize the instance in preparation for a new request.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="81216-119">**Método InitializeForPending**</span><span class="sxs-lookup"><span data-stu-id="81216-119">**InitializeForPending method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | <span data-ttu-id="81216-120">Inicialize a instância para se preparar para gerar uma mensagem para recuperar um certificado emitido ou instalar uma resposta para uma solicitação anterior pelo emissor.</span><span class="sxs-lookup"><span data-stu-id="81216-120">Initialize the instance to prepare to generate a message to either retrieve an issued certificate, or install a response for a previous request by the issuer.</span></span><br/>                                              |
| [<span data-ttu-id="81216-121">**Método ProcessResponseMessage**</span><span class="sxs-lookup"><span data-stu-id="81216-121">**ProcessResponseMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | <span data-ttu-id="81216-122">Processar uma mensagem de resposta e retornar a disposição da mensagem.</span><span class="sxs-lookup"><span data-stu-id="81216-122">Process a response message and return the disposition of the message.</span></span><br/>                                                                                                                                       |



 

 

 




