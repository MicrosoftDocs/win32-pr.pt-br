---
description: Quando uma chamada está ativa no LINEBEARERMODE \_ PassThrough, o provedor de serviços fornece acesso direto ao hardware anexado para controle pelo aplicativo.
ms.assetid: 75e31241-c782-4d50-9590-cf68c0505add
title: Modo de passagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 985e1caf666fcb3278bacf5c5cfe9d8a4e847dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779896"
---
# <a name="passthrough-mode"></a>Modo de passagem

Quando uma chamada está ativa no **LINEBEARERMODE \_ PassThrough**, o provedor de serviços fornece acesso direto ao hardware anexado para controle pelo aplicativo. Os aplicativos podem usar esse modo para controle direto temporário sobre modems assíncronos, acessados por meio das [funções de comunicação](/windows/desktop/DevIO/communications-functions), com a finalidade de configurar ou usar recursos especiais que de outra forma não têm suporte do provedor de serviços, como o fax (classe 1, 2 e assim por diante). Este modo de portador é compatível com o provedor de serviços Unimodem (Universal driver).

Provedores de serviço que dão suporte a **\_ passagem LINEBEARERMODE** indicam isso no membro **dwBearerModes** da estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) . Quando **a \_ passagem LINEBEARERMODE** é indicada, o provedor de serviços Unimodem também incluirá na área **DevSpecific** da estrutura **LINEDEVCAPS** a chave do Registro usada para acessar dados sobre o modem associado ao dispositivo de linha, no seguinte formato:

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

Essa chave do registro pode então ser aberta usando a função [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) .

O modo PassThrough é invocado com mais frequência usando a função [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , definindo o bit de **\_ passagem LINEBEARERMODE** no membro **dwBearerMode** da estrutura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) apontada pelo parâmetro *lpCallParams* . Quando isso é feito, o provedor de serviços abre a porta serial para o modem e coloca imediatamente a chamada em **LINECALLSTATE \_ conectado**. O aplicativo pode usar a função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) com a classe de dispositivo "comm/datamodea" para obter um identificador de arquivo aberto para ler e gravar na porta de comunicação.

O modo PassThrough também pode ser invocado em resposta a uma chamada de entrada. Em geral, os aplicativos invocarão o modo de passagem enquanto a chamada estiver na **\_ oferta de LINECALLSTATE**, antes que a chamada tenha sido respondida. Em vez de chamar [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer), o aplicativo chama [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams), passando o **LINEBEARERMODE \_ PassThrough** como o parâmetro *dwBearerMode* . Quando isso é feito, assim como com o [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), a chamada é colocada imediatamente no **LINECALLSTATE \_ conectado** pelo provedor de serviços, e o aplicativo pode obter um identificador para a porta aberta usando [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid). A função **lineSetCallParams** pode ser chamada quando a chamada está na **\_ oferta LINECALLSTATE**, **LINECALLSTATE \_ accepted** ou **LINECALLSTATE \_ conectado**.

O modo PassThrough normalmente é encerrado chamando [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) no identificador de chamada obtido de [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) ou a [**mensagem \_ callstate**](line-callstate.md) da primeira linha, se a chamada fosse uma chamada recebida. O provedor de serviços fechará a porta e restaurará o modem para seu estado padrão. O aplicativo deve chamar [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) no identificador recebido de [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).

O modo PassThrough também pode ser encerrado chamando [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) com o parâmetro *DwBearerMode* definido como **LINEBEARERMODE \_ Voice**. O tipo de mídia (modo) definido por [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode) é presumido estar em vigor. Se o **LINEMEDIAMODE \_ datamoder** estiver ativo, o provedor de serviços assumirá a chamada como se fosse uma chamada de modem de dados já em andamento; se [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) for posteriormente chamado, o provedor de serviços emitirá os comandos de modem ou as alterações de estado de interface apropriados para descartar uma chamada de dados.

> [!Note]  
> Se o modo de passagem for encerrado enquanto a chamada estiver em andamento, o provedor de serviços TAPI (TSP) da linha poderá restaurar as configurações do modem para seu estado padrão. Unimodem é um exemplo de um TSP que sempre restaura as configurações do modem ao terminar o modo de passagem. Por esse motivo, o modo PassThrough não pode ser usado como um método para configurar o dispositivo. O modo de passagem só deve ser usado para atividades distintas que podem ser consideradas concluídas quando a passagem é encerrada. Exemplos de atividades que podem usar o modo de passagem incluem enviar um fax ou reproduzir dados de som/áudio por meio de um protocolo de modem proprietário.

 

 

 
