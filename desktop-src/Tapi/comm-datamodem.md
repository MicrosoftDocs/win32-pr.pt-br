---
description: A classe de dispositivo comm/DataModel consiste em dispositivos datamoden.
ms.assetid: 6bc314c6-30ec-4318-856a-3ab2fa6aadfb
title: comm/datamodeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89210bcf14931e3905f71cdbb8678f5519cc4c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767768"
---
# <a name="commdatamodem"></a><span data-ttu-id="9e533-103">comm/datamodeto</span><span class="sxs-lookup"><span data-stu-id="9e533-103">comm/datamodem</span></span>

<span data-ttu-id="9e533-104">A classe de dispositivo comm/DataModel consiste em dispositivos datamoden.</span><span class="sxs-lookup"><span data-stu-id="9e533-104">The comm/datamodem device class consists of datamodem devices.</span></span> <span data-ttu-id="9e533-105">Você acessa esses dispositivos usando as funções de [arquivo](/windows/desktop/FileIO/file-management-functions) e [comunicação](/windows/desktop/DevIO/communications-functions).</span><span class="sxs-lookup"><span data-stu-id="9e533-105">You access these devices by using the [file](/windows/desktop/FileIO/file-management-functions) and [communications functions](/windows/desktop/DevIO/communications-functions).</span></span> <span data-ttu-id="9e533-106">Os dispositivos nessa classe estão associados a dispositivos de linha que dão suporte ao \_ tipo de mídia LINEMEDIAMODE DATAmodem, que é especificado no membro **dwMediaModes** da estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="9e533-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_DATAMODEM media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="9e533-107">A função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo **DWSTRINGFORMAT** como o \_ valor binário StringFormat e acrescentando esses membros adicionais:</span><span class="sxs-lookup"><span data-stu-id="9e533-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to the STRINGFORMAT\_BINARY value and appending these additional members:</span></span>

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

<span data-ttu-id="9e533-108">O membro **hComm** é o identificador da porta de comunicações aberta.</span><span class="sxs-lookup"><span data-stu-id="9e533-108">The **hComm** member is the handle of the open communications port.</span></span> <span data-ttu-id="9e533-109">Esse membro será **nulo** se a porta ainda não estiver aberta ou se o parâmetro *dwSelect* de [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) não for o \_ valor de chamada LINECALLSELECT.</span><span class="sxs-lookup"><span data-stu-id="9e533-109">This member is **NULL** if the port is not yet open or if the *dwSelect* parameter of [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) is not the LINECALLSELECT\_CALL value.</span></span> <span data-ttu-id="9e533-110">Se uma chamada estiver ativa, o provedor de serviços normalmente abrirá a porta em si para obter o controle direto do hardware de comunicações, mas só será necessário retornar um identificador válido se a linha estiver conectada.</span><span class="sxs-lookup"><span data-stu-id="9e533-110">If a call is active, the service provider typically opens the port itself to get direct control of the communications hardware, but is only required to return a valid handle if the line is connected.</span></span> <span data-ttu-id="9e533-111">O provedor de serviços abre a porta usando o \_ valor de sinalizador de arquivo \_ sobreposto e, em seguida, configura a porta usando as configurações especificadas pela função [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .</span><span class="sxs-lookup"><span data-stu-id="9e533-111">The service provider opens the port using the FILE\_FLAG\_OVERLAPPED value and then configures the port using the settings specified by the [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) function.</span></span> <span data-ttu-id="9e533-112">Você pode definir opções de configuração adicionais para o dispositivo usando as funções de comunicação com o identificador retornado.</span><span class="sxs-lookup"><span data-stu-id="9e533-112">You can set additional configuration options for the device by using communications functions with the returned handle.</span></span>

<span data-ttu-id="9e533-113">O membro **szDeviceName** é uma cadeia de caracteres terminada em **nulo** que especifica o nome da porta de comunicação associada à linha, ao endereço ou à chamada.</span><span class="sxs-lookup"><span data-stu-id="9e533-113">The **szDeviceName** member is a **null**-terminated string that specifies the name of the communications port associated with the line, address, or call.</span></span>

<span data-ttu-id="9e533-114">Se **hComm** for um identificador válido, você poderá usá-lo em chamadas subsequentes para funções de arquivo, como [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), para enviar e receber dados na chamada.</span><span class="sxs-lookup"><span data-stu-id="9e533-114">If **hComm** is a valid handle, you can use it in subsequent calls to file functions, such as [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), to send and receive data on the call.</span></span> <span data-ttu-id="9e533-115">Quando terminar de usar a porta de comunicações e, preferencialmente, antes de usar a função [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) para desalocar a chamada, você deverá fechar a porta usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="9e533-115">When you are finished using the communications port and preferably before you use the [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) function to deallocate the call, you must close the port by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="9e533-116">Ao usar as funções [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) , alguns provedores de serviços exigem que os dados de configuração para essa classe de dispositivo tenham o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="9e533-116">When using the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions, some service providers require that the configuration data for this device class have the following format:</span></span>

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

<span data-ttu-id="9e533-117">Veja a seguir as informações de configuração do dispositivo para uso com as funções [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .</span><span class="sxs-lookup"><span data-stu-id="9e533-117">The following is device configuration information for use with the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions.</span></span>

<dl> <dt>

<span data-ttu-id="9e533-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="9e533-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="9e533-119">Soma do tamanho da estrutura **DEVCFGHDR** e do tamanho real da estrutura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) .</span><span class="sxs-lookup"><span data-stu-id="9e533-119">Sum of the size of the **DEVCFGHDR** structure and the actual size of the [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9e533-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**DW**</span><span class="sxs-lookup"><span data-stu-id="9e533-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9e533-121">Número de versão da estrutura Unimodem **DevConfig** .</span><span class="sxs-lookup"><span data-stu-id="9e533-121">Version number of the Unimodem **DevConfig** structure.</span></span> <span data-ttu-id="9e533-122">Esse membro pode ser a \_ versão MDMCFG (0x00010003).</span><span class="sxs-lookup"><span data-stu-id="9e533-122">This member can be MDMCFG\_VERSION (0x00010003).</span></span>

</dd> <dt>

<span data-ttu-id="9e533-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span><span class="sxs-lookup"><span data-stu-id="9e533-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span></span>
</dt> <dd>

<span data-ttu-id="9e533-124">Sinalizadores de opção que aparecem na página de opção Unimodem.</span><span class="sxs-lookup"><span data-stu-id="9e533-124">Option flags that appear on the Unimodem Option page.</span></span> <span data-ttu-id="9e533-125">Esse membro pode ser uma combinação desses valores:</span><span class="sxs-lookup"><span data-stu-id="9e533-125">This member can be a combination of these values:</span></span>

<dl> <dt>

<span data-ttu-id="9e533-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>TERMINAL \_ anterior (1)</span><span class="sxs-lookup"><span data-stu-id="9e533-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>TERMINAL\_PRE (1)</span></span>
</dt> <dd>

<span data-ttu-id="9e533-127">Exibe a tela anterior ao terminal.</span><span class="sxs-lookup"><span data-stu-id="9e533-127">Displays the pre-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="9e533-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>\_Postagem do terminal (2)</span><span class="sxs-lookup"><span data-stu-id="9e533-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>TERMINAL\_POST (2)</span></span>
</dt> <dd>

<span data-ttu-id="9e533-129">Exibe a tela pós-terminal.</span><span class="sxs-lookup"><span data-stu-id="9e533-129">Displays the post-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="9e533-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>\_Discagem manual (4)</span><span class="sxs-lookup"><span data-stu-id="9e533-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>MANUAL\_DIAL (4)</span></span>
</dt> <dd>

<span data-ttu-id="9e533-131">Disca o telefone manualmente, se for capaz de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="9e533-131">Dials the phone manually, if capable of doing so.</span></span>

</dd> <dt>

<span data-ttu-id="9e533-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>\_Luzes de lançamento (8)</span><span class="sxs-lookup"><span data-stu-id="9e533-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>LAUNCH\_LIGHTS (8)</span></span>
</dt> <dd>

<span data-ttu-id="9e533-133">Exibe o ícone de modem na área de status da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="9e533-133">Displays the modem icon in the status area of the taskbar.</span></span>

<span data-ttu-id="9e533-134">Somente o valor das luzes de inicialização \_ é definido por padrão</span><span class="sxs-lookup"><span data-stu-id="9e533-134">Only the LAUNCH\_LIGHTS value is set by default</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9e533-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span><span class="sxs-lookup"><span data-stu-id="9e533-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span></span>
</dt> <dd>

<span data-ttu-id="9e533-136">Número de segundos (em uma granularidade de dois segundos) para substituir a espera pelo tom de crédito ($).</span><span class="sxs-lookup"><span data-stu-id="9e533-136">Number of seconds (in two seconds granularity) to replace the wait for credit tone ($).</span></span>

</dd> <dt>

<span data-ttu-id="9e533-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span><span class="sxs-lookup"><span data-stu-id="9e533-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span></span>
</dt> <dd>

<span data-ttu-id="9e533-138">Estrutura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) que pode ser usada com as funções de configuração de modem e comunicações.</span><span class="sxs-lookup"><span data-stu-id="9e533-138">[**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure that can be used with the communications and modem configuration functions.</span></span>

</dd> </dl>

 

 
