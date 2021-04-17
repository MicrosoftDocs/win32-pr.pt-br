---
description: O protocolo de registro de segurança de camada de transporte (TLS) protege os dados do aplicativo usando as chaves criadas durante o handshake.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: Protocolo de registro TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a53d41ad73dc9e1338f0cbff1bec5d6cd6a55e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748957"
---
# <a name="tls-record-protocol"></a><span data-ttu-id="45f19-103">Protocolo de registro TLS</span><span class="sxs-lookup"><span data-stu-id="45f19-103">TLS Record Protocol</span></span>

<span data-ttu-id="45f19-104">O protocolo de registro de [*segurança de camada de transporte*](../secgloss/t-gly.md) (TLS) protege os dados do aplicativo usando as chaves criadas durante o [handshake](tls-handshake-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="45f19-104">The [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) Record protocol secures application data using the keys created during the [Handshake](tls-handshake-protocol.md).</span></span> <span data-ttu-id="45f19-105">O protocolo de registro é responsável por proteger os dados do aplicativo e verificar sua [*integridade*](../secgloss/i-gly.md) e origem.</span><span class="sxs-lookup"><span data-stu-id="45f19-105">The Record Protocol is responsible for securing application data and verifying its [*integrity*](../secgloss/i-gly.md) and origin.</span></span> <span data-ttu-id="45f19-106">Ele gerencia o seguinte:</span><span class="sxs-lookup"><span data-stu-id="45f19-106">It manages the following:</span></span>

-   <span data-ttu-id="45f19-107">Divisão de mensagens de saída em blocos gerenciáveis e remontagem de mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="45f19-107">Dividing outgoing messages into manageable blocks, and reassembling incoming messages.</span></span>
-   <span data-ttu-id="45f19-108">Compactação de blocos de saída e descompressão de blocos de entrada (opcional).</span><span class="sxs-lookup"><span data-stu-id="45f19-108">Compressing outgoing blocks and decompressing incoming blocks (optional).</span></span>
-   <span data-ttu-id="45f19-109">Aplicar um [*Message Authentication Code*](../secgloss/m-gly.md) (Mac) a mensagens de saída e verificar as mensagens de entrada usando o Mac.</span><span class="sxs-lookup"><span data-stu-id="45f19-109">Applying a [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) to outgoing messages, and verifying incoming messages using the MAC.</span></span>
-   <span data-ttu-id="45f19-110">Criptografar mensagens de saída e descriptografar mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="45f19-110">Encrypting outgoing messages and decrypting incoming messages.</span></span>

<span data-ttu-id="45f19-111">Quando o protocolo de registro é concluído, os dados criptografados de saída são passados para a camada TCP (Transmission Control Protocol) para transporte.</span><span class="sxs-lookup"><span data-stu-id="45f19-111">When the Record Protocol is complete, the outgoing encrypted data is passed down to the Transmission Control Protocol (TCP) layer for transport.</span></span>

 

 
