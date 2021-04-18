---
description: Explica a arquitetura do sistema CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Arquitetura do sistema CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296277"
---
# <a name="cryptoapi-system-architecture"></a>Arquitetura do sistema CryptoAPI

A arquitetura do sistema CryptoAPI é composta de cinco áreas funcionais principais:

-   [Funções de criptografia base](#base-cryptographic-functions)
-   [Funções de codificação/decodificação de certificado](#certificate-encodedecode-functions)
-   [Funções de repositório de certificados](#certificate-store-functions)
-   [Funções de mensagens simplificadas](#simplified-message-functions)
-   [Funções de mensagem de nível baixo](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a>Funções de criptografia base

-   *Funções de contexto* usadas para se conectar a um CSP. Essas funções permitem que os aplicativos escolham um CSP específico por nome ou escolham um CSP específico que possa fornecer uma classe necessária de funcionalidade.
-   [*Funções de geração de chave*](../secgloss/k-gly.md) usadas para gerar e armazenar [*chaves criptográficas*](../secgloss/c-gly.md). O suporte completo está incluído para alterar os [*modos de encadeamento*](../secgloss/c-gly.md), os [*vetores de inicialização*](../secgloss/i-gly.md)e outros recursos de criptografia. Para obter mais informações, consulte [funções de geração de chave e troca](cryptography-functions.md).
-   *Funções de troca de chaves* usadas para trocar ou transmitir chaves. Para obter mais informações, consulte [armazenamento de chaves de criptografia e troca](cryptographic-key-storage-and-exchange.md) e [funções de geração de chave e do Exchange](cryptography-functions.md).

## <a name="certificate-encodedecode-functions"></a>Funções de codificação/decodificação de certificado

-   Funções usadas para criptografar ou descriptografar dados. O suporte também está incluído para dados de [*hash*](../secgloss/h-gly.md) . Para obter mais informações, consulte [funções de criptografia de dados e](cryptography-functions.md) descriptografia e [criptografia e descriptografia de dados](data-encryption-and-decryption.md).

## <a name="certificate-store-functions"></a>Funções de repositório de certificados

-   Funções usadas para gerenciar coleções de certificados digitais. Para obter mais informações, consulte [certificados digitais](digital-certificates.md) e [funções de repositório de certificados](cryptography-functions.md).

## <a name="simplified-message-functions"></a>Funções de mensagens simplificadas

-   Funções usadas para criptografar e descriptografar mensagens e dados.
-   Funções usadas para assinar mensagens e dados.
-   Funções usadas para verificar a autenticidade de assinaturas em mensagens recebidas e dados relacionados.

Para obter mais informações, consulte [mensagens simplificadas](simplified-messages.md) e [funções de mensagens simplificadas](cryptography-functions.md).

## <a name="low-level-message-functions"></a>Funções de mensagem de nível baixo

-   Funções usadas para executar todas as tarefas executadas pelas funções de mensagem simplificadas. As funções de mensagem de nível baixo fornecem mais flexibilidade do que as funções de mensagem simplificadas, mas exigem mais chamadas de função. Para obter mais informações, consulte [mensagens de nível inferior](low-level-messages.md) e [funções de mensagens de nível baixo](cryptography-functions.md).

![arquitetura de CryptoAPI](images/cryparch.png)

Cada uma das áreas funcionais tem uma palavra-chave em seu nome de função que indica sua área funcional.



| Área funcional              | Convenção de nome de função |
|------------------------------|--------------------------|
| Funções de criptografia base | Confuso                    |
| Funções de codificação/decodificação  | Confuso                    |
| Funções de repositório de certificados  | Repositório                    |
| Funções de mensagens simplificadas | Mensagem                  |
| Funções de mensagem de nível baixo  | MSG                      |



 

Os aplicativos usam funções em todas essas áreas. Essas funções, juntas, compõem o CryptoAPI. As [*funções de criptografia base*](../secgloss/b-gly.md) usam os CSPs para os algoritmos de criptografia necessários e para a geração e o armazenamento seguro de [chaves de criptografia](cryptographic-keys.md).

Dois tipos diferentes de chaves de criptografia são usados: [*chaves de sessão*](../secgloss/s-gly.md), que são usadas para criptografia/descriptografia única e [*pares de chaves pública/privada*](../secgloss/p-gly.md), que são usadas de forma mais permanente.

> [!Note]  
> Embora um aplicativo possa se comunicar diretamente com qualquer uma das cinco áreas funcionais, ele não pode se comunicar diretamente com um CSP. Todas as comunicações de aplicativo para CSP ocorrem por meio das [*funções criptográficas base*](../secgloss/b-gly.md). As funções criptográficas base têm um parâmetro que especifica qual CSP usar. Esse parâmetro pode ser definido como **nulo** para selecionar um CSP padrão.

 

 

 
