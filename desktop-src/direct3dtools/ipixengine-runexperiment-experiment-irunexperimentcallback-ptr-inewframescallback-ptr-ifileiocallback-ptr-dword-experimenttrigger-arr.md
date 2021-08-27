---
description: Executa um experimento.
MS-HAID: vspixengine.IPixEngine\_RunExperiment\_Experiment\_IRunExperimentCallback\_ptr\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_DWORD\_ExperimentTrigger\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IPixEngine::RunExperiment
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A2EEC278-C074-44B3-94DC-E2D9DC770576
api_name:
- IPixEngine.RunExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 49ff62c3dfc379e5cc2b0741d70644c88509240b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621892"
---
# <a name="span-idvspixengineipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arrspanipixenginerunexperiment-method"></a><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>Método IPixEngine::RunExperiment

Executa um experimento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RunExperiment(
   Experiment               experiment,
   IRunExperimentCallback * pRequestCallback,
   INewFramesCallback*      callbacks,
   IFileIOCallback*         pFileIOCallback,
   DWORD                    triggersCount,
   ExperimentTrigger []     count4_triggersBuffer
);
```

## <a name="parameters"></a>Parâmetros

*Experiência*   
Descreve o experimento a ser executado.

*pRequestCallback*   
O endereço de uma função usada para notificar o host de que o mecanismo iniciou o experimento.

*Retornos*   
O endereço de uma função usada para notificar o host de que novos quadros foram capturados.

*pFileIOCallback*   
O endereço de uma função usada para notificar o host de erros de E/S de arquivo durante a análise.

*triggersCount*   
O número de gatilhos no experimento.

*count4 \_ triggersBuffer*   
Gatilhos de captura.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPixEngine**](/windows/desktop/direct3dtools/ipixengine)

 

 
