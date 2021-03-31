---
title: Outras informações de conexão
description: Os membros da estrutura RASDIALPARAMS também podem especificar as informações de conexão a seguir.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917411"
---
# <a name="other-connection-information"></a>Outras informações de conexão

Os membros da estrutura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) também podem especificar as informações de conexão a seguir.

-   Um número de telefone para substituir o número na entrada do catálogo telefônico.
-   Um número de telefone de [retorno](callback-connections.md) de chamada que o servidor remoto pode chamar de volta para estabelecer a conexão.
-   O nome do domínio de rede remota no qual a autenticação deve ocorrer.

Para o número de retorno de chamada e o domínio, os membros do [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) podem indicar que o RAS deve usar as informações na entrada do catálogo telefônico ou pode fornecer informações que substituam os dados do catálogo telefônico.

Um cliente RAS pode usar o parâmetro *lpRasDialExtensions* da função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para controlar se o RAS usa um prefixo ou sufixo de número de telefone especificado em uma entrada de catálogo telefônico.

 

 