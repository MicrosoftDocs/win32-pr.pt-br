---
description: As \_ constantes de sinalizador de bit LINEFORWARDMODE descrevem as condições sob as quais as chamadas para um endereço podem ser encaminhadas.
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: Constantes de LINEFORWARDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779899"
---
# <a name="lineforwardmode_-constants"></a>\_Constantes LINEFORWARDMODE

As constantes de sinalizador de bit **LINEFORWARDMODE \_** descrevem as condições sob as quais as chamadas para um endereço podem ser encaminhadas.

<dl> <dt>

<span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE \_ ocupado**
</dt> <dd> <dl> <dt>



Encaminhe todas as chamadas em ocupado, independentemente de sua origem. Use esse valor ao encaminhar para chamadas internas e externas em ocupado e sem resposta não podem ser controladas separadamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE \_ BUSYEXTERNAL**
</dt> <dd> <dl> <dt>



Encaminhar todas as chamadas externas em ocupado. Use esse valor quando o encaminhamento para chamadas internas e externas em ocupado e sem resposta puder ser controlado separadamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE \_ BUSYINTERNAL**
</dt> <dd> <dl> <dt>



Encaminhar todas as chamadas internas em ocupado. Use esse valor quando o encaminhamento para chamadas internas e externas em ocupado e sem resposta puder ser controlado separadamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE \_ BUSYNA**
</dt> <dd> <dl> <dt>



Encaminhe todas as chamadas para ocupado/sem resposta, independentemente de sua origem. Use esse valor ao encaminhar para chamadas internas e externas em ocupado e sem resposta não podem ser controladas separadamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE \_ BUSYNAEXTERNAL**
</dt> <dd> <dl> <dt>



Encaminhe todas as chamadas externas para ocupado/sem resposta. Use este valor quando o encaminhamento de chamadas em ocupado e sem resposta não puder ser controlado separadamente para chamadas internas.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE \_ BUSYNAINTERNAL**
</dt> <dd> <dl> <dt>



Encaminhe todas as chamadas internas em resposta/não. Use este valor quando o encaminhamento de chamadas em ocupado e sem resposta não puder ser controlado separadamente para chamadas internas.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE \_ BUSYNASPECIFIC**
</dt> <dd> <dl> <dt>



Encaminhar em ocupado/não responder a todas as chamadas originadas em um endereço especificado (encaminhamento de chamada seletiva).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE \_ BUSYSPECIFIC**
</dt> <dd> <dl> <dt>



Encaminhar em ocupado todas as chamadas originadas em um endereço especificado (encaminhamento de chamada seletiva).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE \_ NOANSW**
</dt> <dd> <dl> <dt>



Encaminhe todas as chamadas sem resposta, independentemente de sua origem. Use esse valor quando o encaminhamento de chamada para chamadas internas e externas sem resposta não puder ser controlado separadamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE \_ NOANSWEXTERNAL**
</dt> <dd> <dl> <dt>



Encaminhe todas as chamadas externas sem resposta. Usar esse valor ao encaminhar para chamadas internas e externas sem resposta pode ser controlado separadamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE \_ NOANSWINTERNAL**
</dt> <dd> <dl> <dt>



Encaminhe todas as chamadas internas sem resposta. Usar esse valor ao encaminhar para chamadas internas e externas sem resposta pode ser controlado separadamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE \_ NOANSWSPECIFIC**
</dt> <dd> <dl> <dt>



Encaminhar sem responder a todas as chamadas originadas em um endereço especificado (encaminhamento de chamada seletiva).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE não \_ disp.**
</dt> <dd> <dl> <dt>



As chamadas são encaminhadas, mas as condições sob as quais o encaminhamento ocorrerão não são conhecidas e nunca serão conhecidas pelo provedor de serviços. (TAPI versões 1,4 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE \_ UNCOND**
</dt> <dd> <dl> <dt>



Encaminhe todas as chamadas incondicionalmente, independentemente de sua origem. Use esse valor quando o encaminhamento incondicional para chamadas internas e externas não puder ser controlado separadamente. O encaminhamento incondicional de substituições em direção ao ocupado e/ou nenhuma condição de resposta.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE \_ UNCONDEXTERNAL**
</dt> <dd> <dl> <dt>



Encaminhe todas as chamadas externas incondicionalmente. Use esse valor quando o encaminhamento incondicional para chamadas internas e externas puder ser controlado separadamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE \_ UNCONDINTERNAL**
</dt> <dd> <dl> <dt>



Encaminhe todas as chamadas internas incondicionalmente. Use esse valor quando o encaminhamento incondicional para chamadas internas e externas puder ser controlado separadamente.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE \_ UNCONDSPECIFIC**
</dt> <dd> <dl> <dt>



Encaminhe incondicionalmente todas as chamadas originadas em um endereço especificado (encaminhamento de chamada seletiva).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE \_ desconhecido**
</dt> <dd> <dl> <dt>



As chamadas são encaminhadas, mas as condições sob as quais o encaminhamento ocorrerão não são conhecidas neste momento. É possível que as condições sejam conhecidas em um momento futuro. (TAPI versões 1,4 e posteriores)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Os sinalizadores de bits definidos por LINEFORWARDMODE \_ não são ortogonal. O encaminhamento incondicional ignora qualquer condição específica, como ocupado ou sem resposta. Se o encaminhamento incondicional não estiver em vigor, o encaminhamento em ocupado e sem resposta poderá ser controlado separadamente ou não separadamente. Se controlado separadamente, os \_ sinalizadores LINEFORWARDMODE Busy e LINEFORWARDMODE \_ NOANSW podem ser usados separadamente. Se não for controlado separadamente, o sinalizador LINEFORWARDMODE \_ BUSYNA deverá ser usado. Da mesma forma, se o encaminhamento de chamadas internas e externas puder ser controlado separadamente, \_ os sinalizadores externos LINEFORWARDMODE internos e LINEFORWARDMODE \_ poderão ser usados separadamente; caso contrário, a combinação será usada.

Os recursos de endereço indicam quais modos de encaminhamento estão disponíveis para cada endereço atribuído a uma linha. Um aplicativo pode usar [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) para definir as condições de encaminhamento no comutador.

Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esses valores de LINEFORWARDMODE \_ se a versão negociada não oferecer suporte a eles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




