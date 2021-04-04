---
description: Em uma PKI da Microsoft, as solicitações de certificado são enviadas de computadores cliente para CAs (autoridades de certificação) como uma cadeia de caracteres binária que contém uma sequência de estruturas de dados codificados.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Codificação de solicitação de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd9dfedede4c7b10d4968242b1d27ad11e2b6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662170"
---
# <a name="certificate-request-encoding"></a><span data-ttu-id="49743-103">Codificação de solicitação de certificado</span><span class="sxs-lookup"><span data-stu-id="49743-103">Certificate Request Encoding</span></span>

<span data-ttu-id="49743-104">Em uma PKI da Microsoft, as solicitações de certificado são enviadas de computadores cliente para CAs (autoridades de certificação) como uma cadeia de caracteres binária que contém uma sequência de estruturas de dados codificados.</span><span class="sxs-lookup"><span data-stu-id="49743-104">In a Microsoft PKI, certificate requests are sent from client computers to certification authorities (CAs) as a binary string that contains a sequence of encoded data structures.</span></span> <span data-ttu-id="49743-105">A API de registro de certificado usa a notação de sintaxe abstrata um (ASN. 1) para descrever e codificar essas estruturas.</span><span class="sxs-lookup"><span data-stu-id="49743-105">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to describe and encode these structures.</span></span> <span data-ttu-id="49743-106">Para os fins desta documentação, o ASN. 1 pode ser dividido conceitualmente nas regras de sintaxe (ISO 8824) que descrevem as estruturas de dados e as regras de codificação (ISO 8825) que especificam como os dados serão codificados para transmissão de rede.</span><span class="sxs-lookup"><span data-stu-id="49743-106">For the purposes of this documentation, ASN.1 can be conceptually divided into the syntax rules (ISO 8824) that describe the data structures and the encoding rules (ISO 8825) that specify how the data is to be encoded for network transmission.</span></span> <span data-ttu-id="49743-107">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="49743-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="49743-108">Introdução à sintaxe e codificação ASN. 1</span><span class="sxs-lookup"><span data-stu-id="49743-108">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [<span data-ttu-id="49743-109">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="49743-109">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
-   [<span data-ttu-id="49743-110">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="49743-110">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)

## <a name="related-topics"></a><span data-ttu-id="49743-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="49743-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49743-112">Sobre a API de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="49743-112">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



