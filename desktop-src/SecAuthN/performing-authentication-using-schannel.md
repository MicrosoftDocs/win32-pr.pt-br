---
description: Todos os protocolos Schannel exigem que o servidor forneça um certificado de uma AC (autoridade de certificação) confiável como prova de sua identidade.
ms.assetid: 060981e0-b52a-4cc2-bfd2-4cf24f921f16
title: Executando a autenticação usando Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c2a5099dd29d6b3b342b583e37e2dc98187f5011c7cc75b75432924fba9ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921015"
---
# <a name="performing-authentication-using-schannel"></a>Executando a autenticação usando Schannel

Todos os protocolos Schannel exigem que o servidor forneça um [*certificado*](../secgloss/c-gly.md) de uma AC ( [*autoridade de certificação*](../secgloss/c-gly.md) ) confiável como prova de sua identidade. Esse processo é chamado de autenticação de servidor. A autenticação de cliente, em que o cliente fornece a prova de sua identidade, é opcional e pode ser solicitada pelo servidor a qualquer momento.

## <a name="authenticating-the-server"></a>Autenticando o servidor

O comportamento padrão do Schannel é usar a função [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) para verificar a [*integridade*](../secgloss/i-gly.md) e a propriedade do [*certificado do servidor*](../secgloss/s-gly.md). Para desabilitar esse recurso, especifique \_ \_ \_ \_ a validação de credenciais do ISC req manual ao chamar a função [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) . Para obter mais informações, consulte [Validando manualmente as credenciais do Schannel](manually-validating-schannel-credentials.md).

## <a name="authenticating-the-client"></a>Autenticando o cliente

O Schannel não valida os certificados do cliente; o servidor deve executar essa autenticação manualmente. Normalmente, o servidor verificará a identidade do cliente em um banco de dados que contém informações de conta de usuário. Para servidores que precisam obter a conta de um cliente usando um certificado, consulte [Mapeando certificados](mapping-certificates.md).

Quando o servidor solicita a autenticação de cliente, o cliente deve enviar um de seus certificados ao servidor. Por padrão, o Schannel será, sem notificação para o cliente, tentará localizar um [*certificado de cliente*](../secgloss/c-gly.md) e enviá-lo ao servidor. Para desabilitar esse recurso, os clientes especificam \_ \_ \_ credenciais de ISC usam \_ creds fornecidas ao chamar a função [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) . Quando esse sinalizador for especificado, o Schannel retornará a \_ s \_ credenciais incompletas \_ para o cliente quando o servidor solicitar autenticação e o cliente não tiver fornecido um certificado anteriormente.

 

 
