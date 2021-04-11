---
description: A mensagem envelopada consiste na mensagem criptografada, nos certificados dos destinatários pretendidos e no conjunto de chaves criptografadas, uma para cada destinatário. A mensagem gerada está no \# formato PKCS 7/CMS.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Criando e recebendo mensagens de dados envelopadas no CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672d56383ac635a295847777c0e557bbe7c40b69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296279"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a><span data-ttu-id="55fc8-104">Criando e recebendo mensagens de dados envelopadas no CAPICOM</span><span class="sxs-lookup"><span data-stu-id="55fc8-104">Creating and Receiving Enveloped Data Messages in CAPICOM</span></span>

<span data-ttu-id="55fc8-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="55fc8-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="55fc8-106">Em vez disso, use o .NET Framework para implementar recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="55fc8-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="55fc8-107">Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="55fc8-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="55fc8-108">Uma mensagem envelopada é uma mensagem criptografada para um conjunto de destinatários.</span><span class="sxs-lookup"><span data-stu-id="55fc8-108">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="55fc8-109">No processo Envelopment, uma chave de criptografia de sessão é gerada e a mensagem é criptografada com essa chave.</span><span class="sxs-lookup"><span data-stu-id="55fc8-109">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="55fc8-110">A chave de criptografia em si é, então, criptografada separadamente para cada destinatário usando as chaves públicas do certificado do destinatário desejado.</span><span class="sxs-lookup"><span data-stu-id="55fc8-110">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="55fc8-111">A mensagem envelopada consiste na mensagem criptografada, nos certificados dos destinatários pretendidos e no conjunto de chaves criptografadas, uma para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="55fc8-111">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="55fc8-112">A mensagem gerada está no \# formato PKCS 7/CMS.</span><span class="sxs-lookup"><span data-stu-id="55fc8-112">The message generated is in PKCS \#7/CMS format.</span></span>

<span data-ttu-id="55fc8-113">As seções a seguir mostram procedimentos e exemplos para tarefas de mensagens envelopadas:</span><span class="sxs-lookup"><span data-stu-id="55fc8-113">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="55fc8-114">Enviando uma mensagem de dados envelopada</span><span class="sxs-lookup"><span data-stu-id="55fc8-114">Sending an Enveloped Data Message</span></span>](sending-an-enveloped-data-message.md)
-   [<span data-ttu-id="55fc8-115">Recebendo uma mensagem de dados envelopada</span><span class="sxs-lookup"><span data-stu-id="55fc8-115">Receiving an Enveloped Data Message</span></span>](receiving-an-enveloped-data-message.md)

 

 



