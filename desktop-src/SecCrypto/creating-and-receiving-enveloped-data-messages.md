---
description: Uma mensagem envelopada é uma mensagem criptografada para um destinatário ou conjunto de destinatários.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Criando e recebendo mensagens de dados envelopadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d973ded4656966d1b61ac0ae9779acf35eb578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811288"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a><span data-ttu-id="2aec3-103">Criando e recebendo mensagens de dados envelopadas</span><span class="sxs-lookup"><span data-stu-id="2aec3-103">Creating and Receiving Enveloped Data Messages</span></span>

<span data-ttu-id="2aec3-104">Uma mensagem envelopada é uma mensagem criptografada para um conjunto de destinatários.</span><span class="sxs-lookup"><span data-stu-id="2aec3-104">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="2aec3-105">No processo Envelopment, uma chave de criptografia de sessão é gerada e a mensagem é criptografada com essa chave.</span><span class="sxs-lookup"><span data-stu-id="2aec3-105">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="2aec3-106">A chave de criptografia em si é, então, criptografada separadamente para cada destinatário usando as chaves públicas do certificado do destinatário desejado.</span><span class="sxs-lookup"><span data-stu-id="2aec3-106">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="2aec3-107">A mensagem envelopada consiste na mensagem criptografada, nos certificados dos destinatários pretendidos e no conjunto de chaves criptografadas, uma para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="2aec3-107">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="2aec3-108">A mensagem gerada está no formato/CMS [*PKCS \# 7*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2aec3-108">The message generated is in [*PKCS \#7*](../secgloss/p-gly.md)/CMS format.</span></span>

<span data-ttu-id="2aec3-109">As seções a seguir mostram procedimentos e exemplos para tarefas de mensagens envelopadas:</span><span class="sxs-lookup"><span data-stu-id="2aec3-109">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="2aec3-110">Codificando dados Envelopos</span><span class="sxs-lookup"><span data-stu-id="2aec3-110">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)
-   [<span data-ttu-id="2aec3-111">Decodificando dados envelopado</span><span class="sxs-lookup"><span data-stu-id="2aec3-111">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)
-   [<span data-ttu-id="2aec3-112">Código alternativo para codificar uma mensagem envelopada</span><span class="sxs-lookup"><span data-stu-id="2aec3-112">Alternate Code for Encoding an Enveloped Message</span></span>](alternate-code-for-encoding-an-enveloped-message.md)
-   [<span data-ttu-id="2aec3-113">Programa C de exemplo: codificando uma mensagem envelopada e assinada</span><span class="sxs-lookup"><span data-stu-id="2aec3-113">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
