---
title: Contas de serviço e BITS
description: Você pode usar o BITS para transferir arquivos de um serviço. O serviço deve usar a conta do sistema LocalSystem, LocalService ou NetworkService. Essas contas estão sempre registradas; portanto, os trabalhos enviados por um serviço usando essas contas sempre são executados.
ms.assetid: 43fb58d6-3a99-488f-ab43-dbb4a794fc2f
keywords:
- bits de contas de serviço
- transferir trabalho BITS , propriedade, conta de serviço
- proxy BITS , contas de serviço
- credenciais para transferir bits de trabalho
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: a996471afefb00b0dea87b07f477f5cab2fd29352c567dc9182fcf28fa5b168a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679898"
---
# <a name="service-accounts-and-bits"></a>Contas de serviço e BITS

Você pode usar o BITS para transferir arquivos de um serviço. O serviço deve usar a conta do sistema LocalSystem, LocalService ou NetworkService. Essas contas estão sempre registradas; portanto, os trabalhos enviados por um serviço usando essas contas sempre são executados.

Se um serviço em execução em uma conta do sistema representar o usuário antes de chamar BITS, o BITS responderá como faria com qualquer conta de usuário (por exemplo, o usuário precisa estar conectado ao computador para que a transferência ocorra). O serviço também deve usar a replicação dinâmica com os ponteiros da interface BITS ao representar o usuário. A ocultação não é herdada, portanto, você deve chamar a função [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) em cada ponteiro de interface que você recebe do BITS (por exemplo, o ponteiro de trabalho retornado da chamada ao método [**IBackgroundCopyManager::CreateJob);**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) não é suficiente definir a replicação no ponteiro da interface do gerenciador. Você também pode chamar a [**função CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para o processo em vez de chamar a **função CoSetProxyBlanket** em cada ponteiro de interface.

No entanto, se o serviço não representar o usuário, os seguintes comportamentos se aplicarão:

- Os trabalhos criados pela conta de serviço pertencem a essa conta. Como as contas do sistema estão sempre conectados, o BITS transfere os arquivos, desde que o computador seja executado e haja uma conexão de rede.
- As contas do sistema não devem usar letras de unidade de rede mapeadas porque as letras da unidade são específicas de uma sessão e o mapeamento pode ser perdido após uma reinicialização do computador.
- Na ausência de um [Token](helper-tokens-for-bits-transfer-jobs.md)Auxiliar, a autenticação de rede usa credenciais de computador para contas LocalSystem e NetworkService e credenciais anônimas para a conta LocalService. O BITS retornará "acesso negado" se a ACL (lista de controle de acesso) do arquivo de origem limitar o acesso a uma conta de usuário.
- Para obter detalhes sobre como a autenticação funciona na presença de um [Token Auxiliar,](helper-tokens-for-bits-transfer-jobs.md)consulte [Autenticação](authentication.md).
- As Internet Explorer proxy do Microsoft Internet Explorer são armazenadas por usuário e não são definidas para contas do sistema. Considere configurar um token auxiliar em seus trabalhos bits ou definir explicitamente as configurações de proxy corretas chamando [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) com **BG \_ JOB PROXY USAGE \_ \_ \_ OVERRIDE**. Como alternativa, você pode usar as opções **/Util /SetIEProxy** do BitsAdmin.exe para definir Internet Explorer configurações de proxy para a conta do sistema LocalSystem, LocalService ou NetworkService. Para obter detalhes, consulte [BitsAdmin Tool](bitsadmin-tool.md).

Observe que o BITS não reconhece as configurações de proxy definidas usando o arquivo Proxycfg.exe servidor.