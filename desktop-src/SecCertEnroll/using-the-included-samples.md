---
description: A API de registro de certificado inclui vários exemplos criados para ajudá-lo a criar aplicativos personalizados. A maioria dos exemplos são escritos usando C++, mas exemplos de C# e Visual Basic Scripting Edition (VBScript) também estão incluídos.
ms.assetid: 70ac7b75-542c-4d79-85ce-4b1bac414879
title: Usando os exemplos incluídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3cbf17d35e65ade52e97438d638cbd4f1489e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755958"
---
# <a name="using-the-included-samples"></a>Usando os exemplos incluídos

A API de registro de certificado inclui vários exemplos criados para ajudá-lo a criar aplicativos personalizados. A maioria dos exemplos são escritos usando C++, mas exemplos de C# e Visual Basic Scripting Edition (VBScript) também estão incluídos.

Quando você instala o SDK (Kit de desenvolvimento de software) do Microsoft Windows, os exemplos a seguir são instalados, por padrão, na pasta de registro de certificado X509 do *% ProgramFiles%* resoftwares \\ \\ Windows \\ v 7.0 \\ \\ \\ \\ .



| Amostra                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                | Idioma            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [createCNGCustomCMC](createcngcustomcmc.md)                           | Cria um objeto de solicitação CMC com base em uma solicitação PKCS 10 aninhada interna \# .<br/>                                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCommon](enrollcommon.md)                                       | Contém as seguintes funções auxiliares e macros usadas pelos exemplos incluídos.<br/>                                                                                                                                                                                                                                                                | C++<br/>      |
| [enrollCustomCMC](enrollcustomcmc.md)                                 | Cria uma solicitação de certificado CMC e registra um computador em uma hierarquia de certificado.<br/>                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCustomPKCS10](enrollcustompkcs10.md)                           | Cria uma solicitação PKCS \# 10 personalizada, envia-a para uma CA ( [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) ) autônoma e instala o certificado emitido no [*repositório de certificados*](/windows/desktop/SecGloss/c-gly).<br/> | C++<br/>      |
| [enrollCustomPKCS10 \_ 2](enrollcustompkcs10-2.md)                      | Cria uma solicitação personalizada de PKCS \# 10 e tenta registrá-la em uma AC corporativa.<br/>                                                                                                                                                                                                                                                               | C++<br/>      |
| [enrollEOBOCMC](enrolleobocmc.md)                                     | Cria uma solicitação de certificado CMC em nome de outro usuário e registra o usuário em uma hierarquia de certificado.<br/>                                                                                                                                                                                                                                    | C++<br/>      |
| [enrollFromPublicKey](enrollfrompublickey.md)                         | Inicializa um \# objeto de solicitação de certificado PKCS 10, o encapsula em um objeto de solicitação CMC, envia a solicitação CMC para uma AC corporativa e salva o certificado retornado pela autoridade de certificação em um arquivo.<br/>                                                                                                                                                      | C++<br/>      |
| [enrollKeyArchivalCMC](enrollkeyarchivalcmc.md)                       | Cria uma solicitação de certificado CMC para arquivar uma [*chave privada*](/windows/desktop/SecGloss/p-gly) em uma autoridade de certificação.<br/>                                                                                                                                                                                                     | C++<br/>      |
| [enrollNestedCMC](enrollnestedcmc.md)                                 | Lê uma solicitação de certificado CMC existente de um arquivo, a encapsula em outra solicitação de CMC, assina essa solicitação externa, envia-a para uma CA e salva a resposta do certificado da autoridade de certificação em um arquivo.<br/>                                                                                                                                                 | C++<br/>      |
| [enrollPKCS7](enrollpkcs7.md)                                         | Cria uma solicitação [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) de um certificado existente herdando as chaves pública e privada e o modelo de certificado. O exemplo registra o usuário em uma hierarquia de certificado e instala a resposta do certificado.<br/>                                   | C++<br/>      |
| [enrollRenewalPKCS7](enrollrenewalpkcs7.md)                           | Cria um \# objeto de solicitação PKCS 7 para renovar um certificado existente.<br/>                                                                                                                                                                                                                                                                             | C++<br/>      |
| [enrollSimpleMachineCert](enrollsimplemachinecert.md)                 | Registra um computador em uma hierarquia de certificado usando um modelo, um nome de exibição de certificado e a descrição do certificado.<br/>                                                                                                                                                                                                                 | C++, VBS<br/> |
| [enrollSimpleUserCert](enrollsimpleusercert.md)                       | Registra um usuário final com uma AC usando um modelo, o nome da entidade e o comprimento, em bits, da chave.<br/>                                                                                                                                                                                                                                       | C++, C #<br/> |
| [enrollWithIX509EnrollmentHelper](enrollwithix509enrollmenthelper.md) | Demonstra como usar o protocolo HTTP do Windows 7 para registrar um certificado em uma autoridade de certificação corporativa.<br/>                                                                                                                                                                                                                                                | C#<br/>      |
| [installResponseFromPFX](installresponsefrompfx.md)                   | Instala um certificado registrado de um arquivo de troca de informações pessoais (PFX) no repositório de certificados.<br/>                                                                                                                                                                                                                                      | C++<br/>      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a API de registro de certificado](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

