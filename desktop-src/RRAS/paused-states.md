---
title: Estados em pausa
description: Durante uma operação de conexão, pode haver ocasiões em que o servidor remoto não pode continuar sem informações adicionais do usuário local.
ms.assetid: a1a36b2a-33df-4cba-85a6-f4225779cd63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914acb85ccf74c92b4bd4119966a421faddeb011
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294455"
---
# <a name="paused-states"></a>Estados em pausa

Durante uma operação de conexão, pode haver ocasiões em que o servidor remoto não pode continuar sem informações adicionais do usuário local. A partir do Windows NT 3,5, a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) dá suporte a Estados pausados. Um estado de pausa permite que o Gerenciador de conexões de acesso remoto suspenda uma operação de conexão para que o aplicativo cliente RAS possa coletar informações do usuário.

Os Estados em pausa são úteis nas seguintes situações:

-   Quando o usuário precisa fornecer um número de [retorno de chamada](callback-connections.md) .
-   Quando a autenticação do usuário falha, o usuário pode digitar um nome de usuário e uma senha diferentes.
-   Quando a senha do usuário tiver expirado, o usuário poderá fornecer uma nova senha.

Por padrão, o suporte ao estado pausado está desabilitado. Os clientes RAS que desejam dar suporte a Estados pausados devem definir o \_ sinalizador RDEOPTS PausedStates na estrutura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) passada como um parâmetro para [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Quando ocorre um estado pausado, o Gerenciador de conexão de acesso remoto invoca o manipulador de notificação do cliente. Se o suporte a estado pausado estiver desabilitado, a mensagem de notificação indicará um erro e a operação de conexão falhará. Se estiver habilitado, o Gerenciador de conexões pausará a operação de conexão para aguardar a resposta do cliente RAS. O cliente RAS pode retomar a operação de conexão por uma segunda chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) ou finalizá-la chamando a função [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) .

Depois de obter a entrada do usuário, o cliente RAS reinicia a operação de conexão chamando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) novamente. Essa segunda chamada **RasDial** deve especificar as seguintes informações:

-   O identificador de conexão retornado pela chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.
-   O mesmo manipulador de notificação da chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.
-   A entrada do usuário nos membros apropriados da estrutura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) . Outros membros da estrutura **RASDIALPARAMS** devem ter as mesmas informações especificadas na chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.

A segunda chamada de [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) não pode ser feita de dentro do manipulador de notificação.

 

 