---
title: Estados em pausa
description: Durante uma operação de conexão, pode haver ocasiões em que o servidor remoto não pode continuar sem informações adicionais do usuário local.
ms.assetid: a1a36b2a-33df-4cba-85a6-f4225779cd63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec66a63adbee524ec231b5c9dd9b0b410c8f4fbc73746ae9b924294c680b4a9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029136"
---
# <a name="paused-states"></a>Estados em pausa

Durante uma operação de conexão, pode haver ocasiões em que o servidor remoto não pode continuar sem informações adicionais do usuário local. Começando com Windows NT 3.5, a [**função RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) dá suporte a estados em pausa. Um estado em pausa permite que o Gerenciador de Conexões remoto suspenda uma operação de conexão para que o aplicativo cliente RAS possa coletar informações do usuário.

Os estados em pausa são úteis nas seguintes situações:

-   Quando o usuário precisa fornecer um número [de retorno de](callback-connections.md) chamada.
-   Quando a autenticação do usuário falhar, o usuário poderá digitar um nome de usuário e uma senha diferentes.
-   Quando a senha do usuário tiver expirado, o usuário poderá fornecer uma nova senha.

Por padrão, o suporte a estado em pausa está desabilitado. Os clientes RAS que querem dar suporte a estados em pausa devem definir o sinalizador PausedStates TORIALOPTS na estrutura \_ [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) passada como um parâmetro para [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Quando ocorre um estado em pausa, o Gerenciador de Conexões remoto invoca o manipulador de notificação do cliente. Se o suporte de estado em pausa estiver desabilitado, a mensagem de notificação indicará um erro e a operação de conexão falhará. Se ele estiver habilitado, o Gerenciador de Conexões pausa a operação de conexão para aguardar a resposta do cliente RAS. O cliente RAS pode retomar a operação de conexão por uma segunda [**chamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) ou encentá-la chamando a [**função Ras Tabulação.**](/windows/desktop/api/Ras/nf-ras-rashangupa)

Depois de obter a entrada do usuário, o cliente RAS reinicia a operação de conexão chamando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) novamente. Esta segunda **chamada RasDial** deve especificar as seguintes informações:

-   O alça de conexão que foi retornado pela chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.
-   O mesmo manipulador de notificação que a [**chamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.
-   A entrada do usuário nos membros apropriados da [**estrutura RASDIALPARAMS.**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) Outros membros da **estrutura RASDIALPARAMS** devem ter as mesmas informações especificadas na chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.

A segunda [**chamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) não pode ser feita de dentro do manipulador de notificação.

 

 