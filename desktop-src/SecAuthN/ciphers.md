---
description: O material a seguir é válido somente quando Digest é usado como um mecanismo SASL. Codificações e criptografia não estão disponíveis para autenticação HTTP usando Microsoft Digest.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Criptografias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165236"
---
# <a name="ciphers"></a><span data-ttu-id="d8a0b-104">Criptografias</span><span class="sxs-lookup"><span data-stu-id="d8a0b-104">Ciphers</span></span>

<span data-ttu-id="d8a0b-105">O material a seguir é válido somente quando Digest é usado como um mecanismo SASL.</span><span class="sxs-lookup"><span data-stu-id="d8a0b-105">The following material is valid only when Digest is used as a SASL mechanism.</span></span> <span data-ttu-id="d8a0b-106">Codificações e criptografia não estão disponíveis para autenticação HTTP usando Microsoft Digest.</span><span class="sxs-lookup"><span data-stu-id="d8a0b-106">Ciphers and encryption are not available for HTTP authentication using Microsoft Digest.</span></span>

<span data-ttu-id="d8a0b-107">A diretiva de codificação de um desafio do Digest SASL contém uma lista das codificações com suporte de um servidor que exige comunicações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="d8a0b-107">A Digest SASL challenge's cipher directive contains a list of the ciphers supported by a server that requires confidential communications.</span></span> <span data-ttu-id="d8a0b-108">A diretiva Cipher só poderá ser incluída se a diretiva QoP estiver definida como "auth-conf".</span><span class="sxs-lookup"><span data-stu-id="d8a0b-108">The cipher directive can only be included if the qop directive is set to "auth-conf".</span></span> <span data-ttu-id="d8a0b-109">As codificações reconhecidas pelo Microsoft Digest estão listadas na tabela a seguir, de forma mais forte para mais fraca.</span><span class="sxs-lookup"><span data-stu-id="d8a0b-109">The ciphers recognized by Microsoft Digest are listed in the following table, in order from strongest to weakest.</span></span>



| <span data-ttu-id="d8a0b-110">Valor de codificação</span><span class="sxs-lookup"><span data-stu-id="d8a0b-110">Cipher value</span></span> | <span data-ttu-id="d8a0b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8a0b-111">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a0b-112">RC4</span><span class="sxs-lookup"><span data-stu-id="d8a0b-112">"rc4"</span></span>        | <span data-ttu-id="d8a0b-113">A codificação RC4 com uma chave de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="d8a0b-113">The RC4 cipher with a 128-bit key.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="d8a0b-114">3DES</span><span class="sxs-lookup"><span data-stu-id="d8a0b-114">"3des"</span></span>       | <span data-ttu-id="d8a0b-115">O [*Triple DES*](/windows/desktop/SecGloss/t-gly) Cipher no modo [*CBC*](/windows/desktop/SecGloss/c-gly) com ede com a mesma chave para cada estágio E (modo de duas chaves).</span><span class="sxs-lookup"><span data-stu-id="d8a0b-115">The [*triple DES*](/windows/desktop/SecGloss/t-gly) cipher in [*CBC*](/windows/desktop/SecGloss/c-gly) mode with EDE with the same key for each E stage (two keys mode).</span></span> <span data-ttu-id="d8a0b-116">O comprimento total da chave é de 112 bits.</span><span class="sxs-lookup"><span data-stu-id="d8a0b-116">Total key length is 112 bits.</span></span> |
| <span data-ttu-id="d8a0b-117">"RC4-56"</span><span class="sxs-lookup"><span data-stu-id="d8a0b-117">"rc4-56"</span></span>     | <span data-ttu-id="d8a0b-118">A codificação RC4 com uma chave de 56 bits.</span><span class="sxs-lookup"><span data-stu-id="d8a0b-118">The RC4 cipher with a 56-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d8a0b-119">"RC4-40"</span><span class="sxs-lookup"><span data-stu-id="d8a0b-119">"rc4-40"</span></span>     | <span data-ttu-id="d8a0b-120">A codificação RC4 com uma chave de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="d8a0b-120">The RC4 cipher with a 40-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d8a0b-121">des</span><span class="sxs-lookup"><span data-stu-id="d8a0b-121">"des"</span></span>        | <span data-ttu-id="d8a0b-122">A criptografia des ( [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) ) no modo CBC ( [*encadeamento de blocos de codificação*](/windows/desktop/SecGloss/c-gly) ) com uma chave de 56 bits.</span><span class="sxs-lookup"><span data-stu-id="d8a0b-122">The [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) (DES) cipher in [*cipher block chaining*](/windows/desktop/SecGloss/c-gly) (CBC) mode with a 56-bit key.</span></span> |



 

<span data-ttu-id="d8a0b-123">Quando um aplicativo de servidor solicita confidencialidade (QoP = "auth-conf") Microsoft Digest gerará um desafio que oferece ao cliente todas as codificações instaladas no servidor e com suporte do resumo.</span><span class="sxs-lookup"><span data-stu-id="d8a0b-123">When a server application requests confidentiality (qop="auth-conf") Microsoft Digest will generate a challenge that offers the client all of the ciphers installed on the server and supported by Digest.</span></span> <span data-ttu-id="d8a0b-124">O cliente Digest selecionará a codificação mais forte disponível.</span><span class="sxs-lookup"><span data-stu-id="d8a0b-124">The Digest client will select the strongest available cipher.</span></span> <span data-ttu-id="d8a0b-125">Para obter detalhes sobre como especificar a confidencialidade, consulte [gerando o desafio Digest](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="d8a0b-125">For details on specifying confidentiality, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 
