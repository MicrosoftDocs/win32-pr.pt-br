---
description: Enviando solicitações de status COPP
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: Enviando solicitações de status COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5494b0e856df573bdbfc9b1554ab82be206a95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645628"
---
# <a name="sending-copp-status-requests"></a><span data-ttu-id="96bb3-103">Enviando solicitações de status COPP</span><span class="sxs-lookup"><span data-stu-id="96bb3-103">Sending COPP Status Requests</span></span>

<span data-ttu-id="96bb3-104">Para enviar uma solicitação de status de COPP (protocolo de proteção de saída) certificada, preencha uma estrutura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) com os dados de solicitação.</span><span class="sxs-lookup"><span data-stu-id="96bb3-104">To send a Certified Output Protection Protocol (COPP) status request, fill in an [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure with the request data.</span></span> <span data-ttu-id="96bb3-105">Os membros da estrutura são:</span><span class="sxs-lookup"><span data-stu-id="96bb3-105">The structure members are:</span></span>

-   <span data-ttu-id="96bb3-106">**rApp**.</span><span class="sxs-lookup"><span data-stu-id="96bb3-106">**rApp**.</span></span> <span data-ttu-id="96bb3-107">Um número aleatório de 128 bits, digitado como um GUID.</span><span class="sxs-lookup"><span data-stu-id="96bb3-107">A 128-bit random number, typed as a GUID.</span></span> <span data-ttu-id="96bb3-108">O mesmo número é retornado na resposta do driver.</span><span class="sxs-lookup"><span data-stu-id="96bb3-108">The same number is returned in the driver's response.</span></span> <span data-ttu-id="96bb3-109">Você deve alocar o número aleatório no heap e, em seguida, copiá-lo para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="96bb3-109">You should allocate the random number on the heap and then copy it into structure.</span></span> <span data-ttu-id="96bb3-110">Isso protege contra ataques em que o invasor modifica o conteúdo da estrutura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) .</span><span class="sxs-lookup"><span data-stu-id="96bb3-110">This guards against attacks where the attacker modifies the contents of the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure.</span></span>
-   <span data-ttu-id="96bb3-111">**guidStatusRequestID**.</span><span class="sxs-lookup"><span data-stu-id="96bb3-111">**guidStatusRequestID**.</span></span> <span data-ttu-id="96bb3-112">Um GUID que identifica a solicitação.</span><span class="sxs-lookup"><span data-stu-id="96bb3-112">A GUID that identifies the request.</span></span> <span data-ttu-id="96bb3-113">Consulte [referência de consulta Copp](copp-query-reference.md).</span><span class="sxs-lookup"><span data-stu-id="96bb3-113">See [COPP Query Reference](copp-query-reference.md).</span></span>
-   <span data-ttu-id="96bb3-114">**dwSequence**.</span><span class="sxs-lookup"><span data-stu-id="96bb3-114">**dwSequence**.</span></span> <span data-ttu-id="96bb3-115">O número de sequência de status.</span><span class="sxs-lookup"><span data-stu-id="96bb3-115">The status sequence number.</span></span> <span data-ttu-id="96bb3-116">Incrementar esse valor após cada solicitação de status.</span><span class="sxs-lookup"><span data-stu-id="96bb3-116">Increment this value after each status request.</span></span> <span data-ttu-id="96bb3-117">(Na seção [iniciando uma sessão Copp](initiating-a-copp-session.md), esse valor é mostrado como *uStatusSeq* nos exemplos de código.)</span><span class="sxs-lookup"><span data-stu-id="96bb3-117">(In the section [Initiating a COPP Session](initiating-a-copp-session.md), this value is shown as *uStatusSeq* in the code examples.)</span></span>
-   <span data-ttu-id="96bb3-118">**cbSizeData**.</span><span class="sxs-lookup"><span data-stu-id="96bb3-118">**cbSizeData**.</span></span> <span data-ttu-id="96bb3-119">O tamanho, em bytes, de quaisquer dados adicionais necessários para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="96bb3-119">The size, in bytes, of any additional data needed for the request.</span></span>
-   <span data-ttu-id="96bb3-120">**StatusData**.</span><span class="sxs-lookup"><span data-stu-id="96bb3-120">**StatusData**.</span></span> <span data-ttu-id="96bb3-121">Dados para a solicitação de status.</span><span class="sxs-lookup"><span data-stu-id="96bb3-121">Data for the status request.</span></span>

<span data-ttu-id="96bb3-122">Passe a estrutura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) para o método [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) .</span><span class="sxs-lookup"><span data-stu-id="96bb3-122">Pass the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure to the [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) method.</span></span> <span data-ttu-id="96bb3-123">Por exemplo, o código a seguir envia uma solicitação de status que consulta quais mecanismos de proteção estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="96bb3-123">For example, the following code sends a status request that queries which protection mechanisms are available:</span></span>


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



<span data-ttu-id="96bb3-124">A resposta é gravada no membro **COPPStatus** da estrutura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) .</span><span class="sxs-lookup"><span data-stu-id="96bb3-124">The response is written into the **COPPStatus** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure.</span></span> <span data-ttu-id="96bb3-125">O tamanho dos dados válidos na resposta é fornecido no membro **cbSizeData** .</span><span class="sxs-lookup"><span data-stu-id="96bb3-125">The size of the valid data in the response is given in the **cbSizeData** member.</span></span> <span data-ttu-id="96bb3-126">Para garantir a integridade da mensagem, o driver computa um MAC (código de autenticação de mensagem) usando o algoritmo OMAC 1 e retorna esse valor no membro **macKDI** da estrutura.</span><span class="sxs-lookup"><span data-stu-id="96bb3-126">To ensure the integrity of the message, the driver computes a message authentication code (MAC) using the OMAC 1 algorithm, and returns this value in the structure's **macKDI** member.</span></span> <span data-ttu-id="96bb3-127">O aplicativo deve verificar esse valor da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="96bb3-127">The application should verify this value as follows:</span></span>

1.  <span data-ttu-id="96bb3-128">Calcule a marca OMAC para o bloco de dados que aparece após o membro **macKDI** da estrutura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (em outras palavras, **cbSizeData** Plus **COPPStatus**).</span><span class="sxs-lookup"><span data-stu-id="96bb3-128">Calculate the OMAC tag for the block of data that appears after the **macKDI** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure (in other words, **cbSizeData** plus **COPPStatus**).</span></span>
2.  <span data-ttu-id="96bb3-129">Compare essa marca com o valor em **macKDI**, usando um **memcmp** reto.</span><span class="sxs-lookup"><span data-stu-id="96bb3-129">Compare this tag with the value in **macKDI**, using a straight **memcmp**.</span></span>

<span data-ttu-id="96bb3-130">O algoritmo OMAC 1 é descrito em detalhes em [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) .</span><span class="sxs-lookup"><span data-stu-id="96bb3-130">The OMAC 1 algorithm is described in detail at [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html).</span></span> <span data-ttu-id="96bb3-131">A COPP usa os seguintes parâmetros OMAC-1:</span><span class="sxs-lookup"><span data-stu-id="96bb3-131">COPP uses the following OMAC-1 parameters:</span></span>

-   <span data-ttu-id="96bb3-132">E = AES</span><span class="sxs-lookup"><span data-stu-id="96bb3-132">E = AES</span></span>
-   <span data-ttu-id="96bb3-133">t = 128 bits</span><span class="sxs-lookup"><span data-stu-id="96bb3-133">t = 128 bits</span></span>

<span data-ttu-id="96bb3-134">Os dados retornados da solicitação de status sempre começam com dois itens:</span><span class="sxs-lookup"><span data-stu-id="96bb3-134">The data returned from the status request always starts with two items:</span></span>

-   <span data-ttu-id="96bb3-135">O mesmo valor de **rApp** que foi passado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96bb3-135">The same value of **rApp** that was passed by the application.</span></span> <span data-ttu-id="96bb3-136">Você deve verificar se esse valor corresponde ao valor original armazenado no heap.</span><span class="sxs-lookup"><span data-stu-id="96bb3-136">You should verify that this value matches the original value stored on the heap.</span></span>
-   <span data-ttu-id="96bb3-137">Um [**valor \_ StatusFlags Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) que indica se o status da proteção de saída foi alterado.</span><span class="sxs-lookup"><span data-stu-id="96bb3-137">A [**COPP\_StatusFlags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) value that indicates whether the output protection status has changed.</span></span>

<span data-ttu-id="96bb3-138">Como a conexão pode ser perdida ou reconfigurada, o aplicativo deve sondar periodicamente o driver para o status atual.</span><span class="sxs-lookup"><span data-stu-id="96bb3-138">Because the connection can be lost or reconfigured, the application should periodically poll the driver for the current status.</span></span> <span data-ttu-id="96bb3-139">Se o \_ sinalizador RENEGOTIATIONREQUIRED Copp for definido, o aplicativo deverá tentar redefinir o nível de proteção.</span><span class="sxs-lookup"><span data-stu-id="96bb3-139">If the COPP\_RenegotiationRequired flag is set, the application should attempt to reset the protection level.</span></span> <span data-ttu-id="96bb3-140">Se o \_ sinalizador LINKLOST Copp for definido, o aplicativo deverá parar de reproduzir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="96bb3-140">If the COPP\_LinkLost flag is set, the application should stop playing the content.</span></span> <span data-ttu-id="96bb3-141">Por exemplo, o \_ sinalizador de LINKLOST Copp pode ser retornado porque o usuário desconectou o conector de saída.</span><span class="sxs-lookup"><span data-stu-id="96bb3-141">For example, the COPP\_LinkLost flag can be returned because the user disconnected the output connector.</span></span> <span data-ttu-id="96bb3-142">O aplicativo deve liberar a instância atual do VMR, criar uma nova instância do VMR e estabelecer uma nova sessão COPP (incluindo a troca de chaves e a validação de certificado).</span><span class="sxs-lookup"><span data-stu-id="96bb3-142">The application should release the current instance of the VMR, create a new instance of the VMR, and establish a new COPP session (including key exchange and certificate validation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="96bb3-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96bb3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96bb3-144">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="96bb3-144">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



