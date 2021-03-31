---
title: Protocolo de carregamento de BITS
description: Esta seção descreve o protocolo de rede para o upload de BITS e os tipos de trabalho de resposta de upload.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642426decd0bc37390fa9fdd9b1ad2be11a0aa84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635116"
---
# <a name="bits-upload-protocol"></a><span data-ttu-id="514b1-103">Protocolo de carregamento de BITS</span><span class="sxs-lookup"><span data-stu-id="514b1-103">BITS Upload Protocol</span></span>

<span data-ttu-id="514b1-104">Esta seção descreve o protocolo de rede para o upload de BITS e os tipos de trabalho de resposta de upload.</span><span class="sxs-lookup"><span data-stu-id="514b1-104">This section describes the network protocol for BITS upload and upload-reply job types.</span></span> <span data-ttu-id="514b1-105">O protocolo de carregamento BITS é colocado em camadas sobre HTTP 1,1 e usa muitos dos cabeçalhos HTTP existentes e define novos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="514b1-105">The BITS upload protocol is layered on top of HTTP 1.1 and uses many of the existing HTTP headers and defines new headers.</span></span> <span data-ttu-id="514b1-106">O protocolo de carregamento do BITS dá suporte a um único arquivo de carregamento por sessão.</span><span class="sxs-lookup"><span data-stu-id="514b1-106">The BITS upload protocol supports a single upload file per session.</span></span>

<span data-ttu-id="514b1-107">O BITS usa pacotes para descrever solicitações de cliente e respostas do servidor.</span><span class="sxs-lookup"><span data-stu-id="514b1-107">BITS uses packets to describe client requests and server responses.</span></span> <span data-ttu-id="514b1-108">O cabeçalho BITS-pacote-tipo especifica o tipo de pacote que está sendo enviado.</span><span class="sxs-lookup"><span data-stu-id="514b1-108">The BITS-Packet-Type header specifies the type of packet being sent.</span></span> <span data-ttu-id="514b1-109">Cada pacote contém cabeçalhos específicos.</span><span class="sxs-lookup"><span data-stu-id="514b1-109">Each packet contains specific headers.</span></span> <span data-ttu-id="514b1-110">O BITS usa o \_ verbo post do bits para identificar os pacotes de carregamento do bits.</span><span class="sxs-lookup"><span data-stu-id="514b1-110">BITS uses the BITS\_POST verb to identify BITS upload packets.</span></span> <span data-ttu-id="514b1-111">Os pacotes de resposta sempre usam o tipo de pacote ACK, que representa a confirmação.</span><span class="sxs-lookup"><span data-stu-id="514b1-111">Response packets always use the Ack packet type which stands for acknowledge.</span></span> <span data-ttu-id="514b1-112">O pacote ACK é enviado no contexto da solicitação anterior; pode haver apenas uma solicitação pendente ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="514b1-112">The Ack packet is sent in the context of the previous request; there can be only one outstanding request at one time.</span></span>

<span data-ttu-id="514b1-113">Para trabalhos de resposta de upload, o BITS usa esse protocolo para carregar o arquivo, mas não usa esse protocolo para enviar a resposta ao cliente.</span><span class="sxs-lookup"><span data-stu-id="514b1-113">For upload-reply jobs, BITS uses this protocol to upload the file but does not use this protocol to send the reply to the client.</span></span> <span data-ttu-id="514b1-114">Em vez disso, o servidor BITS envia o local do arquivo de resposta para o cliente e o cliente cria um trabalho de download do BITS para baixar o arquivo de resposta.</span><span class="sxs-lookup"><span data-stu-id="514b1-114">Instead, the BITS server sends the location of the reply file to the client and the client creates a BITS download job to download the reply file.</span></span>

<span data-ttu-id="514b1-115">Use o protocolo de upload para substituir o cliente BITS ou o software de servidor pela sua própria implementação.</span><span class="sxs-lookup"><span data-stu-id="514b1-115">Use the upload protocol to replace the BITS client or server software with your own implementation.</span></span> <span data-ttu-id="514b1-116">Para obter uma lista de pacotes de solicitação enviados pelo cliente BITS, consulte [pacotes de solicitação do bits](bits-request-packets.md).</span><span class="sxs-lookup"><span data-stu-id="514b1-116">For a list of request packets sent by the BITS client, see [BITS Request Packets](bits-request-packets.md).</span></span> <span data-ttu-id="514b1-117">Para obter uma lista de pacotes de resposta enviados pelo servidor BITS, consulte [pacotes de resposta do bits](bits-response-packets.md).</span><span class="sxs-lookup"><span data-stu-id="514b1-117">For a list of response packets sent by the BITS server, see [BITS Response Packets](bits-response-packets.md).</span></span>

<span data-ttu-id="514b1-118">O cliente determina como ele responde a erros ou a pacotes inesperados do servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="514b1-118">The client determines how it responds to errors or unexpected packets from the BITS server.</span></span> <span data-ttu-id="514b1-119">Se o servidor receber um pacote que não espera, o servidor deverá enviar um pacote ACK com um código de retorno 400 (solicitação inválida).</span><span class="sxs-lookup"><span data-stu-id="514b1-119">If the server receives a packet that it does not expect, the server should send an Ack packet with a 400 (Bad Request) return code.</span></span>

 

 




