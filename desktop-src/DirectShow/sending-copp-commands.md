---
description: Enviando comandos COPP
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Enviando comandos COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105778426"
---
# <a name="sending-copp-commands"></a>Enviando comandos COPP

Para enviar um comando de COPP (protocolo de proteção de saída) certificado, preencha uma estrutura [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) da seguinte maneira:

-   **guidCommandID**. O GUID que identifica o comando. Consulte a referência de comando COPP.
-   **dwSequence**. O número de sequência do comando. Incrementar esse valor após cada comando. (Esse valor é mostrado como **uCommandSeq** no [início de uma sessão Copp](initiating-a-copp-session.md).)
-   **cbSizeData**. O tamanho, em bytes, de todos os dados necessários para o comando.
-   **CommandData**. Dados para o comando.

Depois de preencher esses dados, calcule o MAC para o comando:

1.  Calcule a marca OMAC-1 para o bloco de dados que aparece após o membro **macKDI** da estrutura **AMCOPPCommand** .
2.  Copie esse valor para o membro **macKDI** da estrutura.

Agora, passe a estrutura para o método [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



