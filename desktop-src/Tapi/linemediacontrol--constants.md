---
description: As \_ constantes de sinalizador de bit LINEMEDIACONTROL descrevem um conjunto de operações genéricas em fluxos de mídia.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: Constantes de LINEMEDIACONTROL_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54c7c83df769eef91afe7c310452c342a855f44391815bbc4429ac07bb6ec92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309966"
---
# <a name="linemediacontrol_-constants"></a>\_Constantes LINEMEDIACONTROL

As constantes de sinalizador de bit **LINEMEDIACONTROL \_** descrevem um conjunto de operações genéricas em fluxos de mídia. As interpretações são determinadas pelo fluxo de mídia. O dispositivo de linha deve ter o recurso de controle de mídia para que qualquer operação de controle de mídia seja efetiva.

<dl> <dt>

<span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ nenhum**
</dt> <dd> <dl> <dt>



Nenhuma alteração é feita no fluxo de mídia.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**Pausar LINEMEDIACONTROL \_**
</dt> <dd> <dl> <dt>



Pause temporariamente o fluxo de mídia.

A velocidade do fluxo de mídia é retornada para normal.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL \_ RATEDOWN**
</dt> <dd> <dl> <dt>



A velocidade do fluxo de mídia é diminuída por uma quantidade definida pelo fluxo.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL \_ RATENORMAL**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL \_ RATEUP**
</dt> <dd> <dl> <dt>



A velocidade do fluxo de mídia é aumentada por uma quantidade definida pelo fluxo.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**redefinição de LINEMEDIACONTROL \_**
</dt> <dd> <dl> <dt>



Redefina o fluxo de mídia. Equivalente a um fim de entrada. Todos os buffers são liberados.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**retomar LINEMEDIACONTROL \_**
</dt> <dd> <dl> <dt>



Retomar um fluxo de mídia em pausa.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL \_ Iniciar**
</dt> <dd> <dl> <dt>



Inicie o fluxo de mídia.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL \_ VOLUMEDOWN**
</dt> <dd> <dl> <dt>



A amplitude do fluxo de mídia é diminuída por uma quantidade definida pelo fluxo.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL \_ VOLUMENORMAL**
</dt> <dd> <dl> <dt>



A amplitude do fluxo de mídia é retornada para normal.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL \_ VOLUMEUP**
</dt> <dd> <dl> <dt>



A amplitude do fluxo de mídia é aumentada por uma quantidade definida pelo fluxo.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo. Os 16 bits de ordem inferior são reservados.

O controle de mídia é fornecido para melhorar o desempenho de ações em fluxos de mídia em resposta a eventos relacionados a telefonia. O aplicativo normalmente deve gerenciar um fluxo de mídia por meio da API específica da mídia. A funcionalidade de controle de mídia fornecida aqui não se destina a substituir as APIs de mídia nativas.

As ações de controle de mídia podem ser associadas à detecção de dígitos, à detecção de tons, à transição para um estado de chamada e à detecção de um tipo de mídia. Consulte os recursos do dispositivo de uma linha para determinar se o controle de mídia está disponível na linha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




