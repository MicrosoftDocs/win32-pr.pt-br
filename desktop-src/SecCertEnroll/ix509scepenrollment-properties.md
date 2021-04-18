---
description: A interface IX509SCEPEnrollment expõe as propriedades a seguir.
ms.assetid: 53BE8DE9-87AC-41D1-B1B5-2FEC72F5FCEA
title: Propriedades de IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd9b4cbf9df87f898e61ce0220243044b24607d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789502"
---
# <a name="ix509scepenrollment-properties"></a><span data-ttu-id="69b05-103">Propriedades de IX509SCEPEnrollment</span><span class="sxs-lookup"><span data-stu-id="69b05-103">IX509SCEPEnrollment Properties</span></span>

<span data-ttu-id="69b05-104">A interface [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expõe as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="69b05-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="69b05-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="69b05-105">In this section</span></span>



| <span data-ttu-id="69b05-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="69b05-106">Topic</span></span>                                                                                              | <span data-ttu-id="69b05-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="69b05-107">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69b05-108">**Propriedade de certificado**</span><span class="sxs-lookup"><span data-stu-id="69b05-108">**Certificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificate)<br/>                         | <span data-ttu-id="69b05-109">Obtém o certificado para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="69b05-109">Gets the certificate for the request.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="69b05-110">**Propriedade CertificateFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="69b05-110">**CertificateFriendlyName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname)<br/> | <span data-ttu-id="69b05-111">Obtém ou define o nome amigável do certificado.</span><span class="sxs-lookup"><span data-stu-id="69b05-111">Gets or sets the friendly name for the certificate.</span></span><br/>                                                                                         |
| [<span data-ttu-id="69b05-112">**Propriedade FailInfo**</span><span class="sxs-lookup"><span data-stu-id="69b05-112">**FailInfo property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_failinfo)<br/>                               | <span data-ttu-id="69b05-113">Obtém informações quando o método [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) detecta um ambiente com falha.</span><span class="sxs-lookup"><span data-stu-id="69b05-113">Gets information when the [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) method detects a failed environment.</span></span><br/> |
| [<span data-ttu-id="69b05-114">**Propriedade OldCertificate**</span><span class="sxs-lookup"><span data-stu-id="69b05-114">**OldCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate)<br/>                   | <span data-ttu-id="69b05-115">Obtém ou define um certificado antigo que uma solicitação deve substituir.</span><span class="sxs-lookup"><span data-stu-id="69b05-115">Gets or sets an old certificate that a request is intended to replace.</span></span><br/>                                                                      |
| [<span data-ttu-id="69b05-116">**Propriedade de solicitação**</span><span class="sxs-lookup"><span data-stu-id="69b05-116">**Request property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_request)<br/>                                 | <span data-ttu-id="69b05-117">Obtém a solicitação PKCS10 interna.</span><span class="sxs-lookup"><span data-stu-id="69b05-117">Gets the inner PKCS10 request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="69b05-118">**Propriedade ServerCapabilities**</span><span class="sxs-lookup"><span data-stu-id="69b05-118">**ServerCapabilities property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities)<br/>           | <span data-ttu-id="69b05-119">Define o hash preferencial e os algoritmos de criptografia para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="69b05-119">Sets the preferred hash and encryption algorithms for the request.</span></span><br/>                                                                          |
| [<span data-ttu-id="69b05-120">**Propriedade SignerCertificate**</span><span class="sxs-lookup"><span data-stu-id="69b05-120">**SignerCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate)<br/>             | <span data-ttu-id="69b05-121">Obtém ou define o certificado do signatário para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="69b05-121">Gets or sets the signer certificate for the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="69b05-122">**Propriedade silenciosa**</span><span class="sxs-lookup"><span data-stu-id="69b05-122">**Silent property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_silent)<br/>                                   | <span data-ttu-id="69b05-123">Obtém ou define se a interface do usuário deve ser permitida durante a solicitação.</span><span class="sxs-lookup"><span data-stu-id="69b05-123">Gets or sets whether to allow UI during the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="69b05-124">**Propriedade de status**</span><span class="sxs-lookup"><span data-stu-id="69b05-124">**Status property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_status)<br/>                                   | <span data-ttu-id="69b05-125">Obtém o status da solicitação.</span><span class="sxs-lookup"><span data-stu-id="69b05-125">Gets the status of the request.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="69b05-126">**Propriedade TransactionId**</span><span class="sxs-lookup"><span data-stu-id="69b05-126">**TransactionId property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_transactionid)<br/>                     | <span data-ttu-id="69b05-127">Obtém ou define a ID da transação para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="69b05-127">Gets or sets the transaction id for the request.</span></span><br/>                                                                                            |



 

 

 




