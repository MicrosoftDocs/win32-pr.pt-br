---
description: Explica a arquitetura do sistema CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Arquitetura do sistema CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791ed0ebfc82df1dc7b6e9600d4e0455ae60df3da35cfe3f8fd613f7b230ebd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768798"
---
# <a name="cryptoapi-system-architecture"></a>Arquitetura do sistema CryptoAPI

A arquitetura do sistema CryptoAPI é composta por cinco áreas funcionais principais:

-   [Funções criptográficas base](#base-cryptographic-functions)
-   [Funções de codificação/decodificar certificado](#certificate-encodedecode-functions)
-   [Funções do Armazenamento de Certificados](#certificate-store-functions)
-   [Funções de mensagem simplificadas](#simplified-message-functions)
-   [Funções de mensagem de baixo nível](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a>Funções criptográficas base

-   *Funções de contexto usadas* para se conectar a um CSP. Essas funções permitem que os aplicativos escolham um CSP específico por nome ou escolham um CSP específico que possa fornecer uma classe de funcionalidade necessária.
-   [*Funções de geração de chave usadas*](../secgloss/k-gly.md) para gerar e armazenar [*chaves criptográficas*](../secgloss/c-gly.md). O suporte completo está incluído para alterar [*modos de encadeamento,*](../secgloss/c-gly.md) [*vetores de inicialização*](../secgloss/i-gly.md)e outros recursos de criptografia. Para obter mais informações, consulte [Geração de chaves e Exchange Funções](cryptography-functions.md).
-   *Funções de troca de chaves usadas* para trocar ou transmitir chaves. Para obter mais informações, [consulte Cryptographic Key Armazenamento e Exchange](cryptographic-key-storage-and-exchange.md) e Key Generation and Exchange [Functions](cryptography-functions.md).

## <a name="certificate-encodedecode-functions"></a>Funções de codificação/decodificar certificado

-   Funções usadas para criptografar ou descriptografar dados. O suporte também está incluído para [*dados de hash.*](../secgloss/h-gly.md) Para obter mais informações, consulte Funções de criptografia e [descriptografia](cryptography-functions.md) de dados e [Criptografia de dados e descriptografia](data-encryption-and-decryption.md).

## <a name="certificate-store-functions"></a>Funções do Armazenamento de Certificados

-   Funções usadas para gerenciar coleções de certificados digitais. Para obter mais informações, [consulte Certificados digitais e](digital-certificates.md) funções de armazenamento de [certificados](cryptography-functions.md).

## <a name="simplified-message-functions"></a>Funções de mensagem simplificadas

-   Funções usadas para criptografar e descriptografar mensagens e dados.
-   Funções usadas para assinar mensagens e dados.
-   Funções usadas para verificar a autenticidade de assinaturas em mensagens recebidas e dados relacionados.

Para obter mais informações, consulte [Mensagens simplificadas](simplified-messages.md) e [Funções de mensagem simplificadas](cryptography-functions.md).

## <a name="low-level-message-functions"></a>Funções de mensagem de baixo nível

-   Funções usadas para executar todas as tarefas executadas pelas funções de mensagem simplificadas. As funções de mensagem de baixo nível fornecem mais flexibilidade do que as funções de mensagem simplificadas, mas exigem mais chamadas de função. Para obter mais informações, [consulte Mensagens de baixo nível](low-level-messages.md) e Funções de mensagem de baixo [nível](cryptography-functions.md).

![Arquitetura de cryptoapi](images/cryparch.png)

Cada uma das áreas funcionais tem uma palavra-chave em seu nome de função que indica sua área funcional.



| Área funcional              | Convenção de nome de função |
|------------------------------|--------------------------|
| Funções criptográficas base | Cripta                    |
| Funções de codificação/decodificação  | Cripta                    |
| Funções do armazenamento de certificados  | Repositório                    |
| Funções de mensagem simplificadas | Mensagem                  |
| Funções de mensagem de baixo nível  | Msg                      |



 

Os aplicativos usam funções em todas essas áreas. Essas funções, realizadas juntas, comem CryptoAPI. As [*funções criptográficas base*](../secgloss/b-gly.md) usam os CSPs para os algoritmos criptográficos necessários e para a geração e o armazenamento seguro de chaves [criptográficas](cryptographic-keys.md).

Dois tipos diferentes de chaves criptográficas são [*usados:*](../secgloss/s-gly.md)chaves de sessão , que são usadas para uma única criptografia/descriptografia e pares de chaves [*públicas/privadas,*](../secgloss/p-gly.md)que são usadas de forma mais permanente.

> [!Note]  
> Embora um aplicativo possa se comunicar diretamente com qualquer uma das cinco áreas funcionais, ele não pode se comunicar diretamente com um CSP. Todas as comunicações de aplicativo para CSP ocorrem por meio [*das funções criptográficas base*](../secgloss/b-gly.md). As funções criptográficas base têm um parâmetro que especifica qual CSP usar. Esse parâmetro pode ser definido como **NULL** para selecionar um CSP padrão.

 

 

 
