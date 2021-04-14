---
description: O Schannel usa o CryptoAPI para operações criptográficas, como armazenar chaves públicas/privadas.
ms.assetid: 5ad9a171-5f69-4035-aac5-ae8d27d0abfb
title: Schannel e CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0684cd690911444b77ba27d2876e578fd71c73a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370569"
---
# <a name="schannel-and-cryptoapi"></a><span data-ttu-id="bbd7b-103">Schannel e CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="bbd7b-103">Schannel and CryptoAPI</span></span>

<span data-ttu-id="bbd7b-104">O Schannel usa o [CryptoAPI](../seccrypto/cryptography-essentials.md) para operações criptográficas, como armazenar [*chaves públicas/privadas*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bbd7b-104">Schannel uses [CryptoAPI](../seccrypto/cryptography-essentials.md) for cryptographic operations such as storing [*public/private keys*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="bbd7b-105">Os tópicos a seguir fornecem informações detalhadas sobre como o Schannel utiliza o CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-105">The following topics provide detailed information about how Schannel makes use of CryptoAPI.</span></span>



| <span data-ttu-id="bbd7b-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="bbd7b-106">Topic</span></span>                                                                   | <span data-ttu-id="bbd7b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbd7b-107">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbd7b-108">Repositórios de certificados</span><span class="sxs-lookup"><span data-stu-id="bbd7b-108">Certificate Stores</span></span>](certificate-stores.md)<br/>                 | <span data-ttu-id="bbd7b-109">Os certificados de cliente e de servidor devem ser armazenados em um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-109">Both client and server certificates must be stored in a certificate store.</span></span><br/>                                |
| [<span data-ttu-id="bbd7b-110">CryptoAPI 2.0 chaves privadas</span><span class="sxs-lookup"><span data-stu-id="bbd7b-110">CryptoAPI 2.0 Private Keys</span></span>](cryptoapi-2-0-private-keys.md)<br/> | <span data-ttu-id="bbd7b-111">As credenciais Schannel são representadas internamente como estruturas de [**\_ contexto de certificado**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="bbd7b-111">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span><br/> |



 

 

 
