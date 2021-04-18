---
description: As constantes de sinalizador de bit PHONEBUTTONSTATE descrevem as posições dos botões.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: Constantes de PHONEBUTTONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788046"
---
# <a name="phonebuttonstate_-constants"></a>PHONEBUTTONSTATE_ constantes

As constantes de sinalizador de bit **PHONEBUTTONSTATE_** descrevem as posições do botão.

<dl> <dt>

<span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**
</dt> <dd> <dl> <dt>



O botão está no estado "Down" (pressionado).


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**
</dt> <dd> <dl> <dt>



Indica que o estado para cima ou para baixo do botão não é conhecido pelo provedor de serviços e não se tornará conhecido em um momento futuro. (TAPI versões 1,4 e posteriores)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**
</dt> <dd> <dl> <dt>



Indica que o estado ativo ou inativo do botão não é conhecido neste momento, mas pode ser conhecido em um momento futuro. (TAPI versões 1,4 e posteriores)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**
</dt> <dd> <dl> <dt>



O botão está no estado "para cima".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada no telefone e não usar esses PHONEBUTTONSTATE_ valores para os quais a versão negociada não dá suporte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




