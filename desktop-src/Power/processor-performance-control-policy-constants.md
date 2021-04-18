---
description: As constantes da política de controle de desempenho do processador indicam o algoritmo de controle de desempenho do processador aplicado a um esquema de energia.
ms.assetid: 928ba485-f767-47df-8b57-7630c68068a7
title: Constantes da política de controle de desempenho do processador (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597750f37d9efda80d4bb2bfff7bc121982e7d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505879"
---
# <a name="processor-performance-control-policy-constants"></a>Constantes da política de controle de desempenho do processador

As constantes da política de controle de desempenho do processador indicam o algoritmo de controle de desempenho do processador aplicado a um esquema de energia.



| Constante/valor                                                                                                                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PO_THROTTLE_ADAPTIVE"></span><span id="po_throttle_adaptive"></span><dl> <dt>**Po \_ LIMITAÇÃO \_ adaptável**</dt> <dt>3</dt> </dl> | Tenta fazer a correspondência entre o desempenho do processador e a demanda atual. Essa política usará Estados de alta e baixa voltagem e frequência. Essa política reduzirá o desempenho do processador para a menor voltagem disponível sempre que não houver demanda suficiente para justificar uma tensão mais alta. Essa política irá envolver a limitação do relógio do processador se o estado C3 não estiver sendo utilizado e em resposta a eventos térmicos.<br/> |
| <span id="PO_THROTTLE_CONSTANT"></span><span id="po_throttle_constant"></span><dl> <dt>**Po \_ \_Constante de limitação**</dt> <dt>1</dt> </dl> | Não permite que o processador use nenhum estado de desempenho de alta voltagem. Essa política não envolverá a limitação do relógio do processador, exceto em resposta a eventos térmicos.<br/>                                                                                                                                                                                                                                                                 |
| <span id="PO_THROTTLE_DEGRADE"></span><span id="po_throttle_degrade"></span><dl> <dt>**Po \_ \_Degradação do limite**</dt> <dt>2</dt> </dl>    | Não permite que o processador use nenhum estado de desempenho de alta voltagem. Essa política irá envolver a limitação do relógio do processador quando a bateria estiver abaixo de um determinado limite, se o estado C3 não estiver sendo utilizado ou em resposta a eventos térmicos.<br/>                                                                                                                                                                                    |
| <span id="PO_THROTTLE_NONE"></span><span id="po_throttle_none"></span><dl> <dt>**Po \_ RESTRIÇÃO \_ None**</dt> <dt>0</dt> </dl>             | Nenhum controle de desempenho do processador é aplicado. Essa política sempre executa o processador em seu nível de desempenho mais alto possível. Essa política não envolverá a limitação do relógio do processador, exceto em resposta a eventos térmicos.<br/>                                                                                                                                                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>WinNT. h (incluir Windows. h)</dt> </dl> |



 

 




