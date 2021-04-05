---
description: Mapeando certificados
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Mapeando certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662741"
---
# <a name="mapping-certificates"></a>Mapeando certificados

> [!Note]  
> As informações neste tópico são válidas somente para servidores que exigem autenticação de cliente.

 

Quando um aplicativo de servidor requer autenticação de cliente, o Schannel tenta mapear automaticamente o certificado fornecido pelo cliente para uma conta de usuário.

Depois que [*o contexto de segurança*](../secgloss/s-gly.md) tiver sido estabelecido, o aplicativo de servidor poderá usar a função [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) para obter um token de [*acesso*](../secgloss/a-gly.md) para a conta de usuário para a qual o certificado de [*cliente*](../secgloss/c-gly.md) foi mapeado. Além disso, o servidor pode usar a função [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) para representar o cliente.

Para obter mais informações sobre autenticação, consulte [executando a autenticação usando Schannel](performing-authentication-using-schannel.md).

 

 
