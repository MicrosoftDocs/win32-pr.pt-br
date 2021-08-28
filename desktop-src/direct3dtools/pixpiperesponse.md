---
description: Uma enumeração usada para enviar respostas do mecanismo de captura para Diagnóstico de Gráficos.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração PixPipeResponse
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ad00d7bada935dd27f711499e5975d31709b9940
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631684"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>Enumeração PixPipeResponse

Uma enumeração usada para enviar respostas do mecanismo de captura para Diagnóstico de Gráficos.

## <a name="syntax"></a>Sintaxe


```C++
};
```

## <a name="constants"></a>Constantes

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NOVOS \_ dados \_ disponíveis**  
Uma resposta que indica que novos dados foram gravados no log de gráficos e estão prontos para serem lidos.

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**dados de teste \_**  
Uma resposta que indica informações de configuração sobre a sessão de captura.

<span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**  
Uma resposta que indica que o mecanismo de captura encontrou um erro.

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**  
Uma resposta que indica que o mecanismo de captura iniciou a captura de informações de gráficos. Isso não indica que os dados estão disponíveis para serem examinados ainda.

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**dados PARCIAIs \_**  
Uma resposta que indica que dados parciais foram gravados no log de gráficos.

<span id="READY"></span><span id="ready"></span>**ESTEJA**  
Uma resposta que indica que o mecanismo de captura está pronto para iniciar a captura de informações de gráficos.

<span id="DONE"></span><span id="done"></span>**TRABALHADO**  
Interna

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**  
Uma resposta que indica que uma captura de quadro foi iniciada.

<span id="STATUS"></span><span id="status"></span>**Estado**  
Uma resposta que indica informações de status sobre o aplicativo que está sendo capturado; por exemplo, taxa de quadros.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



