---
description: As \_ constantes de sinalizador de bit LINESPECIALINFO descrevem os sinais de informações especiais que a rede pode usar para relatar várias operações de observação de rede e relatórios.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: Constantes de LINESPECIALINFO_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757616"
---
# <a name="linespecialinfo_-constants"></a>\_Constantes LINESPECIALINFO

As constantes de sinalizador de bit **LINESPECIALINFO \_** descrevem os sinais de informações especiais que a rede pode usar para relatar várias operações de observação de rede e relatórios. Elas são sequências de tons codificadas especiais transmitidas no início dos comunicados gravados do comunicado de rede.

<dl> <dt>

<span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO \_ CUSTIRREG**
</dt> <dd> <dl> <dt>



Esse tom de informação especial precede um número vago, AIS, Centrex de alteração de número e estação de trabalho, código de acesso não discado ou discado com erro ou mensagem do operador de interceptação manual (categoria de irregularidade do cliente). LINESPECIALINFO \_ CUSTIRREG também é relatado quando as informações de cobrança são rejeitadas e quando o endereço discado é bloqueado no comutador.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOcircuit**
</dt> <dd> <dl> <dt>



Esse tom de informações especiais precede um circuito de não ou um comunicado de emergência (categoria de bloqueio de tronco).


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**\_REordenar LINESPECIALINFO**
</dt> <dd> <dl> <dt>



Esse tom de informação especial precede um anúncio de reordenação (categoria de irregularização de equipamentos). \_A REordenação LINESPECIALINFO também é relatada quando o telefone é mantido offhook muito longo.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO não \_ disp.**
</dt> <dd> <dl> <dt>



As especificidades sobre o tom de informações especiais não estão disponíveis e não se tornarão conhecidas.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ desconhecido**
</dt> <dd> <dl> <dt>



As especificidades sobre o tom de informações especiais são desconhecidas no momento, mas podem ser conhecidas mais tarde.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo. Os 16 bits de ordem inferior são reservados.

Os tons de informação especiais são definidos para mensagens de consultoria e não são normalmente usados para cobrança ou finalidade de supervisão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




