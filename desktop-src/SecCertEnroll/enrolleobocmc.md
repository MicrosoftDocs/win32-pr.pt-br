---
description: Cria uma solicitação de certificado CMC em nome de outro usuário e registra o usuário em uma hierarquia de certificado.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: enrollEOBOCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501969"
---
# <a name="enrolleobocmc"></a>enrollEOBOCMC

O exemplo enrollEOBOCMC cria uma solicitação de certificado CMC em nome de outro usuário e registra o usuário em uma hierarquia de certificados. O registro em nome de outro usuário requer que a solicitação de certificado seja assinada usando um certificado de agente de registro.

## <a name="location"></a>Local

Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollEOBOCMC.

## <a name="discussion"></a>Discussão

O exemplo de enrollEOBOCMC:

1.  Processa os seguintes argumentos de linha de comando:
    -   O nome de um modelo de certificado.
    -   O nome do usuário que está solicitando o certificado.
    -   O nome de um arquivo PFX (troca de informações pessoais) no qual salvar a solicitação.
    -   Uma senha a ser usada com o arquivo PFX.
    -   Um nome de modelo de agente de registro opcional. O modelo é usado para criar um certificado de agente de registro se não houver nenhum no repositório de certificados.
2.  Cria um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e o inicializa usando o modelo de certificado especificado na linha de comando.
3.  Adiciona o nome do solicitante ao objeto de solicitação CMC.
4.  Recupera um certificado de agente de registro existente ou, se não for possível encontrar um, cria uma solicitação de certificado do modelo de agente de registro especificado na linha de comando e tenta registrá-lo.
5.  Verifica a cadeia de certificados que contém o certificado do agente de registro.
6.  Cria um objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , inicializa-o usando o certificado do agente de registro, recupera a coleção [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) do objeto de solicitação CMC e adiciona o objeto de certificado de autenticação do agente de registro à coleção. O objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) discutido na próxima etapa usa o certificado para assinar a solicitação CMC.
7.  Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , inicializa-o usando a solicitação CMC, tenta registrá-lo e verifica o progresso do processo de registro.
8.  Exporta o certificado instalado para um arquivo PFX. O arquivo é protegido usando a senha especificada na linha de comando. A função EncodeToFileW é definida em enrollCommon. cpp.
9.  Exclui o certificado do repositório de certificados. As funções usadas no exemplo de código a seguir podem ser encontradas na documentação do CryptoAPI.
10. Exclui a chave privada do computador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitação EOBO de CMC](cmc-eobo-request.md)
</dt> <dt>

[\#Solicitação PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 



