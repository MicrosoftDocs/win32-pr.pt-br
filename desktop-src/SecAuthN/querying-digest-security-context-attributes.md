---
description: A função QueryContextAttributes (Digest) fornece informações sobre as configurações atuais de um contexto de segurança.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Consultando atributos de contexto de segurança de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921625"
---
# <a name="querying-digest-security-context-attributes"></a><span data-ttu-id="26863-103">Consultando atributos de contexto de segurança de resumo</span><span class="sxs-lookup"><span data-stu-id="26863-103">Querying Digest Security Context Attributes</span></span>

<span data-ttu-id="26863-104">A função [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) fornece informações sobre as configurações atuais de um [*contexto de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="26863-104">The [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) function provides information about the current settings of a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="26863-105">Microsoft Digest dá suporte à consulta dos seguintes atributos de contexto de segurança.</span><span class="sxs-lookup"><span data-stu-id="26863-105">Microsoft Digest supports querying the following security context attributes.</span></span>



| <span data-ttu-id="26863-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="26863-106">Attribute</span></span>                   | <span data-ttu-id="26863-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="26863-107">Description</span></span>                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26863-108">\_informações da \_ chave \_ attr SECPKG</span><span class="sxs-lookup"><span data-stu-id="26863-108">SECPKG\_ATTR\_KEY\_INFO</span></span>     | <span data-ttu-id="26863-109">Informações relacionadas aos algoritmos de assinatura e criptografia em uso.</span><span class="sxs-lookup"><span data-stu-id="26863-109">Information relating to the signing and encryption algorithms in use.</span></span>                                                                                                                                   |
| <span data-ttu-id="26863-110">\_informações do \_ pacote \_ attr SECPKG</span><span class="sxs-lookup"><span data-stu-id="26863-110">SECPKG\_ATTR\_PACKAGE\_INFO</span></span> | <span data-ttu-id="26863-111">Informações gerais referentes a Microsoft Digest, como o tamanho máximo de token permitido pelo [*pacote de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="26863-111">General information pertaining to Microsoft Digest, such as the maximum token size permitted by the [*security package*](../secgloss/s-gly.md).</span></span> |
| <span data-ttu-id="26863-112">\_tamanhos de attr SECPKG \_</span><span class="sxs-lookup"><span data-stu-id="26863-112">SECPKG\_ATTR\_SIZES</span></span>         | <span data-ttu-id="26863-113">Os tamanhos máximos permitidos para dados relacionados à mensagem, como assinaturas.</span><span class="sxs-lookup"><span data-stu-id="26863-113">The maximum sizes permitted for message-related data such as signatures.</span></span>                                                                                                                                |



 

 

 
