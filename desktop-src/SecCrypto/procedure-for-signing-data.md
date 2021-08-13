---
description: Mostra a relação entre esses parâmetros de função que apontam para estruturas ou matrizes e seus dados inicializados.
ms.assetid: 89caf4d3-727f-472b-9a09-e81b4ff4d127
title: Procedimento para assinatura de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10bae09c97fa42086f853d43b2a5a9dc02f0cbdbe2dd946fefe5d39e28a32104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977541"
---
# <a name="procedure-for-signing-data"></a>Procedimento para assinatura de dados

Uma única função, [**CryptSignMessage,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)executa todas as tarefas listadas em [Criando uma mensagem assinada.](creating-a-signed-message.md) No entanto, a inicialização de estruturas e outros dados ainda é necessária. A ilustração a seguir mostra a relação entre esses parâmetros de função que apontam para estruturas ou matrizes e seus dados inicializados. A ilustração mostra apenas os parâmetros de função e membros da estrutura derivados de outras estruturas ou funções. O restante dos parâmetros são inicializações simples.

![mapa de inicialização para uma chamada para cryptsignmessage](images/crypsign.png)

**Para assinar dados usando CryptSignMessage**

1.  Obter um ponteiro para os dados que devem ser assinados.
2.  Atribua o ponteiro aos dados para indexar zero de uma matriz "dados a serem assinados".
3.  Obter um handle para o provedor criptográfico.
4.  Abra um [*armazenamento de*](../secgloss/c-gly.md) certificados que contém o certificado do signante.
5.  Obter um endereço para o certificado do signante.
6.  Atribua o endereço do certificado ao índice zero da *matriz MsgCert.*
7.  Atribua os endereços de quaisquer outros certificados a serem incluídos com a mensagem à *matriz MsgCert.*
8.  Inicialize a [**estrutura CRYPT \_ ALGORITHM \_ IDENTIFIER,**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) inicializando o membro **pszObjId** para o algoritmo de hash desejado e os outros membros conforme apropriado.
9.  Inicialize a estrutura [**\_ CRYPT SIGN MESSAGE \_ \_ PARA,**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) inicializando o membro **pSigningCert** para o endereço do certificado do signante, o membro da matriz **MsgCert** para o endereço dos certificados do signante e de outros, o membro **HashAlgorithm** para o endereço da estrutura [**CRYPT ALGORITHM \_ \_ IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) e os outros membros conforme apropriado.
10. Chame a função [**CryptSignMessage,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) passando a estrutura [**CRYPT SIGN MESSAGE \_ \_ \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) para o parâmetro *pSignPara,* o endereço da matriz "dados a serem assinados" para o parâmetro *rgpbToBeSigned,* um endereço para o parâmetro de saída *pbSignedBlob* e valores para os outros parâmetros conforme apropriado.

 

 
