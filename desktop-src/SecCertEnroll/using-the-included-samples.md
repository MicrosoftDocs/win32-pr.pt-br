---
description: A API de Registro de Certificado inclui vários exemplos projetados para ajudá-lo a criar aplicativos personalizados. A maioria dos exemplos é escrita usando C++, mas os exemplos de C# e Visual Basic Scripting Edition (VBScript) também estão incluídos.
ms.assetid: 70ac7b75-542c-4d79-85ce-4b1bac414879
title: Usando os exemplos incluídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511d9d5424455c1b54c6bd03cc72138b3672b256d535dcbdaf31d2393b2cb5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127197"
---
# <a name="using-the-included-samples"></a>Usando os exemplos incluídos

A API de Registro de Certificado inclui vários exemplos projetados para ajudá-lo a criar aplicativos personalizados. A maioria dos exemplos é escrita usando C++, mas os exemplos de C# e Visual Basic Scripting Edition (VBScript) também estão incluídos.

Quando você instala o Microsoft Windows Software Development Kit (SDK), os exemplos a seguir são instalados, por padrão, na pasta *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate \\ Enrollment.



| Amostra                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                | Idioma            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [createCNGCustomCMC](createcngcustomcmc.md)                           | Cria um objeto de solicitação do CMC de uma solicitação PKCS \# 10 aninhada interna.<br/>                                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCommon](enrollcommon.md)                                       | Contém as seguintes funções auxiliares e macros usadas pelos exemplos incluídos.<br/>                                                                                                                                                                                                                                                                | C++<br/>      |
| [enrollCustomCMC](enrollcustomcmc.md)                                 | Cria uma solicitação de certificado do CMC e registra um computador em uma hierarquia de certificados.<br/>                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCustomPKCS10](enrollcustompkcs10.md)                           | Cria uma solicitação PKCS \# 10 personalizada, envia-a para uma AC (autoridade de certificação) autônomo e instala o certificado emitido no armazenamento [*de certificados.*](/windows/desktop/SecGloss/c-gly) [](/windows/desktop/SecGloss/c-gly)<br/> | C++<br/>      |
| [enrollCustomPKCS10 \_ 2](enrollcustompkcs10-2.md)                      | Cria uma solicitação PKCS \# 10 personalizada e tenta inscreveu-a em uma AC corporativa.<br/>                                                                                                                                                                                                                                                               | C++<br/>      |
| [enrollEOBOCMC](enrolleobocmc.md)                                     | Cria uma solicitação de certificado cmc em nome de outro usuário e registra o usuário em uma hierarquia de certificados.<br/>                                                                                                                                                                                                                                    | C++<br/>      |
| [enrollFromPublicKey](enrollfrompublickey.md)                         | Inicializa um objeto de solicitação de certificado PKCS 10, o envolve em um objeto de solicitação do CMC, envia a solicitação de CMC para uma AC corporativa e salva o certificado retornado pela AC em \# um arquivo.<br/>                                                                                                                                                      | C++<br/>      |
| [enrollKeyArchivalCMC](enrollkeyarchivalcmc.md)                       | Cria uma solicitação de certificado do CMC para arquivar [*uma chave privada*](/windows/desktop/SecGloss/p-gly) em uma AC.<br/>                                                                                                                                                                                                     | C++<br/>      |
| [enrollNestedCMC](enrollnestedcmc.md)                                 | Lê uma solicitação de certificado CMC existente de um arquivo, a envolve em outra solicitação do CMC, assina essa solicitação externa, envia-a para uma AC e salva a resposta do certificado da AC em um arquivo.<br/>                                                                                                                                                 | C++<br/>      |
| [enrollPKCS7](enrollpkcs7.md)                                         | Cria uma [*solicitação PKCS \# 7*](/windows/desktop/SecGloss/p-gly) de um certificado existente herdando as chaves públicas e privadas e o modelo de certificado. O exemplo registra o usuário em uma hierarquia de certificados e instala a resposta do certificado.<br/>                                   | C++<br/>      |
| [enrollRenewalPKCS7](enrollrenewalpkcs7.md)                           | Cria um objeto de \# solicitação PKCS 7 para renovar um certificado existente.<br/>                                                                                                                                                                                                                                                                             | C++<br/>      |
| [enrollSimpleMachineCert](enrollsimplemachinecert.md)                 | Registra um computador em uma hierarquia de certificados usando um modelo, um nome de exibição de certificado e a descrição do certificado.<br/>                                                                                                                                                                                                                 | C++, VBS<br/> |
| [enrollSimpleUserCert](enrollsimpleusercert.md)                       | Registra um usuário final com uma AC usando um modelo, o nome da assunto e o comprimento, em bits, da chave.<br/>                                                                                                                                                                                                                                       | C++, C #<br/> |
| [enrollWithIX509EnrollmentHelper](enrollwithix509enrollmenthelper.md) | Demonstra como usar o protocolo HTTP Windows 7 para registrar um certificado em uma AC corporativa.<br/>                                                                                                                                                                                                                                                | C#<br/>      |
| [installResponseFromPFX](installresponsefrompfx.md)                   | Instala um certificado inscrito de um arquivo PFX (Informações Exchange Pessoal) para o armazenamento de certificados.<br/>                                                                                                                                                                                                                                      | C++<br/>      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a API de Registro de Certificado](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

