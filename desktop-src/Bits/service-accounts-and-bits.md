---
title: Contas de serviço e BITS
description: Você pode usar BITS para transferir arquivos de um serviço. O serviço deve usar a conta do sistema LocalSystem, LocalService ou NetworkService. Essas contas estão sempre conectadas; Portanto, os trabalhos enviados por um serviço usando essas contas sempre são executados.
ms.assetid: 43fb58d6-3a99-488f-ab43-dbb4a794fc2f
keywords:
- BITS de contas de serviço
- transferir BITS de trabalho, propriedade, conta de serviço
- BITS de proxy, contas de serviço
- credenciais para transferir BITS de trabalho
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 475a623e6b105d3ef2bdc6586db613c010fe8923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084627"
---
# <a name="service-accounts-and-bits"></a>Contas de serviço e BITS

Você pode usar BITS para transferir arquivos de um serviço. O serviço deve usar a conta do sistema LocalSystem, LocalService ou NetworkService. Essas contas estão sempre conectadas; Portanto, os trabalhos enviados por um serviço usando essas contas sempre são executados.

Se um serviço em execução em uma conta do sistema representar o usuário antes de chamar BITS, o BITS responderá como faria para qualquer conta de usuário (por exemplo, o usuário precisa estar conectado ao computador para que a transferência ocorra). O serviço também deve usar o encobrimento dinâmico com os ponteiros de interface do BITS ao representar o usuário. O encobrimento não é herdado, portanto, você deve chamar a função [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) em cada ponteiro de interface que você recebe de bits (por exemplo, o ponteiro do trabalho retornado da chamada do método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) ); Não é suficiente definir o encobrimento no ponteiro da interface do Gerenciador. Você também pode chamar a função [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para o processo em vez de chamar a função **CoSetProxyBlanket** em cada ponteiro de interface.

No entanto, se o serviço não representar o usuário, os seguintes comportamentos se aplicarão:

- Os trabalhos criados pela conta de serviço pertencem a essa conta. Como as contas do sistema estão sempre conectadas, o BITS transfere os arquivos desde que o computador esteja em execução e haja uma conexão de rede.
- As contas do sistema não devem usar letras de unidade de rede mapeadas porque as letras da unidade são específicas a uma sessão e o mapeamento pode ser perdido após a reinicialização do computador.
- Na ausência de um [token auxiliar](helper-tokens-for-bits-transfer-jobs.md), a autenticação de rede usa credenciais de computador para contas LocalSystem e NetworkService e credenciais anônimas para a conta LocalService. O BITS retornará "acesso negado" se a ACL (lista de controle de acesso) do arquivo de origem limitar o acesso a uma conta de usuário.
- Para obter detalhes sobre como a autenticação funciona na presença de um [token auxiliar](helper-tokens-for-bits-transfer-jobs.md), consulte [autenticação](authentication.md).
- As configurações de proxy do Microsoft Internet Explorer são armazenadas por usuário e não são definidas para contas do sistema. Considere configurar um token auxiliar em seus trabalhos do BITS ou definir explicitamente as configurações de proxy corretas chamando [**método ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) com a substituição de uso de **proxy de \_ trabalho \_ \_ \_ BG**. Como alternativa, você pode usar os comutadores **/util/SetIEProxy** da BitsAdmin.exe para definir as configurações de proxy do Internet Explorer para a conta do sistema LocalSystem, LocalService ou NetworkService. Para obter detalhes, consulte [ferramenta BitsAdmin](bitsadmin-tool.md).

Observe que o BITS não reconhece as configurações de proxy que são definidas usando o arquivo Proxycfg.exe.