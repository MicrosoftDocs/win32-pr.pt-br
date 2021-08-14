---
description: O processo de codificação é o inverso do processo de decodificação descrito em Decodificar uma estrutura DE \_ INFORMAÇÕES DO CERTIFICADO.
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: Codificando uma estrutura CERT_INFO dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b469ae0bdf02ffd8f30f8b0c2dd44051239a5702ff32704d58de8b60f1ca9701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766773"
---
# <a name="encoding-a-cert_info-structure"></a>Codificando uma estrutura DE \_ INFORMAÇÕES DE CERTIFICADO

O processo de codificação é o inverso do processo de decodificação descrito em [Decodificar uma estrutura DE \_ INFORMAÇÕES DO CERTIFICADO.](decoding-a-cert-info-structure.md) Por exemplo, o procedimento a seguir adicionaria um **Emissor codificado** a uma estrutura [**CERT \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) Consulte também a ilustração que segue o procedimento.

**Para adicionar um Emissor codificado a uma estrutura CERT \_ INFO**

1.  Crie uma cadeia de caracteres que contém o nome do emissor a ser usado.
2.  Crie uma matriz de [**estruturas CERT \_ RDN \_ ATTR,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) que serão inicializadas para conter as informações apropriadas sobre a cadeia de caracteres de nome do emissor que acabou de ser criada.
3.  Crie uma matriz de [**\_ estruturas cert RDN,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) uma das quais tem as informações sobre a matriz de estruturas [**\_ \_ ATTR do CERT RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) que acabou de ser inicializada.
4.  Crie uma [**estrutura DE INFORMAÇÕES DE NOME \_ \_ DO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) CERTIFICADO que tenha um ponteiro para a matriz de estruturas [**cert \_ RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) que acabou de criar.
5.  Chame [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) para obter o tamanho do BLOB codificado na saída, passando o endereço da estrutura [**CERT NAME \_ \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) que você acabou de criar.
6.  Alocar memória para o BLOB codificado de saída.
7.  Chame [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) novamente, passando as mesmas informações, mas agora passando a ele o endereço da memória que acabou de alocar.
8.  De definir **o membro Issuer.cbData** da estrutura [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) para o tamanho retornado na etapa 5 e o membro **Issuer.pbData** para o endereço obtido na etapa 6. O BLOB **do Emissor codificado** agora reside lá.

![adicionando um emissor codificado a uma estrutura de \- informações de certificado](images/encflow.png)

Para inicializar e codificar algumas informações de extensão de certificado, use o procedimento a seguir. Consulte também a ilustração que segue o procedimento.

**Para adicionar informações de extensão codificada a uma estrutura CERT \_ INFO**

1.  Criar e inicializar uma estrutura de informações de extensão – para este exemplo, é uma estrutura [**DE \_ INFORMAÇÕES DE \_ RESTRIÇÕES BÁSICAS \_ DO CERT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info)
2.  Chame [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject), passando o endereço da estrutura que acabou de ser criada, para obter o tamanho do BLOB codificado na saída.
3.  Alocar memória para o BLOB codificado de saída.
4.  Chame [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) novamente, passando as mesmas informações, exceto agora passar o endereço da memória alocada.
5.  Crie uma matriz de [**estruturas DE \_ EXTENSÃO CERT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension)
6.  Inicialize uma das estruturas [**DE \_ EXTENSÃO do CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) para que **pszObjId** seja a cadeia de caracteres adequada para os dados contidos em **Value** e que **Value** contenha o BLOB de dados criptografados que foi produzido da chamada para [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject).
7.  Inicialize o **membro rgExtension** da estrutura [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) para apontar para a matriz de [**estruturas DE EXTENSÃO \_ DE**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) CERTIFICADO.

![adicionando informações de extensão codificada a uma estrutura de \- informações do certificado](images/xtenflow.png)

 

 



