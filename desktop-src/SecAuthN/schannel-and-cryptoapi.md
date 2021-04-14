---
description: O Schannel usa o CryptoAPI para operações criptográficas, como armazenar chaves públicas/privadas.
ms.assetid: 5ad9a171-5f69-4035-aac5-ae8d27d0abfb
title: Schannel e CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0684cd690911444b77ba27d2876e578fd71c73a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370569"
---
# <a name="schannel-and-cryptoapi"></a>Schannel e CryptoAPI

O Schannel usa o [CryptoAPI](../seccrypto/cryptography-essentials.md) para operações criptográficas, como armazenar [*chaves públicas/privadas*](../secgloss/p-gly.md).

Os tópicos a seguir fornecem informações detalhadas sobre como o Schannel utiliza o CryptoAPI.



| Tópico                                                                   | Descrição                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Repositórios de certificados](certificate-stores.md)<br/>                 | Os certificados de cliente e de servidor devem ser armazenados em um repositório de certificados.<br/>                                |
| [CryptoAPI 2.0 chaves privadas](cryptoapi-2-0-private-keys.md)<br/> | As credenciais Schannel são representadas internamente como estruturas de [**\_ contexto de certificado**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) .<br/> |



 

 

 
