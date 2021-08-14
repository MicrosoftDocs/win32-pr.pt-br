---
description: Mapeando certificados
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Mapeando certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f671afa6278da49427d0f7b49f78895198333e24d135383207b359846216638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921835"
---
# <a name="mapping-certificates"></a>Mapeando certificados

> [!Note]  
> As informações neste tópico são válidas somente para servidores que exigem autenticação de cliente.

 

Quando um aplicativo de servidor requer autenticação de cliente, o Schannel tenta mapear automaticamente o certificado fornecido pelo cliente para uma conta de usuário.

Depois que [*o contexto de segurança*](../secgloss/s-gly.md) tiver sido estabelecido, o aplicativo de servidor poderá usar a função [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) para obter um token de [*acesso*](../secgloss/a-gly.md) para a conta de usuário para a qual o certificado de [*cliente*](../secgloss/c-gly.md) foi mapeado. Além disso, o servidor pode usar a função [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) para representar o cliente.

Para obter mais informações sobre autenticação, consulte [executando a autenticação usando Schannel](performing-authentication-using-schannel.md).

 

 
