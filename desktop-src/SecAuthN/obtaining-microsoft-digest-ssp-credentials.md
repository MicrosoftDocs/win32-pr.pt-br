---
description: As credenciais do usuário são exigidas pelo Microsoft Digest; o cliente e o servidor devem apresentar credenciais válidas antes que possam estabelecer um contexto de segurança para a troca de mensagens. Os identificadores de credenciais são usados para obter e apresentar as credenciais.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Obtendo credenciais do Microsoft Digest SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461057"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a>Obtendo credenciais do Microsoft Digest SSP

[*As credenciais*](../secgloss/c-gly.md) do usuário são exigidas pelo Microsoft Digest; o cliente e o servidor devem apresentar credenciais válidas antes que possam estabelecer um [*contexto de segurança*](../secgloss/s-gly.md) para a troca de mensagens. Os identificadores de credenciais são usados para obter e apresentar as credenciais.

Como o identificador de credencial é usado para armazenar informações de configuração, o mesmo identificador não pode ser usado para operações do lado do cliente e do servidor. Isso significa que os aplicativos que dão suporte a conexões de cliente e de servidor devem obter um mínimo de duas identificadores de credenciais.

Para obter um identificador para as credenciais exigidas pelo Microsoft Digest, chame a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .

Os exemplos de linguagem C a seguir demonstram como obter credenciais.

-   [Obtendo credenciais de resumo padrão](obtaining-default-digest-credentials.md)
-   [Obtendo credenciais de resumo alternativas](obtaining-alternate-digest-credentials.md)

 

 
