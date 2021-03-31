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
# <a name="sending-copp-status-requests"></a>Enviando solicitações de status COPP

Para enviar uma solicitação de status de COPP (protocolo de proteção de saída) certificada, preencha uma estrutura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) com os dados de solicitação. Os membros da estrutura são:

-   **rApp**. Um número aleatório de 128 bits, digitado como um GUID. O mesmo número é retornado na resposta do driver. Você deve alocar o número aleatório no heap e, em seguida, copiá-lo para a estrutura. Isso protege contra ataques em que o invasor modifica o conteúdo da estrutura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) .
-   **guidStatusRequestID**. Um GUID que identifica a solicitação. Consulte [referência de consulta Copp](copp-query-reference.md).
-   **dwSequence**. O número de sequência de status. Incrementar esse valor após cada solicitação de status. (Na seção [iniciando uma sessão Copp](initiating-a-copp-session.md), esse valor é mostrado como *uStatusSeq* nos exemplos de código.)
-   **cbSizeData**. O tamanho, em bytes, de quaisquer dados adicionais necessários para a solicitação.
-   **StatusData**. Dados para a solicitação de status.

Passe a estrutura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) para o método [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) . Por exemplo, o código a seguir envia uma solicitação de status que consulta quais mecanismos de proteção estão disponíveis:


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



A resposta é gravada no membro **COPPStatus** da estrutura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) . O tamanho dos dados válidos na resposta é fornecido no membro **cbSizeData** . Para garantir a integridade da mensagem, o driver computa um MAC (código de autenticação de mensagem) usando o algoritmo OMAC 1 e retorna esse valor no membro **macKDI** da estrutura. O aplicativo deve verificar esse valor da seguinte maneira:

1.  Calcule a marca OMAC para o bloco de dados que aparece após o membro **macKDI** da estrutura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (em outras palavras, **cbSizeData** Plus **COPPStatus**).
2.  Compare essa marca com o valor em **macKDI**, usando um **memcmp** reto.

O algoritmo OMAC 1 é descrito em detalhes em [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) . A COPP usa os seguintes parâmetros OMAC-1:

-   E = AES
-   t = 128 bits

Os dados retornados da solicitação de status sempre começam com dois itens:

-   O mesmo valor de **rApp** que foi passado pelo aplicativo. Você deve verificar se esse valor corresponde ao valor original armazenado no heap.
-   Um [**valor \_ StatusFlags Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) que indica se o status da proteção de saída foi alterado.

Como a conexão pode ser perdida ou reconfigurada, o aplicativo deve sondar periodicamente o driver para o status atual. Se o \_ sinalizador RENEGOTIATIONREQUIRED Copp for definido, o aplicativo deverá tentar redefinir o nível de proteção. Se o \_ sinalizador LINKLOST Copp for definido, o aplicativo deverá parar de reproduzir o conteúdo. Por exemplo, o \_ sinalizador de LINKLOST Copp pode ser retornado porque o usuário desconectou o conector de saída. O aplicativo deve liberar a instância atual do VMR, criar uma nova instância do VMR e estabelecer uma nova sessão COPP (incluindo a troca de chaves e a validação de certificado).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



