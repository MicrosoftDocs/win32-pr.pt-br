---
description: Os requisitos gerais para implementação de terminal plug-able estão listados abaixo.
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: Implementando terminais plug-able
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a75dd7b085377c8474c9a89d74a297c3ca66c6740c01c7428e7b6f250e16c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762898"
---
# <a name="implementing-pluggable-terminals"></a>Implementando terminais plug-able

Os requisitos gerais para implementação de terminal plug-able são:

-   O código de streaming subjacente de um terminal que pode ser conectado deve corresponder aos recursos dos MSPs desejados.
-   O terminal deve usar DirectShow filtros para trabalhar com a maioria dos MSPs (isso é assumido daqui em diante).
-   Os terminais de áudio devem dar suporte a PCM mono linear de 8 kHz de 16 bits para a maioria dos MSPs.
-   O terminal deve habilitar o marshalling threaded gratuito implementando [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). O terminal pode fazer isso chamando a API COM [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) e agregando **IMarshal** ao ponteiro retornado. O destruidor do objeto terminal deve chamar [**IMarshal->Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).
-   O terminal deve implementar ou agregar quaisquer interfaces adicionais específicas do terminal apropriadas.
-   A implementação do terminal deve ser thread-safe.
-   A implementação do terminal \# deve incluir Termmgr.h para a definição [**de ITTerminalControl.**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) Isso é além das bibliotecas comuns e que são necessárias para aplicativos TAPI 3 ou TAPI 3 no Windows 2000 SP1.

Notas de implementação de interface e método:

O terminal deve implementar [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) (interface dupla – vtable + [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)).

[**ITTerminal::get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

O terminal deve retornar uma **representação BSTR** de um GUID que você escolheu que identifica o tipo de terminal. Aloque **o BSTR** via [**SysAllocString.**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) Para converter de GUID para **BSTR,** chame [**StringFromCLSID,**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) **SysAllocString** e [**CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

[**ITTerminal::get \_ TerminalType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

O terminal geralmente deve retornar TT \_ DYNAMIC se um aplicativo implementar o terminal. Retornar TT STATIC também funcionará e retornar esse valor poderá ser apropriado se o terminal corresponder a um dispositivo de hardware; no entanto, fazer isso pode ser confuso para os usuários porque um terminal estático não estará presente na enumeração de terminal estático do \_ MSP.

[**ITTerminal::get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

Se a implementação do terminal não limitar arbitrariamente o número de fluxos aos que o terminal pode ser conectado simultaneamente, o terminal sempre deverá retornar TS \_ NOTINUSE.

Caso contrário, a implementação do terminal limita arbitrariamente o número de fluxos aos que o terminal pode ser conectado por vez. Nesse caso, o terminal deve manter uma contagem de quantos fluxos ele está conectado. O terminal deve incrementar essa contagem interna em uma chamada [**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) bem-sucedida e decrementá-la em uma chamada [**ITTerminalControl::D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) bem-sucedida. Em [**ITTerminal::get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state), ele deverá retornar TS INUSE se essa contagem for igual ao número máximo de fluxos em que o terminal pode ser selecionado por vez; caso contrário, ele deverá retornar \_ TS \_ NOTINUSE. Observe que, se o limite for um, a contagem poderá ser simplesmente um valor booliana ou TERMINAL \_ STATE.

[**ITTerminal::get \_ Name**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

O terminal deve retornar um **nome BSTR** de sua escolha, alocado por [**meio de SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring). Esse nome deve ser significativo para o usuário e deve ser localizado.

[**ITTerminal::get \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

O terminal deve retornar seu tipo de mídia, TAPIMEDIATYPE \_ AUDIO ou TAPIMEDIATYPE \_ VIDEO.

[**ITTerminal::get \_ Direction**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

O terminal retorna o valor de enum TERMINAL \_ DIRECTION que indica a direção do terminal. Se o terminal for bidirecional (por exemplo, uma ponte), ele deverá retornar TD \_ BIDIRECTIONAL.

O terminal deve implementar [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (somente vtable).

[**ITTerminalControl::get \_ AddressHandle**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

Um terminal fornecido pelo aplicativo sempre deve retornar **NULL** como o alça de endereço. Isso indica ao MSP que esse terminal não foi criado em um objeto de endereço MSP específico.

[**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

Nessa chamada, o terminal adicionará seus filtros ao grafo determinado e os conectará uns aos outros, se aplicável. Em seguida, o terminal deve retornar os pinos expostos pelo terminal para a direção do fluxo especificada.

Um terminal que não dá suporte à conexão simultânea a vários fluxos definiria uma variável interna como TS INUSE após a conclusão \_ bem-sucedida desse método.

O terminal pode usar o *parâmetro dwTerminalDirection* dessa chamada para determinar a direção do fluxo ao qual ele está sendo conectado. Isso é necessário para terminais bidirecionais.

> [!Note]  
> Normalmente (nas classes base do MSP e em todos os MSPs conhecidos), o código de fluxo MSP falhará na conexão se o terminal retornar mais de um pino de uma única [**chamada ConnectTerminal.**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) Isso é bom, porque um terminal que retorna mais de um pino durante a conexão exige que o MSP tenha conhecimento especial do terminal para usar os pinos extras com eficiência.

 

[**ITTerminalControl::CompleteConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

O terminal deve retornar apenas S \_ OK. O terminal também pode fazer a inicialização pós-conexão, se necessário.

[**ITTerminalControl::D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

O terminal deve fazer o que for necessário para desconectar o terminal do restante do grafo. Normalmente, isso envolve remover todos os filtros dos terminais do grafo e definir o estado do terminal como TS \_ NOTINUSE.

[**ITTerminalControl::RunRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

O terminal deve retornar apenas E \_ NOTIMPL.

[**ITTerminalControl::StopRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

O terminal deve retornar apenas E \_ NOTIMPL.

 

 
