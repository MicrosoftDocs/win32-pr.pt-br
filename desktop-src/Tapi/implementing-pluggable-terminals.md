---
description: Os requisitos gerais para implementação de terminal conectável estão listados abaixo.
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: Implementando terminais conectáveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 494b2f6bc5ccb214bc7101f570a4db3037fd8cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757968"
---
# <a name="implementing-pluggable-terminals"></a>Implementando terminais conectáveis

Os requisitos gerais para a implementação de terminal conectável são:

-   Um código de streaming subjacente de um terminal conectável deve corresponder aos recursos do MSPs desejado.
-   O terminal deve usar filtros do DirectShow para trabalhar com a maioria dos MSPs (isso é assumido daqui em diante).
-   Os terminais de áudio devem dar suporte a 8 kHz de PCM linear mono de 16 bits para a maioria dos MSPs.
-   O terminal deve habilitar o empacotamento livre de threads implementando [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). O terminal pode fazer isso chamando a API COM [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) e agregando **IMarshal** ao ponteiro retornado. O destruidor do objeto de terminal deve chamar a [**versão IMarshal->**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).
-   O terminal deve implementar ou agregar qualquer outra interface específica do terminal que seja apropriada.
-   A implementação do terminal deve ser thread-safe.
-   A implementação do terminal deve \# incluir Termmgr. h para a definição de [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol). Isso é além das inclusões e bibliotecas usuais que são necessárias para aplicativos TAPI 3 ou TAPI 3 no Windows 2000 SP1.

Notas de implementação de interface e método:

O terminal deve implementar [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) (interface dual – vtable + [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)).

[**ITTerminal:: obter \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

O terminal deve retornar uma representação **BSTR** de um GUID escolhido que identifica o tipo de terminal. Aloque o **BSTR** via [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring). Para converter de GUID para **BSTR**, chame [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid), **SysAllocString** e [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

[**ITTerminal:: obter \_ terminaltype**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

O terminal, em geral, deve retornar TT \_ dinâmico se um aplicativo implementar o terminal. Retornar TT \_ estático também funcionará e o retorno desse valor poderá ser apropriado se o terminal corresponder a um dispositivo de hardware; no entanto, fazer isso pode ser confuso para os usuários, pois um terminal estático não estará presente na enumeração de terminal estática do MSP.

[**ITTerminal:: obter \_ estado**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

Se a implementação do terminal não limitar arbitrariamente o número de fluxos aos quais o terminal pode ser conectado simultaneamente, o terminal sempre deverá retornar TS \_ NOTINUSE.

Caso contrário, a implementação do terminal limita arbitrariamente o número de fluxos aos quais o terminal pode ser conectado por vez. Nesse caso, o terminal deve manter uma contagem de quantos fluxos ele está conectado. O terminal deve incrementar essa contagem interna em uma chamada [**ITTerminalControl:: ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) bem-sucedida e decrementa-la em uma [**ITTerminalControl bem-sucedida::D chamada isconnectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) . No [**\_ estado ITTerminal:: Get**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state), ele deve retornar TS \_ INUSE se essa contagem for igual ao número máximo de fluxos em que o terminal pode ser selecionado por vez; caso contrário, ele deverá retornar TS \_ NOTINUSE. Observe que, se o limite for um, a contagem poderá simplesmente ser um valor booliano ou de estado do TERMINAL \_ .

[**ITTerminal:: obter \_ nome**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

O terminal deve retornar um nome **BSTR** de sua escolha, alocado por meio de [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring). Esse nome deve ser significativo para o usuário e deve ser localizado.

[**ITTerminal:: obter \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

O terminal deve retornar seu tipo de mídia, seja TAPIMEDIATYPE \_ áudio ou TAPIMEDIATYPE \_ vídeo.

[**ITTerminal:: obter \_ direção**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

O terminal retorna o \_ valor de enumeração da direção do terminal que indica a direção do terminal. Se o terminal for bidirecional (por exemplo, uma ponte), ele deverá retornar o TD \_ bidirecional.

O terminal deve implementar [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (somente vtable).

[**ITTerminalControl:: obter \_ AddressHandle**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

Um terminal fornecido pelo aplicativo sempre deve retornar **NULL** como o identificador de endereço. Isso indica para o MSP que esse terminal não foi criado em um objeto de endereço MSP específico.

[**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

Nessa chamada, o terminal adicionará seus filtros ao grafo fornecido e os conectará entre si, se aplicável. Em seguida, o terminal deve retornar os Pins expostos pelo terminal para a direção do fluxo especificada.

Um terminal que não dá suporte à conexão simultânea com vários fluxos definiria uma variável interna para TS \_ INUSE na conclusão bem-sucedida desse método.

O terminal pode usar o parâmetro *dwTerminalDirection* dessa chamada para determinar a direção do fluxo ao qual ele está sendo conectado. Isso é necessário para terminais bidirecionais.

> [!Note]  
> Normalmente (nas classes base MSP e em todos os MSPs conhecidos), o código de fluxo MSP falhará na conexão se o terminal retornar mais de um PIN de uma única chamada [**ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) . Isso é bom, porque um terminal que retorna mais de um PIN durante a conexão requer que o MSP tenha conhecimento especial do terminal para fazer uso dos Pins extras com eficiência.

 

[**ITTerminalControl::CompleteConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

O terminal deve simplesmente retornar S \_ OK. O terminal também pode fazer a inicialização após a conexão, se necessário.

[**ITTerminalControl::D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

O terminal deve fazer tudo o que for necessário para desconectar o terminal do restante do grafo. Normalmente, isso envolve a remoção de todos os filtros dos terminais do grafo e a definição do estado do terminal como TS \_ NOTINUSE.

[**ITTerminalControl::RunRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

O terminal deve apenas retornar E \_ NOTIMPL.

[**ITTerminalControl::StopRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

O terminal deve apenas retornar E \_ NOTIMPL.

 

 
