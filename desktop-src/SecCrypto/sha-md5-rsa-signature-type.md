---
description: Os CSPs para \_ o Prov RSA \_ Schannel devem dar suporte ao CALG \_ SSL3 \_ SHAMD5 hash que seja compatível com o provedor criptográfico base da Microsoft usado em SSL 3,0 e autenticação de cliente TLS 1,0.
ms.assetid: ca8be4fd-e7ca-4def-927d-b168628c566e
title: Tipo de assinatura do SHA/MD5 RSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71dcd515c61a4baf3da1fb35e4b5e6d21d5c849e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757998"
---
# <a name="shamd5-rsa-signature-type"></a>Tipo de assinatura do SHA/MD5 RSA

Os CSPs para \_ o Prov RSA \_ Schannel devem dar suporte ao CALG \_ SSL3 \_ SHAMD5 [*hash*](../secgloss/h-gly.md) que seja compatível com o provedor CRIPTOGRÁFICO Base da Microsoft usado em SSL 3,0 e autenticação de cliente TLS 1,0. Esse hash consiste em uma concatenação de um hash [*MD5*](../secgloss/m-gly.md) e um hash SHA assinado com uma chave privada RSA ou Diffie-Hellman. Um identificador para um valor de hash desse tipo é criado usando a função [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) ou [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) com CALG \_ SSL3 \_ SHAMD5 como o parâmetro *algid* . Exemplos de uso de funções de hash podem ser vistos no [programa c de exemplo: Criando e aplicando hash a uma chave de sessão e um](example-c-program-creating-and-hashing-a-session-key.md) [programa de exemplo c: assinando um hash e verificando a assinatura de hash](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).

 

 
