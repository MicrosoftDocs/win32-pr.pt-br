---
description: Conecte-se e comunique-se com um cartão inteligente específico.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Funções de acesso de cartão inteligente e leitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755322"
---
# <a name="smart-card-and-reader-access-functions"></a><span data-ttu-id="a870e-103">Funções de acesso de cartão inteligente e leitor</span><span class="sxs-lookup"><span data-stu-id="a870e-103">Smart Card and Reader Access Functions</span></span>

<span data-ttu-id="a870e-104">As funções a seguir se conectam e se comunicam com um [*cartão inteligente*](../secgloss/s-gly.md)específico.</span><span class="sxs-lookup"><span data-stu-id="a870e-104">The following functions connect to and communicate with a specific [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="a870e-105">As operações de e/s para o cartão usam um buffer para enviar ou receber dados e uma estrutura que contém informações de controle de protocolo.</span><span class="sxs-lookup"><span data-stu-id="a870e-105">I/O operations to the card use a buffer for sending or receiving data and a structure that contains protocol control information.</span></span> <span data-ttu-id="a870e-106">A estrutura de informações de controle de protocolo sempre começa com uma estrutura de [**\_ \_ solicitação de e/s scartar**](scard-io-request.md) .</span><span class="sxs-lookup"><span data-stu-id="a870e-106">The protocol control information structure always begins with an [**SCARD\_IO\_REQUEST**](scard-io-request.md) structure.</span></span>



| <span data-ttu-id="a870e-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="a870e-107">Topic</span></span>                                                  | <span data-ttu-id="a870e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a870e-108">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a870e-109">**SCardConnect**</span><span class="sxs-lookup"><span data-stu-id="a870e-109">**SCardConnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | <span data-ttu-id="a870e-110">Conecte-se a um cartão.</span><span class="sxs-lookup"><span data-stu-id="a870e-110">Connect to a card.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="a870e-111">**SCardReconnect**</span><span class="sxs-lookup"><span data-stu-id="a870e-111">**SCardReconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | <span data-ttu-id="a870e-112">Restabelecer uma conexão.</span><span class="sxs-lookup"><span data-stu-id="a870e-112">Reestablish a connection.</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="a870e-113">**SCardDisconnect**</span><span class="sxs-lookup"><span data-stu-id="a870e-113">**SCardDisconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | <span data-ttu-id="a870e-114">Encerrar uma conexão.</span><span class="sxs-lookup"><span data-stu-id="a870e-114">Terminate a connection.</span></span>                                                                                                                                                                                                                    |
| [<span data-ttu-id="a870e-115">**SCardBeginTransaction**</span><span class="sxs-lookup"><span data-stu-id="a870e-115">**SCardBeginTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | <span data-ttu-id="a870e-116">Inicie uma [*transação*](../secgloss/t-gly.md), impedindo que outros aplicativos acessem um cartão.</span><span class="sxs-lookup"><span data-stu-id="a870e-116">Start a [*transaction*](../secgloss/t-gly.md), blocking other applications from accessing a card.</span></span>                                                                                            |
| [<span data-ttu-id="a870e-117">**SCardEndTransaction**</span><span class="sxs-lookup"><span data-stu-id="a870e-117">**SCardEndTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | <span data-ttu-id="a870e-118">Encerrar uma transação, permitindo que outros aplicativos acessem um cartão.</span><span class="sxs-lookup"><span data-stu-id="a870e-118">End a transaction, allowing other applications to access a card.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="a870e-119">**SCardStatus**</span><span class="sxs-lookup"><span data-stu-id="a870e-119">**SCardStatus**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | <span data-ttu-id="a870e-120">Forneça o status atual do leitor.</span><span class="sxs-lookup"><span data-stu-id="a870e-120">Provide the current status of the reader.</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="a870e-121">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="a870e-121">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | <span data-ttu-id="a870e-122">Solicita o serviço e recebe dados de volta de um cartão usando [*T = 0*](../secgloss/t-gly.md), [*T = 1*](../secgloss/t-gly.md)e protocolos brutos.</span><span class="sxs-lookup"><span data-stu-id="a870e-122">Requests service and receives data back from a card using [*T=0*](../secgloss/t-gly.md), [*T=1*](../secgloss/t-gly.md), and raw protocols.</span></span> |



 

 

 
