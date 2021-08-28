---
description: <span id="vspixengine.remotecommandtype"></span>enumeração RemoteCommandType-uma enumeração usada para comunicação entre o mecanismo de captura e um host (como Visual Studio Diagnóstico de Gráficos).
MS-HAID: vspixengine.RemoteCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração RemoteCommandType
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B517F70C-2BFB-42E7-8597-AC5915AB2DE0
api_name:
- RemoteCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 73accd6f73a7c33219c83a3285837d2e1c7c133a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631714"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span id="vspixengine.remotecommandtype"></span>Enumeração RemoteCommandType

uma enumeração usada para se comunicar entre o mecanismo de captura e um host (como Visual Studio Diagnóstico de Gráficos).

## <a name="syntax"></a>Sintaxe


```C++
};
```

## <a name="constants"></a>Constantes

<span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**  
Inicia a comunicação.

<span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**  
Inicia uma sessão de captura Diagnóstico de Gráficos (um experimento).

<span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**  
Inicia uma captura (o mesmo que pressionar a tela de impressão). Enviado por um host durante a captura de um quadro.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



