---
description: Uma enum usada para enviar respostas do mecanismo de captura para Diagnóstico de Gráficos.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: EnumeraçãoPipeResponse
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
ms.openlocfilehash: b28971a4a4011422fae5f37c11b4d8fc665cce7c0989842ab81dda027777c253
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119260"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>EnumeraçãoPipeResponse

Uma enum usada para enviar respostas do mecanismo de captura para Diagnóstico de Gráficos.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NOVOS \_ DADOS \_ DISPONÍVEIS**  
Uma resposta que indica que novos dados foram gravados no log de gráficos e estão prontos para serem lidos.

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**DADOS DE \_ EXPERIMENTO**  
Uma resposta que indica informações de configuração sobre a sessão de captura.

<span id="ERRORCODE"></span><span id="errorcode"></span>**Errorcode**  
Uma resposta que indica que o mecanismo de captura encontrou um erro.

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**  
Uma resposta que indica que o mecanismo de captura começou a capturar informações gráficas. Isso não indica que os dados estão disponíveis para serem examinados ainda.

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**DADOS \_ PARCIAIS**  
Uma resposta que indica que os dados parciais foram gravados no log de gráficos.

<span id="READY"></span><span id="ready"></span>**Pronto**  
Uma resposta que indica que o mecanismo de captura está pronto para começar a capturar informações gráficas.

<span id="DONE"></span><span id="done"></span>**Feito**  
Interna

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**  
Uma resposta que indica que uma captura de quadro foi iniciada.

<span id="STATUS"></span><span id="status"></span>**Status**  
Uma resposta que indica informações de status sobre o aplicativo que está sendo capturado; por exemplo, taxa de quadros.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



