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
# <a name="tls-record-protocol"></a>Protocolo de registro TLS

O protocolo de registro de [*segurança de camada de transporte*](../secgloss/t-gly.md) (TLS) protege os dados do aplicativo usando as chaves criadas durante o [handshake](tls-handshake-protocol.md). O protocolo de registro é responsável por proteger os dados do aplicativo e verificar sua [*integridade*](../secgloss/i-gly.md) e origem. Ele gerencia o seguinte:

-   Divisão de mensagens de saída em blocos gerenciáveis e remontagem de mensagens de entrada.
-   Compactação de blocos de saída e descompressão de blocos de entrada (opcional).
-   Aplicar um [*Message Authentication Code*](../secgloss/m-gly.md) (Mac) a mensagens de saída e verificar as mensagens de entrada usando o Mac.
-   Criptografar mensagens de saída e descriptografar mensagens de entrada.

Quando o protocolo de registro é concluído, os dados criptografados de saída são passados para a camada TCP (Transmission Control Protocol) para transporte.

 

 
