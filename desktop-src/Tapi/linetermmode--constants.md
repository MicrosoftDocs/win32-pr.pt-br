---
description: As \_ constantes de sinalizador de bit LINETERMMODE descrevem diferentes tipos de eventos em uma linha telefônica que pode ser roteada para um dispositivo de terminal.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: Constantes de LINETERMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411c1dd633ff1bef49e08eb127f4145f81f3d6785d07f3566431fe7b5d7e8fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518806"
---
# <a name="linetermmode_-constants"></a>\_Constantes LINETERMMODE

As constantes de sinalizador de bit **LINETERMMODE \_** descrevem diferentes tipos de eventos em uma linha telefônica que pode ser roteada para um dispositivo de terminal.

<dl> <dt>

<span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**botões de LINETERMMODE \_**
</dt> <dd> <dl> <dt>



Esses são eventos de pressionamento de botão enviados do terminal para a linha.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**exibição do LINETERMMODE \_**
</dt> <dd> <dl> <dt>



Essas são informações de exibição enviadas da linha para o terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ HOOKSWITCH**
</dt> <dd> <dl> <dt>



Esses são eventos Hookswitch enviados do terminal para a linha.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**lâmpadas LINETERMMODEs \_**
</dt> <dd> <dl> <dt>



Esses são eventos de lâmpada enviados da linha para o terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**
</dt> <dd> <dl> <dt>



Esse é o fluxo de mídia bidirecional associado a uma chamada na linha e no terminal. Use esse valor quando o roteamento de ambos os canais unidirecionais do fluxo de mídia de uma chamada não puder ser controlado independentemente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**
</dt> <dd> <dl> <dt>



Esse é o fluxo de mídia unidirecional da linha para o terminal associado a uma chamada na linha. Use esse valor quando o roteamento de ambos os canais unidirecionais do fluxo de mídia de uma chamada puder ser controlado independentemente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**
</dt> <dd> <dl> <dt>



Esse é o fluxo de mídia unidirecional do terminal para a linha associada a uma chamada na linha. Use esse valor quando o roteamento de ambos os canais unidirecionais do fluxo de mídia de uma chamada puder ser controlado independentemente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**\_toque LINETERMMODE**
</dt> <dd> <dl> <dt>



Essas são as informações de controle de toque enviadas do comutador para o terminal.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Essas constantes descrevem as classes de fluxo de controle e de informações que podem ser roteadas diretamente entre um dispositivo de linha e um dispositivo de terminal (como um conjunto de telefone).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




