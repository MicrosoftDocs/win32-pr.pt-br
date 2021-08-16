---
description: Explica como validar as credenciais Schannel manualmente.
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: Validando manualmente as credenciais do Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71ddff50ab674825d8effd1a08477116ee0c654d031e7f353a30c95e4f1249f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786998"
---
# <a name="manually-validating-schannel-credentials"></a>Validando manualmente as credenciais do Schannel

Por padrão, o Schannel valida o certificado [*do servidor*](../secgloss/s-gly.md) chamando a [**função WinVerifyTrust;**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) no entanto, se você tiver desabilitado esse recurso usando o sinalizador DE VALIDAÇÃO DE CRED MANUAL DO ISC REQ, deverá validar o certificado fornecido pelo servidor que está tentando \_ \_ estabelecer sua \_ \_ identidade.

Para validar manualmente o certificado do servidor, você deve primeiro obter. Use a [**função QueryContextAttributes (Geral)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) e especifique o valor do atributo CONTEXT DO CERTIFICADO \_ REMOTO SECPKG \_ ATTR. \_ \_ Esse atributo retorna uma [**estrutura CONTEXT \_ CERT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) que contém o certificado fornecido pelo servidor. Esse certificado é chamado de certificado folha porque é o último certificado na cadeia de certificados e está mais distante do [*certificado raiz.*](../secgloss/r-gly.md)

Usando o certificado folha, você deve verificar o seguinte:

-   A cadeia de certificados está concluída e a raiz é um certificado de uma AC (autoridade [*de certificação)*](../secgloss/c-gly.md) confiável.
-   A hora atual não está além das datas de início e término de cada um dos certificados na cadeia de certificados.
-   Nenhum dos certificados na cadeia de certificados foi revogado.
-   A profundidade do certificado folha não é mais profunda do que a profundidade máxima permitida especificada na extensão do certificado. Essa verificação só será necessária se houver uma profundidade especificada.
-   O uso do certificado está correto, por exemplo, um certificado [*do cliente*](../secgloss/c-gly.md) não deve ser usado para autenticar um servidor.
-   Para autenticação de servidor, a identidade do servidor contida no certificado folha do servidor corresponde ao servidor que o cliente está tentando contatar. Normalmente, o cliente corresponderá a algum item no campo Nome da Assunto do certificado com o endereço IP do servidor ou o nome DNS.

 

 
