---
description: Enviando comandos COPP
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Enviando comandos COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66a6ad66abe7e6c4a596446b147fe5943c5460b4ef540dbc5e5a3dfad4bdc7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078876"
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

 

 



