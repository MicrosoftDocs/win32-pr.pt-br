---
description: O servidor envia ao cliente uma referência para o contexto de segurança compartilhado usando a diretiva opaca do desafio de resumo.
ms.assetid: 543c4bed-b224-4da7-9746-12c9993a40af
title: Autenticando solicitações subsequentes com Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25954612a99fa0a0a9710f5e8e0679948cc3bac5ceae669a06ec40bd5c22241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101416"
---
# <a name="authenticating-subsequent-requests-with-microsoft-digest"></a>Autenticando solicitações subsequentes com Microsoft Digest

O servidor envia ao cliente uma referência para o [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) compartilhado usando a diretiva opaca do desafio de resumo. Após uma autenticação bem-sucedida, o cliente deve especificar esse valor em solicitações subsequentes para o servidor de destino. Incluir o valor opaco em solicitações de recursos que são acessíveis usando o contexto de segurança existente elimina a necessidade de autenticar novamente no controlador de domínio. Essas solicitações são autenticadas novamente no servidor, usando a [*chave de sessão*](/windows/desktop/SecGloss/s-gly) Digest armazenada em cache após a autenticação inicial.

O diagrama a seguir ilustra as etapas tomadas pelo cliente e pelo servidor durante uma solicitação subsequente para recursos protegidos por acesso.

![Autenticando solicitações subsequentes usando o Microsoft Digest](images/digest2.png)

Para solicitar recursos adicionais após uma autenticação bem-sucedida, o cliente chama a função Microsoft Digest [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para gerar uma resposta de desafio de resumo. O valor opaco é incluído na diretiva opaca da resposta de desafio enviada ao servidor como um cabeçalho de autorização (mostrado como solicitação HTTP).

O servidor chama a função [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) para determinar se há um contexto de [*segurança*](/windows/desktop/SecGloss/s-gly) existente para o cliente. Quando um contexto existente é encontrado, a função retorna s \_ E \_ completo \_ necessário para indicar que o servidor deve chamar a função [**CompleteAuthToken**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) . Essa função executa a autenticação de cliente usando a [*chave de sessão*](/windows/desktop/SecGloss/s-gly) Digest armazenada em cache durante a [autenticação inicial](initial-authentication-using-microsoft-digest.md) em vez de autenticar novamente no controlador de domínio.

 

 
