---
description: Muitas das funções exigem tipos de codificação de certificado ou mensagem.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Tipos de codificação de certificado e mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3193b321d27892f8df9535ef81b8a988bf558e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461053"
---
# <a name="certificate-and-message-encoding-types"></a><span data-ttu-id="e97bc-103">Tipos de codificação de certificado e mensagem</span><span class="sxs-lookup"><span data-stu-id="e97bc-103">Certificate and Message Encoding Types</span></span>

<span data-ttu-id="e97bc-104">Muitas das funções exigem [*tipos de codificação*](../secgloss/m-gly.md)de certificado ou mensagem.</span><span class="sxs-lookup"><span data-stu-id="e97bc-104">Many of the functions require certificate or [*message encoding types*](../secgloss/m-gly.md).</span></span> <span data-ttu-id="e97bc-105">Esse tipo de codificação é um **DWORD**, possivelmente contendo os tipos de codificação de certificado e de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e97bc-105">This encoding type is a **DWORD**, possibly containing both the certificate and message encoding types.</span></span> <span data-ttu-id="e97bc-106">O tipo de codificação de certificado é armazenado na palavra de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="e97bc-106">The certificate encoding type is stored in the low-order word.</span></span> <span data-ttu-id="e97bc-107">O tipo de codificação de mensagem é armazenado na palavra de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="e97bc-107">The message encoding type is stored in the high-order word.</span></span> <span data-ttu-id="e97bc-108">Alguns campos de funções ou de estrutura exigem apenas um dos tipos de codificação, mas é sempre aceitável especificar os dois tipos de codificação.</span><span class="sxs-lookup"><span data-stu-id="e97bc-108">Some functions or structure fields require only one of the encoding types, but it is always acceptable to specify both encoding types.</span></span> <span data-ttu-id="e97bc-109">Para obter um exemplo que especifica os dois tipos de codificação, consulte [ \# inclusões e \# define](-includes-and--defines.md).</span><span class="sxs-lookup"><span data-stu-id="e97bc-109">For an example specifying both encoding types, see [\#includes and \#defines](-includes-and--defines.md).</span></span>

<span data-ttu-id="e97bc-110">A seguinte convenção de nomenclatura de parâmetro é usada para indicar os tipos de codificação necessários.</span><span class="sxs-lookup"><span data-stu-id="e97bc-110">The following parameter naming convention is used to indicate the encoding types required.</span></span>



| <span data-ttu-id="e97bc-111">Nome</span><span class="sxs-lookup"><span data-stu-id="e97bc-111">Name</span></span>                       | <span data-ttu-id="e97bc-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e97bc-112">Comments</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e97bc-113">*dwMsgAndCertEncodingType*</span><span class="sxs-lookup"><span data-stu-id="e97bc-113">*dwMsgAndCertEncodingType*</span></span> | <span data-ttu-id="e97bc-114">Ambos os tipos de codificação são necessários.</span><span class="sxs-lookup"><span data-stu-id="e97bc-114">Both encoding types are required.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e97bc-115">*dwMsgEncodingType*</span><span class="sxs-lookup"><span data-stu-id="e97bc-115">*dwMsgEncodingType*</span></span>        | <span data-ttu-id="e97bc-116">Somente o tipo de codificação de mensagem é necessário.</span><span class="sxs-lookup"><span data-stu-id="e97bc-116">Only the message encoding type is required.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e97bc-117">*dwCertEncodingType*</span><span class="sxs-lookup"><span data-stu-id="e97bc-117">*dwCertEncodingType*</span></span>       | <span data-ttu-id="e97bc-118">Somente o tipo de codificação de certificado é necessário.</span><span class="sxs-lookup"><span data-stu-id="e97bc-118">Only the certificate encoding type is required.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e97bc-119">*dwEncodingType*</span><span class="sxs-lookup"><span data-stu-id="e97bc-119">*dwEncodingType*</span></span>           | <span data-ttu-id="e97bc-120">Um tipo de codificação de mensagem ou de certificado é necessário.</span><span class="sxs-lookup"><span data-stu-id="e97bc-120">Either a message or certificate encoding type is required.</span></span> <span data-ttu-id="e97bc-121">Se a palavra de ordem inferior que contém o tipo de codificação de certificado for diferente de zero, ela será usada.</span><span class="sxs-lookup"><span data-stu-id="e97bc-121">If the low-order word containing the certificate encoding type is nonzero, then it is used.</span></span> <span data-ttu-id="e97bc-122">Caso contrário, a palavra de ordem superior que contém o tipo de codificação de mensagem será usada.</span><span class="sxs-lookup"><span data-stu-id="e97bc-122">Otherwise, the high-order word containing the message encoding type is used.</span></span> <span data-ttu-id="e97bc-123">Se ambos forem especificados, o tipo de codificação de certificado na palavra de ordem inferior será usado.</span><span class="sxs-lookup"><span data-stu-id="e97bc-123">If both are specified, the certificate encoding type in the low-order word is used.</span></span> |



 

<span data-ttu-id="e97bc-124">Os tipos de codificação atualmente definidos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e97bc-124">Currently defined encoding types are shown in the following table.</span></span>



| <span data-ttu-id="e97bc-125">Tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="e97bc-125">Encoding type</span></span>          | <span data-ttu-id="e97bc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e97bc-126">Value</span></span>      |
|------------------------|------------|
| <span data-ttu-id="e97bc-127">\_codificação ASN \_ cript</span><span class="sxs-lookup"><span data-stu-id="e97bc-127">CRYPT\_ASN\_ENCODING</span></span>   | <span data-ttu-id="e97bc-128">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e97bc-128">0x00000001</span></span> |
| <span data-ttu-id="e97bc-129">\_Codificação ASN \_ X509</span><span class="sxs-lookup"><span data-stu-id="e97bc-129">X509\_ASN\_ENCODING</span></span>    | <span data-ttu-id="e97bc-130">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e97bc-130">0x00000001</span></span> |
| <span data-ttu-id="e97bc-131">\_ \_ Codificação ASN do PKCS 7 \_</span><span class="sxs-lookup"><span data-stu-id="e97bc-131">PKCS\_7\_ASN\_ENCODING</span></span> | <span data-ttu-id="e97bc-132">0x00010000</span><span class="sxs-lookup"><span data-stu-id="e97bc-132">0x00010000</span></span> |



 

 

 
