---
description: O protocolo de registro TLS (Transport Layer Security) protege os dados do aplicativo usando as chaves criadas durante o Handshake.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: Protocolo de registro TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce441de892367b49e1fd4aa285b5398dd5e7c1667d0ea785f6925995c89e1dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915736"
---
# <a name="tls-record-protocol"></a>Protocolo de registro TLS

O protocolo de registro TLS (Transport [*Layer Security)*](../secgloss/t-gly.md) protege os dados do aplicativo usando as chaves criadas durante o [Handshake](tls-handshake-protocol.md). O Protocolo de Registro é responsável por proteger os dados do aplicativo e verificar sua [*integridade*](../secgloss/i-gly.md) e sua origem. Ele gerencia o seguinte:

-   Dividir mensagens de saída em blocos gerenciáveis e remontar mensagens de entrada.
-   Compactando blocos de saída e descompactando blocos de entrada (opcional).
-   Aplicar um [*MAC (Message Authentication Code)*](../secgloss/m-gly.md) a mensagens de saída e verificar mensagens de entrada usando o MAC.
-   Criptografar mensagens de saída e descriptografar mensagens de entrada.

Quando o Protocolo de Registro é concluído, os dados criptografados de saída são passados para a camada TCP (Protocolo de Controle de Transmissão) para transporte.

 

 
