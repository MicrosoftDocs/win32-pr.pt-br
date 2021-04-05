---
description: As informações neste tópico se aplicam ao Windows Server 2003 e ao Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Protocolo protocolo SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921615"
---
# <a name="secure-sockets-layer-protocol"></a>Protocolo protocolo SSL

As informações neste tópico se aplicam ao Windows Server 2003 e ao Windows XP. Para conjuntos de codificação para o Windows Server 2008 e o Windows Vista, consulte [pacotes de codificação no Schannel](cipher-suites-in-schannel.md).

O Schannel dá suporte às versões 2,0 e 3,0 do [*protocolo protocolo SSL (SSL)*](../secgloss/s-gly.md).

> [!Note]  
> A partir do Windows 10, versão 1607 e Windows Server 2016, o SSL 2,0 foi removido e não tem mais suporte.

 

## <a name="ssl-30"></a>SSL 3.0

O SSL 3,0 é o predecessor do [protocolo de segurança da camada de transporte](transport-layer-security-protocol.md).

O Schannel dá suporte aos conjuntos de codificação listados em [TLS Cipher Suites](tls-cipher-suites.md) para SSL 3,0. O SSL 3,0 dá suporte a todos os conjuntos de codificação listados em TLS Cipher Suites, bem como SSL \_ Fortezza \_ Kea \_ with \_ Fortezza \_ CBC \_ Sha.

## <a name="ssl-20"></a>SSL 2.0

O SSL 2,0 foi substituído pelo TLS e não deve ser usado para um novo desenvolvimento.

O Schannel dá suporte aos seguintes conjuntos de codificação para SSL 2,0. Os pacotes são listados na ordem do mais seguro para o menos seguro.

-   SSL \_ RC4 \_ 128 \_ com \_ MD5
-   SSL \_ DES \_ 192 \_ EDE3 \_ CBC \_ com \_ MD5
-   Protocolo \_ de criptografia RC2 \_ CBC \_ 128 \_ CBC \_ com \_ MD5
-   \_CBC SSL \_ des \_ 64 \_ com \_ MD5
-   SSL \_ RC4 \_ 128 \_ EXPORT40 \_ com \_ MD5

 

 
