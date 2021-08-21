---
description: A classe de dispositivo comm/DataModel consiste em dispositivos datamoden.
ms.assetid: 6bc314c6-30ec-4318-856a-3ab2fa6aadfb
title: comm/datamodeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6bfa18aaa174fd6b3c6bef6a79160845341e15374b6a4dcc72da1795a4bd67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118868084"
---
# <a name="commdatamodem"></a>comm/datamodeto

A classe de dispositivo comm/DataModel consiste em dispositivos datamoden. Você acessa esses dispositivos usando as funções de [arquivo](/windows/desktop/FileIO/file-management-functions) e [comunicação](/windows/desktop/DevIO/communications-functions). Os dispositivos nessa classe estão associados a dispositivos de linha que dão suporte ao \_ tipo de mídia LINEMEDIAMODE DATAmodem, que é especificado no membro **dwMediaModes** da estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o dispositivo de linha.

A função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo **DWSTRINGFORMAT** como o \_ valor binário StringFormat e acrescentando esses membros adicionais:

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

O membro **hComm** é o identificador da porta de comunicações aberta. Esse membro será **nulo** se a porta ainda não estiver aberta ou se o parâmetro *dwSelect* de [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) não for o \_ valor de chamada LINECALLSELECT. Se uma chamada estiver ativa, o provedor de serviços normalmente abrirá a porta em si para obter o controle direto do hardware de comunicações, mas só será necessário retornar um identificador válido se a linha estiver conectada. O provedor de serviços abre a porta usando o \_ valor de sinalizador de arquivo \_ sobreposto e, em seguida, configura a porta usando as configurações especificadas pela função [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) . Você pode definir opções de configuração adicionais para o dispositivo usando as funções de comunicação com o identificador retornado.

O membro **szDeviceName** é uma cadeia de caracteres terminada em **nulo** que especifica o nome da porta de comunicação associada à linha, ao endereço ou à chamada.

Se **hComm** for um identificador válido, você poderá usá-lo em chamadas subsequentes para funções de arquivo, como [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), para enviar e receber dados na chamada. Quando terminar de usar a porta de comunicações e, preferencialmente, antes de usar a função [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) para desalocar a chamada, você deverá fechar a porta usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

Ao usar as funções [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) , alguns provedores de serviços exigem que os dados de configuração para essa classe de dispositivo tenham o seguinte formato:

``` syntax
typedef struct  tagDEVCFG  {
  DEVCFGHDR   dfgHdr;
  COMMCONFIG  commconfig;
} DEVCFG, *PDEVCFG, FAR* LPDEVCFG;

// Device setting information
typedef struct  tagDEVCFGDR  {
  DWORD       dwSize;
  DWORD       dwVersion;
  WORD        fwOptions;
  WORD        wWaitBong;
} DEVCFGHDR;
```

Veja a seguir as informações de configuração do dispositivo para uso com as funções [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Soma do tamanho da estrutura **DEVCFGHDR** e do tamanho real da estrutura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) .

</dd> <dt>

<span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**DW**
</dt> <dd>

Número de versão da estrutura Unimodem **DevConfig** . Esse membro pode ser a \_ versão MDMCFG (0x00010003).

</dd> <dt>

<span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**
</dt> <dd>

Sinalizadores de opção que aparecem na página de opção Unimodem. Esse membro pode ser uma combinação desses valores:

<dl> <dt>

<span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>TERMINAL \_ anterior (1)
</dt> <dd>

Exibe a tela anterior ao terminal.

</dd> <dt>

<span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>\_Postagem do terminal (2)
</dt> <dd>

Exibe a tela pós-terminal.

</dd> <dt>

<span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>\_Discagem manual (4)
</dt> <dd>

Disca o telefone manualmente, se for capaz de fazer isso.

</dd> <dt>

<span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>\_Luzes de lançamento (8)
</dt> <dd>

Exibe o ícone de modem na área de status da barra de tarefas.

Somente o valor das luzes de inicialização \_ é definido por padrão

</dd> </dl> </dd> <dt>

<span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**
</dt> <dd>

Número de segundos (em uma granularidade de dois segundos) para substituir a espera pelo tom de crédito ($).

</dd> <dt>

<span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**
</dt> <dd>

Estrutura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) que pode ser usada com as funções de configuração de modem e comunicações.

</dd> </dl>

 

 
