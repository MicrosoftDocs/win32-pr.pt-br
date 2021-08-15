---
description: Uma enum usada para indicar qual versão do protótipo de remoção está sendo usada.
MS-HAID: vspixengine.REMOTINGVERSION
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração REMOTINGVERSION
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 598E9586-05FF-4889-BBAF-44814EEF203A
api_name:
- REMOTINGVERSION
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d7e5c937610b06a58309181a4dad2c95846d287b335c8ab6b2fed9008f338f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985476"
---
# <a name="span-idvspixengineremotingversionspanremotingversion-enumeration"></a><span id="vspixengine.remotingversion"></span>Enumeração REMOTINGVERSION

Uma enum usada para indicar qual versão do protótipo de remoção está sendo usada.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="REMOTING_DEV12"></span><span id="remoting_dev12"></span>**REMOTING \_ DEV12**  
Um valor que indica que o protocolo Visual Studio 2013 de comunicação de comunicação remo do RTM está sendo usado.

<span id="REMOTING_DEV12_UPDATE_1"></span><span id="remoting_dev12_update_1"></span>**REMOTING \_ DEV12 \_ UPDATE \_ 1**  
Um valor que indica que o protocolo de comunicação Visual Studio 2013 atualização 1 está sendo usado.

<span id="REMOTING_DEV12_UPDATE_4"></span><span id="remoting_dev12_update_4"></span>**REMOTING \_ DEV12 \_ UPDATE \_ 4**  
Um valor que indica que o protocolo Visual Studio 2013 Update 4 de comunicação remo está sendo usado.

<span id="REMOTING_DEV14"></span><span id="remoting_dev14"></span>**REMOTING \_ DEV14**  
Um valor que indica que o protocolo de Visual Studio 2015 RTM está sendo usado.

<span id="REMOTING_WIN10"></span><span id="remoting_win10"></span>**COMO FAZER A \_ REMOÇÃO DO WIN10**  
Um valor que indica que o protocolo Windows 10 de comunicação remoting está sendo usado (a partir do Windows 10, o diagnóstico de gráficos é um componente do sistema operacional)

<span id="REMOTING_WIN10_JAN_2015"></span><span id="remoting_win10_jan_2015"></span>**REMOTING \_ WIN10 \_ JAN \_ 2015**  
Um valor que indica que o protocolo de Windows 10 (janeiro de 2015) está sendo usado.

<span id="REMOTING_WIN10_JAN_2015_1"></span><span id="remoting_win10_jan_2015_1"></span>**REMOTING \_ WIN10 \_ JAN \_ 2015 \_ 1**  
Um valor que indica que o protocolo de comunicação Windows 10 (janeiro de 2015, v1) está sendo usado.

<span id="REMOTING_WIN10_JAN_2015_2"></span><span id="remoting_win10_jan_2015_2"></span>**REMOTING \_ WIN10 \_ JAN \_ 2015 \_ 2**  
Um valor que indica que o protocolo de Windows 10 (janeiro de 2015, v2) está sendo usado. Esta versão do protocolo introduziu solicitações para visualizar recursos lado a lado.

<span id="REMOTING_WIN10_JAN_2015_3"></span><span id="remoting_win10_jan_2015_3"></span>**REMOTING \_ WIN10 \_ JAN \_ 2015 \_ 3**  
Um valor que indica que o protocolo de Windows 10 (janeiro de 2015, v3) está sendo usado. Esta versão do protocolo introduziu IPixEngine7, agora preterido, para verificar o suporte à versão da interface.

<span id="REMOTING_IPIXENGINE7_VERSION_CHECKING"></span><span id="remoting_ipixengine7_version_checking"></span>**VERIFICAÇÃO DE \_ VERSÃO DE IPIXENGINE7 \_ DE \_ REMOTING**  
Um valor que indica que o protocolo de comunicação Windows 10 (janeiro de 2015, v1) está sendo usado. Esta versão do protocolo deixa de depender de REMOTINGVERSION para recursos de protocolo de mediação. O GUID da interface agora é alterado quando int não público

<span id="REMOTING_WIN10_FEB_2015_1"></span><span id="remoting_win10_feb_2015_1"></span>**REMOTING \_ WIN10 \_ FEB \_ 2015 \_ 1**  
Um valor que indica que o protocolo de comunicação Windows 10 (janeiro de 2015, v1) está sendo usado. Esta versão do protocolo apresenta propriedades de informações resumidas com IDs exclusivas e fixas.

<span id="REMOTING_WIN10_2015_03_00"></span><span id="remoting_win10_2015_03_00"></span>**REMOTING \_ WIN10 \_ 2015 \_ 03 \_ 00**  
Um valor que indica que o protocolo de comunicação Windows 10 (janeiro de 2015, v1) está sendo usado. Esta versão do protocolo introduziu suporte para a janela de estado DirectX11.

<span id="REMOTING_LATES"></span><span id="remoting_lates"></span>**ATRASOS \_ DE REMOÇÃO**  
Um valor que indica que o protocolo de comunicação remo mais recente está sendo usado.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



