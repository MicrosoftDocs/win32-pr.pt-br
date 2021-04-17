---
description: Lista as alterações para os recursos de dados do enveloping.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Adições de dados envelopadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770349"
---
# <a name="enveloped-data-additions"></a><span data-ttu-id="0296f-103">Adições de dados envelopadas</span><span class="sxs-lookup"><span data-stu-id="0296f-103">Enveloped Data Additions</span></span>

<span data-ttu-id="0296f-104">As seguintes alterações foram feitas em recursos de dados envelopos:</span><span class="sxs-lookup"><span data-stu-id="0296f-104">The following changes have been made to enveloped data capabilities:</span></span>

-   <span data-ttu-id="0296f-105">A identificação do destinatário pode ser feita não apenas pelo emissor e número de série (PKCS \# 7 1,5), mas também pelo identificador de chave.</span><span class="sxs-lookup"><span data-stu-id="0296f-105">Recipient identification can be done not only by Issuer and Serial Number (PKCS \#7 1.5), but also by Key Identifier.</span></span>
-   <span data-ttu-id="0296f-106">Três opções de troca de chave de destinatário são fornecidas:</span><span class="sxs-lookup"><span data-stu-id="0296f-106">Three recipient key exchange choices are provided:</span></span>
    -   <span data-ttu-id="0296f-107">Transporte de chave usando chaves RSA.</span><span class="sxs-lookup"><span data-stu-id="0296f-107">Key Transport using RSA keys.</span></span>
    -   <span data-ttu-id="0296f-108">O acordo de chave usando Ephemeral-Static Diffie-Hellman chaves de algoritmo encapsuladas com 3DES ou RC2, ou Ephemeral-Static curva elíptica Diffie-Hellman chaves de algoritmo encapsuladas com AES.</span><span class="sxs-lookup"><span data-stu-id="0296f-108">Key Agreement using either Ephemeral-Static Diffie-Hellman algorithm keys wrapped with 3DES or RC2, or Ephemeral-Static Elliptic Curve Diffie-Hellman algorithm keys wrapped with AES.</span></span>
    -   <span data-ttu-id="0296f-109">Chave de criptografia de chave ou transferência de chave de lista de mensagens em que a chave usada para criptografar a chave de criptografia de conteúdo já foi distribuída para os destinatários.</span><span class="sxs-lookup"><span data-stu-id="0296f-109">Key Encryption Key or Mail List key transfer where the key used to encrypt the content encryption key has already been distributed to the recipients.</span></span> <span data-ttu-id="0296f-110">RC2, 3DES e AES são permitidos como algoritmos de encapsulamento de chaves.</span><span class="sxs-lookup"><span data-stu-id="0296f-110">RC2, 3DES and AES are allowed as key-wrapping algorithms.</span></span>
-   <span data-ttu-id="0296f-111">Os atributos não protegidos podem ser incluídos na mensagem.</span><span class="sxs-lookup"><span data-stu-id="0296f-111">Unprotected attributes can be included in the message.</span></span>
-   <span data-ttu-id="0296f-112">Um campo **OriginatorInfo** que contém informações sobre o originador foi adicionado que pode conter certificados e CRLs.</span><span class="sxs-lookup"><span data-stu-id="0296f-112">An **OriginatorInfo** field that contains information about the originator has been added that can contain certificates and CRLs.</span></span>
-   <span data-ttu-id="0296f-113">Algoritmos baseados em ECC (criptografia de curva elíptica) e AES exigem o Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0296f-113">Elliptic Curve Cryptography (ECC) based algorithms and AES require Windows Vista or later.</span></span>

 

 



