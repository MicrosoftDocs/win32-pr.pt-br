---
description: Cria uma solicitação personalizada de PKCS \# 10 e tenta registrá-la em uma CA (autoridade de certificação) corporativa.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb88a2295217874a12da8b701a46f8dafe3db1cbf53d01273222e607195a789a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780035"
---
# <a name="enrollcustompkcs10_2"></a>enrollCustomPKCS10 \_ 2

O exemplo de enrollCustomPKCS10 \_ 2 cria uma solicitação personalizada de PKCS \# 10 e tenta registrá-la em uma CA ( [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) ) corporativa.

## <a name="location"></a>Localização

ao instalar o Microsoft Windows Software Development Kit (SDK), o exemplo é instalado por padrão na pasta *% programfiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 Certificate enrollment \\ VC \\ enrollCustomPKCS10 \_ 2.

## <a name="discussion"></a>Discussão

O exemplo de enrollCustomPKCS10 \_ 2:

1.  Processa os argumentos de linha de comando. A linha de comando deve conter o nome de um modelo e o nome de um provedor criptográfico.
2.  Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e o inicializa usando o nome do modelo especificado na linha de comando.
3.  Recupera a [*solicitação de certificado*](/windows/desktop/SecGloss/c-gly) do objeto de registro.
4.  Recupera a solicitação PKCS \# 10 interna do objeto de solicitação de certificado obtido na etapa 3.
5.  Recupera uma [*chave privada*](/windows/desktop/SecGloss/p-gly) da solicitação PKCS \# 10.
6.  Cria uma coleção [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) e adiciona os provedores criptográficos disponíveis à coleção e, em seguida, recupera um objeto [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) para o provedor especificado na linha de comando.
7.  Define o objeto de status na chave privada.
8.  Tenta registrar a [*solicitação de certificado*](/windows/desktop/SecGloss/c-gly).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\#Solicitação PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 
