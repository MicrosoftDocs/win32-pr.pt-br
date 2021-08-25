---
description: Lista as alterações para os recursos de dados do enveloping.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Adições de dados envelopadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75aab8e931ff8c8591a899a21a1071754e32f2e2cecec3755baa3dc64db94dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874416"
---
# <a name="enveloped-data-additions"></a>Adições de dados envelopadas

As seguintes alterações foram feitas em recursos de dados envelopos:

-   A identificação do destinatário pode ser feita não apenas pelo emissor e número de série (PKCS \# 7 1,5), mas também pelo identificador de chave.
-   Três opções de troca de chave de destinatário são fornecidas:
    -   Transporte de chave usando chaves RSA.
    -   O acordo de chave usando Ephemeral-Static Diffie-Hellman chaves de algoritmo encapsuladas com 3DES ou RC2, ou Ephemeral-Static curva elíptica Diffie-Hellman chaves de algoritmo encapsuladas com AES.
    -   Chave de criptografia de chave ou transferência de chave de lista de mensagens em que a chave usada para criptografar a chave de criptografia de conteúdo já foi distribuída para os destinatários. RC2, 3DES e AES são permitidos como algoritmos de encapsulamento de chaves.
-   Os atributos não protegidos podem ser incluídos na mensagem.
-   Um campo **OriginatorInfo** que contém informações sobre o originador foi adicionado que pode conter certificados e CRLs.
-   algoritmos baseados em ECC (criptografia de curva elíptica) e AES exigem o Windows Vista ou posterior.

 

 



