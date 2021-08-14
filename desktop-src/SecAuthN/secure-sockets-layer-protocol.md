---
description: As informações neste tópico se aplica ao Windows Server 2003 e Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: protocolo protocolo SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf8e6b7232db8bef98d5170887d6be75c9770927954a40b606450bf214efdf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918379"
---
# <a name="secure-sockets-layer-protocol"></a>protocolo protocolo SSL

As informações neste tópico se aplica ao Windows Server 2003 e Windows XP. Para os suites de criptografia para Windows Server 2008 e Windows Vista, consulte [Cipher Suites in Schannel](cipher-suites-in-schannel.md).

O Schannel dá suporte às versões 2.0 e 3.0 do [*protocolo protocolo SSL (SSL).*](../secgloss/s-gly.md)

> [!Note]  
> A partir Windows 10, a versão 1607 e Windows Server 2016, o SSL 2.0 foi removido e não tem mais suporte.

 

## <a name="ssl-30"></a>SSL 3.0

O SSL 3.0 é o antecessor do Protocolo de Segurança de Camada [de Transporte](transport-layer-security-protocol.md).

O Schannel dá suporte aos suites de criptografia listados em [Conjunto de Criptografia TLS](tls-cipher-suites.md) para SSL 3.0. O SSL 3.0 dá suporte a todos os suites de criptografia listados em TLS Cipher Suites, bem como AO SSL \_ FORTEZZA \_ KEA \_ WITH \_ FORTEZZA \_ CBC \_ SHA.

## <a name="ssl-20"></a>SSL 2.0

O SSL 2.0 foi superado pelo TLS e não deve ser usado para novo desenvolvimento.

O Schannel dá suporte aos seguintes pacote de criptografia para SSL 2.0. Os suites são listados na ordem da mais segura para a menos segura.

-   SSL \_ RC4 \_ 128 \_ WITH \_ MD5
-   SSL \_ DES \_ 192 \_ EDE3 \_ CBC \_ COM \_ MD5
-   SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ WITH \_ MD5
-   SSL \_ DES \_ 64 \_ CBC \_ COM \_ MD5
-   SSL \_ RC4 \_ 128 \_ EXPORT40 \_ WITH \_ MD5

 

 
