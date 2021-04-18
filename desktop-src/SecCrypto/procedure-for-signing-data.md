---
description: Mostra a relação entre os parâmetros de função que apontam para estruturas ou matrizes e seus dados inicializados.
ms.assetid: 89caf4d3-727f-472b-9a09-e81b4ff4d127
title: Procedimento para assinar dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba289928ab39c690e1c44bdbf65c77c18b7edab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792673"
---
# <a name="procedure-for-signing-data"></a>Procedimento para assinar dados

Uma única função, [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage), executa todas as tarefas listadas em [criando uma mensagem assinada](creating-a-signed-message.md). No entanto, a inicialização de estruturas e outros dados ainda é necessária. A ilustração a seguir mostra a relação entre os parâmetros de função que apontam para estruturas ou matrizes e seus dados inicializados. A ilustração mostra apenas os parâmetros de função e membros de estrutura que são derivados de outras estruturas ou funções. O restante dos parâmetros são inicializações simples.

![mapa de inicialização para uma chamada para CryptSignMessage](images/crypsign.png)

**Para assinar dados usando o CryptSignMessage**

1.  Obtenha um ponteiro para os dados que serão assinados.
2.  Atribua o ponteiro aos dados para indexar zero de uma matriz de "dados a serem assinados".
3.  Obtenha um identificador para o provedor criptográfico.
4.  Abra um [*repositório de certificados*](../secgloss/c-gly.md) que contenha o certificado do signatário.
5.  Obtenha um endereço para o certificado do Assinante.
6.  Atribua o endereço do certificado ao índice zero da matriz *MsgCert* .
7.  Atribua os endereços de quaisquer outros certificados a serem incluídos com a mensagem para a matriz *MsgCert* .
8.  Inicialize a estrutura do [**\_ \_ identificador do algoritmo cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) , inicializando o membro **pszObjId** para o algoritmo de hash desejado e os outros membros, conforme apropriado.
9.  Inicialize a estrutura de [**\_ \_ mensagens \_ de sinal cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) , inicializando o membro **pSigningCert** para o endereço do certificado do signatário, o membro da matriz **MsgCert** para o endereço dos certificados do signatário e outros, o membro **HashAlgorithm** para o endereço da estrutura [**do \_ \_ identificador do algoritmo cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) e os outros membros, conforme apropriado.
10. Chame a função [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) , passando a estrutura para [**\_ \_ mensagem \_ de sinal cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) para o parâmetro *pSignPara* , o endereço da matriz "dados a serem assinados" para o parâmetro *rgpbToBeSigned* , um endereço para o parâmetro de saída *pbSignedBlob* e valores para os outros parâmetros, conforme apropriado.

 

 
