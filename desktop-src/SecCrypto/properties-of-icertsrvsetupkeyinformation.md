---
description: As propriedades a seguir são definidas pela interface ICertSrvSetupKeyInformation.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Propriedades de ICertSrvSetupKeyInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828557"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a>Propriedades de ICertSrvSetupKeyInformation

As propriedades a seguir são definidas pela interface [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) .



| Propriedade                                                                           | Descrição                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContainerName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | Obtém ou define o nome usado pelo CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) para gerar, armazenar ou acessar a chave.                                                                       |
| [**Existente**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | Obtém ou define um valor que indica se a chave privada já existe.                                                                                                                                                                                                                       |
| [**ExistingCACertificate**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | Obtém ou define o valor binário que foi codificado usando [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) e que é o valor binário do certificado de autoridade de certificação que corresponde a uma chave existente. |
| [**HashAlgorithm**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | Obtém ou define o nome do algoritmo de hash usado para assinar ou verificar o certificado de autoridade de certificação para a chave.                                                                                                                                                                                                |
| [**Comprimento**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | Obtém ou define a intensidade da chave para um dos valores com suporte pelo CSP.                                                                                                                                                                                                                   |
| [**ProviderName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | Obtém ou define o nome do CSP que é usado para gerar ou armazenar a chave privada.                                                                                                                                                                                                               |



 

 

 
