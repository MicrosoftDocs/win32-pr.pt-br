---
description: Sessões de áudio
ms.assetid: b8a1b656-a582-4112-99e9-bd575719ebb3
title: Sessões de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d5b8cee0a3a53709d2c450bef36ae00e3a6f4d9323c75ff80e96b19550eb39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929406"
---
# <a name="audio-sessions"></a>Sessões de áudio

Uma *sessão de áudio* é um grupo de fluxos de áudio relacionados que um cliente WASAPI pode gerenciar coletivamente. Os clientes podem controlar o nível de volume e o estado de mudo de cada sessão individual. O sistema aplica o volume especificado pelo cliente e as configurações de mudo uniformemente a todos os fluxos na sessão.

Quando um cliente Inicializa um fluxo de áudio, ele atribui o fluxo de áudio a uma sessão de áudio. Para obter mais informações, consulte [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).

Uma sessão de áudio contém fluxos de renderização ou fluxos de captura, mas não ambos. Por padrão, as configurações de volume e mudo para uma sessão de renderização são persistentes entre as reinicializações do sistema. As configurações de volume e mudo para uma sessão de captura não são persistentes. (Uma sessão que contém fluxos que operam no modo de loopback é tratada da mesma forma que uma sessão de captura. Ou seja, as configurações de sessão não são persistentes. Para obter mais informações sobre o modo de loopback, consulte [gravação de loopback](loopback-recording.md).)

Cada fluxo de áudio pertence a exatamente uma sessão. Um cliente atribui um fluxo de áudio a uma sessão específica no momento em que ele inicializa o objeto de fluxo. O fluxo retém sua associação na sessão durante o tempo de vida do fluxo. Depois que um objeto de fluxo é criado, o objeto existe até que um cliente libere a última referência contada para o objeto e, em seguida, o objeto seja excluído.

Embora um cliente não possa alterar a sessão à qual um fluxo existente é atribuído, ele pode obter um efeito semelhante ao excluir o fluxo (liberando todas as referências a ele), criando um novo fluxo para substituir o fluxo excluído e atribuir o novo fluxo a outra sessão.

Cada sessão de renderização representa um subconjunto dos fluxos que formam a combinação global que é reproduzida por meio de um [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md)específico. A combinação global combina todas as sessões de todos os aplicativos que compartilham o dispositivo.

Frequentemente, um aplicativo com vários fluxos atribui todos os seus fluxos à mesma sessão. No entanto, o aplicativo pode, como uma opção, atribuir fluxos diferentes a sessões diferentes. Qualquer fluxo que o aplicativo não atribui explicitamente a uma sessão pertence à sessão padrão.

Os aplicativos de áudio típicos devem evitar modificar as configurações de volume e mudo para as sessões. Em vez disso, os usuários controlam essas configurações por meio das interfaces de usuário dos programas de controle. por exemplo, no Windows Vista, o programa fornecido pelo sistema, Sndvol.exe, exibe um controle de volume e controle de mudo para cada sessão de renderização ativa ou recentemente ativa no sistema. Por meio desses controles, os usuários podem ajustar as configurações de volume e mudo para todas as sessões no sistema.

Atualmente, o programa SNDVOL exibe controles de volume somente para dispositivos de ponto de extremidade de renderização de áudio. Ele não exibe controles de volume para dispositivos de captura de áudio.

Uma sessão estará ativa se contiver um ou mais fluxos ativos. Um fluxo ativo está no *estado executando*. Um fluxo inativo está no *estado parado*. Uma sessão fica ativa quando seu primeiro fluxo se torna ativo. Uma sessão se torna inativa quando seu último fluxo ativo se torna inativo. Depois que uma sessão esteve inativa por um período de tempo, o sistema altera o estado da sessão de inativo para expirado.

SNDVOL exibe os controles de volume e sem áudio para todas as sessões de renderização ativas e inativas. SNDVOL remove os controles de volume e de mudo de uma sessão quando o estado da sessão é alterado de inativo para expirado ou quando a sessão é encerrada. (Uma sessão é encerrada quando o último de seus fluxos é excluído; ou seja, quando um cliente libera a contagem de referência final no último objeto de fluxo restante na sessão.) A única exceção a essa regra é para sons de notificação do sistema. O SNDVOL sempre exibe os controles de volume e mudo para sons de notificação do sistema, independentemente do estado da sessão para esses sons.

Normalmente, um fluxo pertence a uma sessão que abrange apenas o processo que contém o aplicativo que criou o fluxo. No entanto, os aplicativos têm a opção de definir sessões entre processos que combinam fluxos de dois ou mais processos.

O WASAPI dá suporte a sessões entre processos principalmente para que:

-   O programa SNDVOL pode apresentar ao usuário um único controle de volume para gerenciar sons de notificação do sistema em todos os aplicativos.
-   Um player de mídia executado em um processo pode transmitir conteúdo protegido para um programa de descriptografia que é executado em outro processo.

Semelhante às configurações de controle para sessões de renderização específicas do processo, as configurações de controle para sessões de processamento entre processos são, por padrão, persistentes entre as reinicializações do sistema. O WASAPI fornece esse comportamento principalmente para o benefício de sons de notificação do sistema, que deve manter as configurações de volume e mudo do usuário à medida que a combinação de aplicativos varia ao longo do tempo.

O programa SNDVOL rotula o controle de volume para cada sessão com um nome de exibição e um ícone. Um cliente tem a opção de atribuir explicitamente um nome de exibição e um ícone a uma sessão. Se o cliente não fornecer esses itens, SNDVOL exibirá um nome padrão e o ícone padrão em vez disso. O nome padrão incorpora informações como o título da janela do aplicativo. O ícone padrão é o ícone para a janela do aplicativo. Somente no caso de sessões específicas do processo, esses padrões fornecem informações significativas para os usuários. Observe que uma sessão entre processos pode ser associada a mais de um aplicativo. Nesse caso, apenas um nome de exibição e ícone fornecidos pelo cliente são significativos.

Embora as configurações de volume e mudo para uma sessão de renderização sejam, por padrão, persistentes entre as reinicializações do sistema, o nome de exibição e o ícone fornecidos pelo cliente não são. Para garantir que o SNDVOL exiba o nome e o ícone fornecidos pelo cliente, o cliente deve atribuir explicitamente o nome e o ícone à sessão no momento em que o cliente atribui o primeiro fluxo à sessão. O sistema retém o nome de exibição e o ícone para uma sessão somente até que a sessão seja encerrada.

Cada sessão é identificada por um GUID de sessão. No momento em que um cliente abre um fluxo, o cliente atribui esse fluxo a uma sessão específica. O cliente fornece as duas informações a seguir para identificar essa sessão:

-   Um GUID de sessão.
-   Se a sessão é uma sessão de processo cruzado ou específico do processo — uma sessão específica do processo contém apenas fluxos do processo do cliente.

Essas informações são suficientes para distinguir uma sessão específica de todas as outras sessões no mesmo computador. O GUID de sessão para uma sessão específica de processo identifica exclusivamente a sessão somente dentro do escopo do processo que possui a sessão. Por outro lado, o GUID de sessão para uma sessão de processo cruzado é exclusivo dentro do escopo de todos os processos em execução no computador.

No caso de uma sessão específica de processo, o sistema usa uma combinação de GUID de sessão e ID de processo para identificar exclusivamente a sessão dentro do escopo do computador. Portanto, se os clientes em dois processos diferentes atribuirem seus respectivos fluxos a duas sessões específicas do processo com GUIDs de sessão idênticos, o sistema tratará as sessões como separadas, pois suas IDs de processo são diferentes. Além disso, se uma sessão entre processos usar a mesma GUID de sessão como uma ou mais sessões específicas do processo, o sistema tratará a sessão entre processos como distinta das sessões específicas do processo, mesmo que compartilhem a mesma GUID de sessão.

por exemplo, no Windows Vista, as APIs de nível superior, como as funções Windows multimídia **waveOutXxx** e o DirectSound normalmente atribuem os fluxos de áudio que eles criam para as sessões padrão, específicas do processo, identificadas pelo valor guid da sessão guid \_ NULL. Para clientes dessas APIs, a sessão padrão para cada processo de cliente é separada das sessões padrão para outros processos de cliente, mesmo que as sessões tenham GUIDs de sessão idênticas. Além disso, se um ou mais aplicativos atribuirem fluxos à sessão entre processos que é identificada pelo valor GUID de sessão GUID \_ NULL, o sistema tratará essa sessão entre processos como separada das sessões padrão, específicas do processo que compartilham a mesma GUID de sessão. Da mesma forma, o programa SNDVOL exibe um controle de volume separado para cada sessão padrão, específica de processo do cliente, e ele exibe um controle de volume adicional para a sessão entre processos que é identificada pelo valor GUID de sessão GUID \_ NULL, caso essa sessão exista.

Cada sessão é associada a apenas um dispositivo de ponto de extremidade de áudio. Se duas sessões tiverem GUIDs de sessão e IDs de processo idênticos, mas estiverem associadas a dispositivos diferentes, o sistema tratará as duas sessões como separadas. Uma sessão nunca pode conter fluxos de captura e de renderização porque um fluxo de captura pode ser associado somente a um dispositivo de captura e um fluxo de renderização só pode ser associado a um dispositivo de renderização.

Conforme mencionado anteriormente, as configurações de volume e mudo para uma sessão são persistentes entre as reinicializações do sistema. Duas ou mais instâncias de um aplicativo podem criar sessões específicas do processo com GUIDs de sessão idênticos. Por meio do programa SNDVOL, o usuário pode selecionar configurações diferentes de volume e mudo para cada uma dessas sessões. Depois que essas sessões forem encerradas, o sistema manterá as configurações de controle de apenas uma dessas sessões — a última sessão a ser encerrada. Posteriormente, se uma nova instância do aplicativo criar uma sessão específica do processo com o mesmo GUID de sessão anterior, essa sessão herdará as configurações de volume e de mudo salvas anteriormente.

Um aplicativo não deve tentar adicionar um fluxo ou controlar o nível de volume de uma sessão que pertence a outro aplicativo não relacionado. Além disso, um aplicativo não deve tentar controlar o nível de volume da sessão gerenciada pelo sistema para sons de notificação. No entanto, um aplicativo pode reproduzir um som por meio da sessão do sistema para sons de notificação chamando a função **PlaySound** . Para obter mais informações, consulte [sons de notificação para aplicativos de áudio herdados](notification-sounds-for-legacy-audio-applications.md).

Um aplicativo pode se registrar para receber notificações quando o estado de uma sessão é alterado. Para obter mais informações, consulte [eventos de sessão de áudio](audio-session-events.md).

Em casos raros, um aplicativo que cria uma sessão específica de processo pode precisar consolidar o controle das sessões específicas do processo para duas ou mais instâncias de aplicativo em um único controle de volume no SNDVOL. Para obter mais informações, consulte [agrupando parâmetros](grouping-parameters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 



