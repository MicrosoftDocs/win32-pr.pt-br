---
title: Interação do protocolo de autenticação e ponto de acesso durante a autenticação
description: A função RasEapMakeMessage controla a maioria da interação entre o protocolo de autenticação e o AP (ponto de acesso).
ms.assetid: edc128e0-3104-4df9-80f4-b2aebcfe1087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aea18883225a2a34e592b73e0cdc93b019c1bf466124976f01851febb2a17d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117766"
---
# <a name="access-point-and-authentication-protocol-interaction-during-authentication"></a>Interação do protocolo de autenticação e ponto de acesso durante a autenticação

A função [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) controla a maioria da interação entre o protocolo de autenticação e o AP (ponto de acesso). O **RasEapMakeMessage** processa pacotes EAP de entrada e cria pacotes EAP para transmissão para o par remoto. Ele também processa eventos como tempo limite e conclusão de autenticação.

Se uma mensagem for recebida do ponto remoto, o serviço de autenticação AP chamará [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)), passando um ponteiro para a mensagem recebida no parâmetro *pReceivePacket* .

Se o serviço chamar [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) com *PReceivePacket* definido como **NULL**, o AP estará iniciando a caixa de diálogo com o protocolo de autenticação ou solicitando que o protocolo reenvie o último pacote. O protocolo de autenticação deve determinar qual ação o serviço está assumindo com base em seu estado e no contexto da mensagem.

No retorno de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)), o valor do membro **Action** da estrutura de [**\_ \_ saída PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) indica qual ação, se houver, o serviço de autenticação usa. O membro de **ação** recebe valores do tipo enumerado da [**\_ \_ ação EAP do PPP**](/windows/desktop/api/Raseapif/ne-raseapif-ppp_eap_action) .

Se **Action** for **EAPACTION \_ Send**, **EAPACTION \_ SendAndDone**, **EAPACTION \_ SendWithTimeout** ou **EAPACTION \_ SendWithTimeoutInteractive**, o serviço transmitirá o pacote apontado pelo parâmetro *pSendPacket* para o par remoto.

O valor de **\_ SendWithTimeout de EAPACTION** permite um tempo limite, após o qual o serviço de autenticação assume que o link foi perdido e desconecta a sessão.

O valor de **\_ SendWithTimeoutInteractive EAPACTION** permite que uma quantidade infinita de tempo limite ocorra. O autenticador deve usar esse valor ao esperar a entrada do usuário no cliente. Esse tempo limite permite que o usuário tenha um período de tempo não especificado para concluir a entrada necessária.

Se **Action** for **EAPACTION \_ SendWithTimeout** ou **EAPACTION \_ SendWithTimeoutInteractive**, o protocolo de autenticação deverá definir o membro **dwIdExpected** da estrutura de [**saída do \_ EAP \_ do PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) para o identificador do próximo pacote que é esperado do par remoto. Independentemente se o próximo pacote recebido do par corresponde a esse valor, o serviço de autenticação passa o pacote para o protocolo de autenticação em uma chamada subsequente para [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). O protocolo de autenticação pode descartar silenciosamente o pacote simplesmente retornando o **erro \_ \_ \_ pacote de PPP inválido**. Se um pacote com o identificador esperado não for recebido dentro do período de tempo limite configurado, o serviço de autenticação ainda chamará **RasEapMakeMessage**. Nesse caso, a chamada é feita com o parâmetro *pReceivePacket* definido como **NULL**, para indicar que o pacote anterior precisa ser enviado novamente.

Se o membro de **ação** for **EAPACTION \_ concluído** ou **EAPACTION \_ SendAndDone**, o serviço de autenticação examinará o membro **dwAuthResultCode** da [**\_ \_ saída PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). Se **dwAuthResultCode** não for um \_ erro, a autenticação foi bem-sucedida. Se **dwAuthResultCode** for um valor diferente de nenhum \_ erro, a autenticação falhará. O código de erro retornado para o caso de falha deve vir de Raserror. h, Mprerror. h ou Winerror. h. Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte:

-   ERRO \_ sem \_ permissão de discagem \_
-   ERRO \_ passwd \_ expirado
-   ERRO de \_ Acct \_ desabilitado
-   \_horário de \_ logon \_ restrito de erro
-   ERRO \_ interno de autenticação \_

No caso em que **Action** é **EAPACTION \_ Done** ou **EAPACTION \_ SendAndDone**, o membro **pUserAttributes** deve apontar para atributos que substituem atributos do mesmo tipo que foram passados para o servidor na chamada para [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).

O protocolo de autenticação no servidor pode solicitar que o serviço de autenticação invoque o provedor de autenticação atual retornando **EAPACTION \_ Authenticate** no membro de **ação** na [**\_ \_ saída PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). Nesse caso, o ponteiro **pUserAttributes** na **saída PPP \_ EAP \_** aponta apenas para atributos que foram gerados pelo protocolo de autenticação no servidor. Ele não inclui nenhum dos atributos que foram passados para o servidor na chamada para [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). O provedor de autenticação não requer esses atributos iniciais porque as credenciais de autenticação estão dentro da mensagem EAP em si, não em um atributo RADIUS separado. Quando o serviço de autenticação responde à ação de autenticação **EAPACTION \_** , **pUserAttributes** na [**\_ \_ entrada EAP do PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), aponta para todos os atributos gerados durante a autenticação. Esses atributos são retornados para o protocolo de autenticação no cliente.

Se o protocolo de autenticação usar **EAPACTION \_ autenticar**, o provedor de autenticação executará o PAP ou o MD5-CHAP. esse método de autenticação pode ser usado somente com clientes Windows.

Se o protocolo de autenticação autenticar o usuário sem depender de um provedor de autenticação, não será necessário que o protocolo defina a **ação** como **EAPACTION \_ autenticar**. Um exemplo desse caso é o TLS (segurança de camada) EAP-Transport.

O pacote de êxito do EAP é um pacote não reconhecido. Portanto, ele pode ser perdido e não enviado pelo servidor. Se o serviço de autenticação no cliente receber um pacote de protocolo de controle de rede (NCP), o serviço de autenticação do lado do servidor continuará como se a autenticação tivesse êxito. Isso ocorre porque o servidor passou para a fase NCP do PPP. De acordo, o serviço de autenticação chama [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) com o membro **fSuccessPacketReceived** da estrutura de [**\_ \_ entrada PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) definida como **true**.

Durante o curso da sessão de autenticação, o protocolo de autenticação pode exigir a interação diretamente com o usuário no cliente. O fornecedor do protocolo de autenticação pode fornecer uma interface do usuário interativa para essa finalidade. O protocolo de autenticação pode solicitar que o serviço exiba a interface do usuário interativa definindo os membros **fInvokeInteractiveUI**, **pUIContextData** e **dwSizeOfUIContextData** na estrutura de [**saída do \_ EAP \_ do PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) . Para obter mais informações sobre como usar uma interface do usuário interativa, consulte [Interactive user interface](interactive-user-interface.md).

O protocolo de autenticação deve exibir uma interface do usuário somente por meio do mecanismo descrito em [interface do usuário interativo](interactive-user-interface.md). Se o próprio protocolo de autenticação exibir a interface do usuário, o thread PPP será bloqueado até que a interface do usuário seja ignorada.

Se, durante o processo de autenticação, [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) retornar qualquer valor diferente de **sem \_ erro ou um** **pacote de erro \_ PPP \_ inválido \_**, a sessão será desconectada e o erro será registrado (no servidor) ou exibido para o usuário (no cliente).

 

 