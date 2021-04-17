---
description: Lista as alterações para os recursos de dados do enveloping.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Adições de dados envelopadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770349"
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
-   Algoritmos baseados em ECC (criptografia de curva elíptica) e AES exigem o Windows Vista ou posterior.

 

 



