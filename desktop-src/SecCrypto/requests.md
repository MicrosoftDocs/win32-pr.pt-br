---
description: Os serviços de certificados dão suporte a solicitações de certificado com base no \# formato PKCS 10 e no formato keygen (Netscape). Os serviços de certificados também dão suporte a \# solicitações de renovação PKCS 7 e a solicitações de CMS (sintaxe de mensagem criptografada).
ms.assetid: 6321ce99-f5d1-4d72-a062-99cffb543731
title: Requests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7870e09d930fb06d50f0cc8acfff1270db1c92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800075"
---
# <a name="requests"></a><span data-ttu-id="3c1da-104">Requests</span><span class="sxs-lookup"><span data-stu-id="3c1da-104">Requests</span></span>

<span data-ttu-id="3c1da-105">Os serviços de certificados dão suporte a [*solicitações de certificado*](../secgloss/c-gly.md) com base no \# formato PKCS 10 e no formato keygen (Netscape).</span><span class="sxs-lookup"><span data-stu-id="3c1da-105">Certificate Services supports [*certificate requests*](../secgloss/c-gly.md) based on the PKCS \#10 format and the Keygen (Netscape) format.</span></span> <span data-ttu-id="3c1da-106">Os serviços de certificados também dão suporte a \# solicitações de renovação PKCS 7 e a solicitações de CMS (sintaxe de mensagem criptografada).</span><span class="sxs-lookup"><span data-stu-id="3c1da-106">Certificate Services also supports PKCS \#7 renewal requests and Cryptographic Message Syntax (CMS) requests.</span></span>

<span data-ttu-id="3c1da-107">Os serviços de certificados também fornecem uma interface [ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) , que contém métodos para enviar uma solicitação de certificado e (se a solicitação for aprovada) para receber o certificado emitido resultante.</span><span class="sxs-lookup"><span data-stu-id="3c1da-107">Certificate Services also provides an [ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) interface, which contains methods for submitting a certificate request and (if the request is approved) for receiving the resulting issued certificate.</span></span>

<span data-ttu-id="3c1da-108">As interfaces adicionais relacionadas à segurança estão disponíveis no [controle de registro de certificado](certificate-enrollment-control.md).</span><span class="sxs-lookup"><span data-stu-id="3c1da-108">Additional security-related interfaces are available in the [Certificate Enrollment Control](certificate-enrollment-control.md).</span></span>

 

 
