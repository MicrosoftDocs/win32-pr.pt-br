---
description: O processo de codificação é o inverso do processo de decodificação descrito na decodificação de uma estrutura de informações de certificado \_ .
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: Codificando uma estrutura de CERT_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645a1d3054546a7b11c57d4f515dc7d3e26b5fe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753406"
---
# <a name="encoding-a-cert_info-structure"></a>Codificando uma \_ estrutura de informações de certificado

O processo de codificação é o inverso do processo de decodificação descrito na [decodificação de uma \_ estrutura de informações de certificado](decoding-a-cert-info-structure.md). Por exemplo, o procedimento a seguir adicionaria um **emissor** codificado a uma estrutura de [**\_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) . Consulte também a ilustração que segue o procedimento.

**Para adicionar um emissor codificado a uma estrutura de \_ informações de certificado**

1.  Crie uma cadeia de caracteres contendo o nome do emissor a ser usado.
2.  Crie uma matriz de [**estruturas \_ \_ attr de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) , que será inicializada para conter as informações apropriadas sobre a cadeia de caracteres de nome do emissor recém-criada.
3.  Crie uma matriz de [**estruturas \_ RDN de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) , uma das quais tem as informações sobre a matriz de estruturas [**\_ \_ attr de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) que acabou de ser inicializada.
4.  Crie uma estrutura de [**\_ \_ informações de nome de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) que tenha um ponteiro para a matriz de estruturas [**\_ RDN de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) que acabou de criar.
5.  Chame [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) para obter o tamanho do blob codificado de saída, passando-o para o endereço da estrutura de [**\_ \_ informações do nome de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) que você acabou de criar.
6.  Aloque memória para o BLOB codificado de saída.
7.  Chame [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) novamente, passando as mesmas informações, mas agora passando o endereço da memória que acabou de ser alocada.
8.  Defina o membro **emissor. cbData** da estrutura [**\_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) para o tamanho retornado na etapa 5 e o membro **emissor. pbData** para o endereço obtido na etapa 6. O blob do **emissor** codificado agora reside lá.

![adicionando um emissor codificado a uma estrutura de \- informações de certificado](images/encflow.png)

Para inicializar e codificar algumas informações de extensão de certificado, use o procedimento a seguir. Consulte também a ilustração que segue o procedimento.

**Para adicionar informações de extensão codificadas a uma estrutura de informações de certificado \_**

1.  Criar e inicializar uma estrutura de informações de extensão — neste exemplo, é uma estrutura de informações de [**\_ \_ restrições \_ básicas de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) .
2.  Chame [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject), passando o endereço da estrutura que acabou de criar para obter o tamanho do blob codificado de saída.
3.  Aloque memória para o BLOB codificado de saída.
4.  Chame [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) novamente, passando as mesmas informações, exceto que agora passe o endereço da memória alocada.
5.  Crie uma matriz de estruturas de [**\_ extensão de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) .
6.  Inicialize uma das estruturas [**de \_ extensão de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) para que **pszObjId** seja a cadeia de caracteres apropriada para os dados contidos em **valor** e esse **valor** contenha o blob de dados criptografados que foi impresso da chamada para [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject).
7.  Inicialize o membro **rgExtension** da estrutura [**de \_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) para apontar para a matriz de estruturas de [**\_ extensão de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) .

![adicionando informações de extensão codificadas a uma estrutura de informações de certificado \-](images/xtenflow.png)

 

 



