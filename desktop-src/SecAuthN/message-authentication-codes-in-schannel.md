---
description: Um Message Authentication Code (MAC) é usado para detectar violação e falsificação de mensagens.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Códigos de autenticação de mensagens no Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170812"
---
# <a name="message-authentication-codes-in-schannel"></a><span data-ttu-id="a5d6f-103">Códigos de autenticação de mensagens no Schannel</span><span class="sxs-lookup"><span data-stu-id="a5d6f-103">Message Authentication Codes in Schannel</span></span>

<span data-ttu-id="a5d6f-104">Um [*Message Authentication Code*](../secgloss/m-gly.md) (Mac) é usado para detectar violação e falsificação de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a5d6f-104">A [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) is used to detect message tampering and forgery.</span></span> <span data-ttu-id="a5d6f-105">O remetente de uma mensagem cria um MAC criptografando um [*hash*](../secgloss/h-gly.md) unidirecional do corpo da mensagem usando uma [*chave de sessão*](../secgloss/s-gly.md) compartilhada pelo remetente e pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="a5d6f-105">The sender of a message creates a MAC by encrypting a one-way [*hash*](../secgloss/h-gly.md) of the message body using a [*session key*](../secgloss/s-gly.md) shared by sender and recipient.</span></span> <span data-ttu-id="a5d6f-106">O MAC é anexado à mensagem que é enviada ao destinatário.</span><span class="sxs-lookup"><span data-stu-id="a5d6f-106">The MAC is appended to the message that is sent to the recipient.</span></span> <span data-ttu-id="a5d6f-107">O destinatário da mensagem gera o MAC novamente, usando a chave de sessão compartilhada e o corpo da mensagem e compara o MAC gerado com o MAC recebido do remetente.</span><span class="sxs-lookup"><span data-stu-id="a5d6f-107">The message recipient generates the MAC again, using the shared session key and message body, and compares the generated MAC to the MAC received from the sender.</span></span> <span data-ttu-id="a5d6f-108">Se os dois forem idênticos, o remetente deverá ter a chave de sessão compartilhada e a mensagem não foi alterada em trânsito.</span><span class="sxs-lookup"><span data-stu-id="a5d6f-108">If the two are identical, then the sender must have the shared session key, and the message has not been altered in transit.</span></span>

<span data-ttu-id="a5d6f-109">Em protocolos Schannel, o algoritmo usado para gerar o MAC é determinado pelo [conjunto de codificação](cipher-suites-in-schannel.md) em uso pelo remetente e pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="a5d6f-109">In Schannel protocols, the algorithm used to generate the MAC is determined by the [cipher suite](cipher-suites-in-schannel.md) in use by the sender and recipient.</span></span>

 

 
