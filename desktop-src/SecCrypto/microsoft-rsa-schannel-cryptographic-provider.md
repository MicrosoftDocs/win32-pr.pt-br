---
description: O provedor criptográfico RSA/Schannel da Microsoft dá suporte a hash, assinatura de dados e verificação de assinatura.
ms.assetid: 34ede85a-579f-400f-a53e-e40711fcaaf3
title: Provedor criptográfico RSA/Schannel da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b38ef6573cada965c0b5e982d7808a7fe2b7670271f4f8ce1fd51c99d002db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100686"
---
# <a name="microsoft-rsaschannel-cryptographic-provider"></a>Provedor criptográfico RSA/Schannel da Microsoft

O provedor criptográfico do Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) oferece suporte a hash, assinatura de dados e verificação de assinatura. O identificador de algoritmo CALG \_ SSL3 \_ SHAMD5 é usado para autenticação de cliente SSL 3,0 e TLS 1,0. Esse CSP dá suporte à derivação de chave para os protocolos SSL2, PCT1, SSL3 e TLS1. O [*hash*](../secgloss/h-gly.md) consiste em uma concatenação de um hash MD5 com um hash SHA e assinado com uma [*chave privada*](../secgloss/p-gly.md)RSA. Ele pode ser exportado para outros países/regiões.



|                   | Valor                         |
|-------------------|-------------------------------|
| **Tipo de provedor** | PROV \_ RSA \_ Schannel           |
| **Nome do provedor** | Microsoft \_ \_ SChannel RSA \_ - \_ Prov  |



 

Para obter mais informações sobre provedores RSA/Schannel, consulte [funções de CSP](cryptography-functions.md).

 

 
