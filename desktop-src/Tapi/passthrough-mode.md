---
description: Quando uma chamada está ativa em LINEBEARERMODE PASSTHROUGH, o provedor de serviços fornece acesso direto ao \_ hardware anexado para controle pelo aplicativo.
ms.assetid: 75e31241-c782-4d50-9590-cf68c0505add
title: Modo de passagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69480fb05b0a86c783b983dcf43f5e241dff865ea6bea16ad4a3744ad06a1fb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959716"
---
# <a name="passthrough-mode"></a>Modo de passagem

Quando uma chamada está ativa em **LINEBEARERMODE \_ PASSTHROUGH**, o provedor de serviços fornece acesso direto ao hardware anexado para controle pelo aplicativo. Os aplicativos podem usar esse modo para controle direto temporário sobre modems assíncronos, [acessados](/windows/desktop/DevIO/communications-functions)por meio das funções de comunicação , com a finalidade de configurar ou usar recursos especiais sem suporte do provedor de serviços, como facsimile (Classe 1, 2 e assim por diante). Esse modo de portador é compatível com o provedor de serviços UNIMODEM (Universal Modem Driver).

Provedores de serviços que suportam **LINEBEARERMODE \_ PASSTHROUGH** indicam isso no membro **dwBearerModes** da [**estrutura LINEDEVCAPS.**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) Quando **LINEBEARERMODE \_ PASSTHROUGH** for indicado, o provedor de serviços Unimodem também incluirá na área **DevSpecific** da estrutura **LINEDEVCAPS** a chave do Registro usada para acessar dados sobre o modem associado ao dispositivo de linha, no seguinte formato:

``` syntax
struct {
    DWORD dwContents;   // Set to 1 (indicates containing key).
    DWORD dwKeyOffset;  // Offset to key from start of this
                        // structure (not from start of
                        // LINEDEVCAPS structure).
                        // 8 in this case. 
    BYTE rgby[...];     // Place that contains null-terminated
                        // registry key. 
}
```

Por exemplo:

``` syntax
    00000001 00000008 74737953 435c6d65  ........System\C
    65727275 6f43746e 6f72746e 7465536c  urrentControlSet
    7265535c 65636976 6c435c73 5c737361  urrentControlSet
    65646f4d 30305c6d xx003030 xxxxxxxx  Modem\0000.
```

Essa chave do Registro pode ser aberta usando a [**função RegOpenKey.**](/windows/desktop/api/winreg/nf-winreg-regopenkeya)

O modo de passagem é invocado com mais frequência usando a função [**lineMakeCall,**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) definindo o bit **LINEBEARERMODE \_ PASSTHROUGH** no membro **dwBearerMode** da estrutura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) apontada pelo parâmetro *lpCallParams.* Quando isso for feito, o provedor de serviços abrirá a porta serial para o modem e colocará imediatamente a chamada **em LINECALLSTATE \_ CONNECTED.** Em seguida, o aplicativo pode usar a função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) com a classe de dispositivo "comm/datamodem" para obter um alça de arquivo aberto para ler e gravar na porta de comunicação.

O modo de passagem também pode ser invocado em resposta a uma chamada de entrada. Em geral, os aplicativos invocarão o modo de passagem enquanto a chamada estiver **em LINECALLSTATE \_ OFFERING**, antes que a chamada seja respondida. Em vez de chamar [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer), o aplicativo chama [**lineSetCallParams,**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams)passando **LINEBEARERMODE \_ PASSTHROUGH** como o *parâmetro dwBearerMode.* Quando isso é feito, assim como com [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), a chamada é colocada imediatamente em **LINECALLSTATE \_ CONNECTED** pelo provedor de serviços, e o aplicativo pode obter um handle para a porta aberta usando [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid). A **função lineSetCallParams** pode ser chamada quando a chamada está **em LINECALLSTATE \_ OFFERING**, **LINECALLSTATE \_ ACCEPTED** ou **LINECALLSTATE \_ CONNECTED**.

O modo de passagem normalmente é encerrado chamando [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) no alça de chamada obtido de [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) ou da primeira mensagem [**LINE \_ CALLSTATE,**](line-callstate.md) se a chamada foi uma chamada de entrada. O provedor de serviços fechará a porta e restaurará o modem para seu estado padrão. O aplicativo deve chamar [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) no handle recebido de [**lineGetID.**](/windows/desktop/api/Tapi/nf-tapi-linegetid)

O modo de passagem também pode ser encerrado chamando [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) com o parâmetro *dwBearerMode* definido como **LINEBEARERMODE \_ VOICE.** Presume-se que o tipo de mídia (modo) definido por [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode) está em vigor. Se **LINEMEDIAMODE \_ DATAMODEM** estiver ativo, o provedor de serviços assumirá a chamada como se fosse uma chamada de modem de dados já em andamento; se [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) for chamado posteriormente, o provedor de serviços emitirá os comandos de modem apropriados ou alterações de estado da interface para soltar uma chamada de dados.

> [!Note]  
> Se o modo de passagem for encerrado enquanto a chamada estiver em andamento, o provedor de serviços TAPI (TSP) para a linha poderá restaurar as configurações do modem para seu estado padrão. Unimodem é um exemplo de um TSP que sempre restaura as configurações do modem ao encerrar o modo de passagem. Por esse motivo, o modo de passagem não pode ser usado como um método para configurar o dispositivo. O modo de passagem só deve ser usado para atividades distintas que podem ser consideradas concluídas quando a Passagem é encerrada. Exemplos de atividades que podem usar o modo de passagem incluem enviar um fax ou transmitir dados de onda/áudio por meio de um protocolo de modem proprietário.

 

 

 
