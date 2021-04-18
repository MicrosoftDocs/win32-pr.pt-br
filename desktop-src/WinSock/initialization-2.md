---
description: O ws2 \_32.dll carrega a DLL de interface do provedor de serviços no sistema usando os mecanismos padrão de carregamento da biblioteca dinâmica do Microsoft Windows e inicializa-o chamando WSPStartup.
ms.assetid: 6df28d93-8757-45b3-8f05-86381c3be64e
title: Inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d6ef10db421ef15f2bb94eb67e96fc2cfc5924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772990"
---
# <a name="initialization"></a>Inicialização

O *Ws2 \_32.dll* carrega a DLL de interface do provedor de serviços no sistema usando os mecanismos padrão de carregamento da biblioteca dinâmica do Microsoft Windows e inicializa-o chamando [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Normalmente, isso é disparado por um aplicativo chamando [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) para criar um novo soquete a ser associado a um provedor de serviços cuja dll de interface não esteja atualmente carregada na memória. O caminho para a DLL de interface do provedor de serviços é armazenado *pelo \_32.dllWs2* no momento em que o provedor de serviços está sendo instalado. Confira [funções de instalação e configuração](installation-and-configuration-functions-2.md) para obter mais informações.

Ao longo do tempo, podem existir versões diferentes para as DLLs, os aplicativos e os provedores de serviços do Winsock. Novas versões podem definir novos recursos e novos parâmetros para estruturas de dados e parâmetros de bits, etc. Portanto, os números de versão indicam como interpretar várias estruturas de dados.

Para permitir a combinação ideal e a correspondência de diferentes versões de aplicativos, versões do ws2 \_32.dll si mesma e versões de provedores de serviço por diferentes fornecedores, o SPI fornece um mecanismo de negociação de versão para uso entre o *\_32.dllde ws2* e os provedores de serviços. Essa negociação de versão é tratada pelo [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Basicamente, o *\_32.dllWs2* passa para o provedor de serviços os números de versão mais altos com os quais ele é compatível. O provedor de serviços compara isso com seu próprio intervalo de números de versão com suporte. Se esses intervalos se sobrepõem, o provedor de serviços retorna um valor dentro da parte sobreposta do intervalo como o resultado da negociação. Normalmente, isso deve ser o maior valor possível. Se os intervalos não se sobrepõem, as duas partes são incompatíveis e a função retorna um erro.

[**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) deve ser chamado pelo menos uma vez por cada processo de cliente e pode ser chamado várias vezes por Ws2 \_32.dll ou outras entidades. Um [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) correspondente deve ser chamado para cada chamada **WSPStartup** bem-sucedida. O provedor de serviços deve manter uma contagem de referência em cada processo. Em cada chamada de **WSPStartup** , o chamador pode especificar qualquer número de versão com suporte na DLL do SP.

Um provedor de serviços deve armazenar o ponteiro para a tabela de expedição de chamada do cliente que é recebida como um parâmetro [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) por processo. Se um determinado processo chamar **WSPStartup** várias vezes, o provedor de serviços deverá usar apenas o ponteiro de tabela de expedição fornecido mais recentemente.

Como parte do processo de inicialização do provedor de serviços, o ws2 \_32.dll recupera a tabela de expedição do provedor de serviços por meio do parâmetro *lpProcTable* para obter pontos de entrada para o restante das funções SPI especificadas neste documento.

Usar uma tabela de expedição (ao contrário dos mecanismos de DLL usuais para acessar pontos de entrada) atende a duas finalidades:

-   É mais conveniente para a32.dll Ws2 \_ , já que uma única chamada pode ser feita para descobrir o conjunto inteiro de pontos de entrada.
-   Ele permite que provedores de serviço em camadas formados em cadeias de protocolos operem com mais eficiência.

## <a name="initializing-protocol-chains"></a>Inicializando cadeias de protocolo

No momento em que a estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para uma cadeia de protocolos é instalada, o caminho para o primeiro provedor em camadas na cadeia também é especificado. Quando uma cadeia de protocolos é inicializada, o \_32.dll Ws2 usa esse caminho para carregar a DLL do provedor e, em seguida, invoca [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Como o **WSPStartup** inclui um ponteiro para a estrutura **de \_ informações do WSAPROTOCOL** da cadeia como um de seus parâmetros, os provedores em camadas podem determinar em que tipo de cadeia eles estão sendo inicializados e a identidade da próxima camada inferior na cadeia. Um provedor em camadas, por sua vez, carregaria o próximo provedor de protocolo na cadeia e o inicializaria com uma chamada para **WSPStartup** e assim por diante. Sempre que a próxima camada inferior for outro provedor em camadas, a estrutura **de \_ informações WSAPROTOCOL** da cadeia deverá ser referenciada na chamada **WSPStartup** . Quando a próxima camada inferior é um protocolo base (que significa o fim da cadeia), a estrutura de **\_ informações WSAPROTOCOL** da cadeia não é mais propagada para baixo. Em vez disso, a camada atual deve fazer referência a uma estrutura de **\_ informações de WSAPROTOCOL** que corresponde ao protocolo que o provedor base deve usar. Portanto, o provedor base não tem nenhuma noção de estar envolvido em uma cadeia de protocolos.

A tabela de expedição fornecida por qualquer provedor em camadas específico irá, em muitos casos, duplicar os pontos de entrada de um provedor subjacente. O provedor em camadas só inseriria seus próprios pontos de entrada para funções que precisava estar diretamente envolvido no. No entanto, observe que é imperativo que um provedor em camadas não modifique o conteúdo da tabela de chamada recebida ao chamar [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) na próxima camada inferior em uma cadeia de protocolos. Essas chamadas devem ser feitas diretamente para a DLL do Windows Sockets 2.

 

 
