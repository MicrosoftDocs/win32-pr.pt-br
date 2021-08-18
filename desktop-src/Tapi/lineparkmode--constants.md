---
description: As \_ constantes de sinalizador de bit LINEPARKMODE descrevem diferentes maneiras de chamadas de estacionamento.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: Constantes de LINEPARKMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3070ad3f9e56de5e4e1a026b5f779c59469e947ff55b530e9d5b414a1b3b53b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139999"
---
# <a name="lineparkmode_-constants"></a>\_Constantes LINEPARKMODE

As constantes de sinalizador de bit **LINEPARKMODE \_** descrevem diferentes maneiras de chamadas de estacionamento.

<dl> <dt>

<span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ direcionado**
</dt> <dd> <dl> <dt>



Especifica o parque de chamada direcionada. O endereço em que a chamada será estacionada deve ser fornecido para a opção.


</dt> </dl> </dd> <dt>

<span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE não \_ direcionado**
</dt> <dd> <dl> <dt>



Especifica o parque de chamada não direcionado. O endereço em que a chamada está estacionada é selecionado pelo comutador e fornecido pelo comutador para o aplicativo.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

As **\_ constantes LINEPARKMODE** são usadas durante o estacionamento de uma chamada. Consulte os recursos de dispositivo de endereço de uma linha para descobrir qual modo de estacionamento está disponível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




