---
description: A predefinição de notação de sintaxe abstrata (ASN. 1) define os seguintes conjuntos de regras que regem como as estruturas de dados que estão sendo enviadas entre computadores são codificadas e decodificadas.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: Distinguished Encoding Rules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501972"
---
# <a name="distinguished-encoding-rules"></a><span data-ttu-id="8e88b-103">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="8e88b-103">Distinguished Encoding Rules</span></span>

<span data-ttu-id="8e88b-104">A predefinição de notação de sintaxe abstrata (ASN. 1) define os seguintes conjuntos de regras que regem como as estruturas de dados que estão sendo enviadas entre computadores são codificadas e decodificadas.</span><span class="sxs-lookup"><span data-stu-id="8e88b-104">Abstract Syntax Notation One (ASN.1) defines the following rule sets that govern how data structures that are being sent between computers are encoded and decoded.</span></span>

-   <span data-ttu-id="8e88b-105">Regras básicas de codificação (BER)</span><span class="sxs-lookup"><span data-stu-id="8e88b-105">Basic Encoding Rules (BER)</span></span>
-   <span data-ttu-id="8e88b-106">CER (regras de codificação canônica)</span><span class="sxs-lookup"><span data-stu-id="8e88b-106">Canonical Encoding Rules (CER)</span></span>
-   <span data-ttu-id="8e88b-107">Distinguished Encoding Rules (DER)</span><span class="sxs-lookup"><span data-stu-id="8e88b-107">Distinguished Encoding Rules (DER)</span></span>
-   <span data-ttu-id="8e88b-108">Regras de codificação empacotadas (por)</span><span class="sxs-lookup"><span data-stu-id="8e88b-108">Packed Encoding Rules (PER)</span></span>

<span data-ttu-id="8e88b-109">O conjunto de regras original foi definido pela especificação BER.</span><span class="sxs-lookup"><span data-stu-id="8e88b-109">The original rule set was defined by the BER specification.</span></span> <span data-ttu-id="8e88b-110">CER e DER foram desenvolvidos posteriormente como subconjuntos especializados do BER.</span><span class="sxs-lookup"><span data-stu-id="8e88b-110">CER and DER were developed later as specialized subsets of BER.</span></span> <span data-ttu-id="8e88b-111">POR foi desenvolvido em resposta a críticas sobre a quantidade de largura de banda necessária para transmitir dados usando o BER ou suas variantes.</span><span class="sxs-lookup"><span data-stu-id="8e88b-111">PER was developed in response to criticisms about the amount of bandwidth required to transmit data using BER or its variants.</span></span> <span data-ttu-id="8e88b-112">POR fornece uma economia significativa.</span><span class="sxs-lookup"><span data-stu-id="8e88b-112">PER provides a significant savings.</span></span>

<span data-ttu-id="8e88b-113">O DER foi criado para atender aos requisitos da especificação X. 509 para transferência segura de dados.</span><span class="sxs-lookup"><span data-stu-id="8e88b-113">DER was created to satisfy the requirements of the X.509 specification for secure data transfer.</span></span> <span data-ttu-id="8e88b-114">A API de registro de certificado usa DER exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="8e88b-114">The Certificate Enrollment API uses DER exclusively.</span></span> <span data-ttu-id="8e88b-115">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e88b-115">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="8e88b-116">Sintaxe de transferência de DER</span><span class="sxs-lookup"><span data-stu-id="8e88b-116">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
-   [<span data-ttu-id="8e88b-117">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8e88b-117">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a><span data-ttu-id="8e88b-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e88b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e88b-119">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8e88b-119">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="8e88b-120">Codificação de solicitação de certificado</span><span class="sxs-lookup"><span data-stu-id="8e88b-120">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="8e88b-121">Introdução à sintaxe e codificação ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8e88b-121">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



