---
description: Explica como validar as credenciais do Schannel manualmente.
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: Validando manualmente as credenciais do Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ec87b662cf9d3711c1ae729d2dd3b14ac5f79e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752009"
---
# <a name="manually-validating-schannel-credentials"></a>Validando manualmente as credenciais do Schannel

Por padrão, o Schannel valida o [*certificado do servidor*](../secgloss/s-gly.md) chamando a função [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) ; no entanto, se você tiver desabilitado esse recurso usando o \_ sinalizador de validação de credenciais necessárias do ISC \_ \_ \_ , você deverá validar o certificado fornecido pelo servidor que está tentando estabelecer sua identidade.

Para validar manualmente o certificado do servidor, primeiro você deve obtê-lo. Use a função [**QueryContextAttributes (geral)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) e especifique o \_ valor do \_ atributo de contexto de certificado remoto attr SECPKG \_ \_ . Esse atributo retorna uma estrutura de [**\_ contexto de certificado**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) que contém o certificado fornecido pelo servidor. Esse certificado é chamado de certificado de folha porque é o último certificado na cadeia de certificados e está mais longe do [*certificado raiz*](../secgloss/r-gly.md).

Usando o certificado de folha, você deve verificar o seguinte:

-   A cadeia de certificados está concluída e a raiz é um certificado de uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA) confiável.
-   A hora atual não está além das datas de início e de término de cada um dos certificados na cadeia de certificados.
-   Nenhum dos certificados na cadeia de certificados foi revogado.
-   A profundidade do certificado de folha não é mais profunda do que a profundidade máxima permitida especificada na extensão do certificado. Essa verificação só será necessária se houver uma profundidade especificada.
-   O uso do certificado está correto, por exemplo, um [*certificado de cliente*](../secgloss/c-gly.md) não deve ser usado para autenticar um servidor.
-   Para a autenticação de servidor, a identidade do servidor contida no certificado de folha do servidor corresponde ao servidor que o cliente está tentando contatar. Normalmente, o cliente corresponderá a algum item no campo nome da entidade do certificado para o endereço IP ou o nome DNS do servidor.

 

 
