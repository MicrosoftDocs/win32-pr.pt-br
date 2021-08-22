---
description: As \_ constantes de sinalizador de bit LINETRANSLATERESULT descrevem vários resultados de uma conversão de endereço.
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: Constantes de LINETRANSLATERESULT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba28c04bc52d3857d76bffefed5fe07803954e72f4a5e7e05ffa22d4ee6c646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518776"
---
# <a name="linetranslateresult_-constants"></a>\_Constantes LINETRANSLATERESULT

As constantes de sinalizador de bit **LINETRANSLATERESULT \_** descrevem vários resultados de uma conversão de endereço.

<dl> <dt>

<span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**\_Canonical LINETRANSLATERESULT**
</dt> <dd> <dl> <dt>



Indica que a cadeia de caracteres de entrada estava em um formato canônico válido.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT \_ DIALBILLING**
</dt> <dd> <dl> <dt>



Indica que o endereço retornado contém um "$".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>



Indica que o endereço retornado contém um "W".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



Indica que o endereço retornado contém um "?".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Indica que o endereço retornado contém um "@".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT \_ International**
</dt> <dd> <dl> <dt>



Indica que a chamada está sendo tratada como uma chamada internacional (o código de país ou região especificado no endereço de destino é diferente do código de país ou região especificado para o **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT \_**
</dt> <dd> <dl> <dt>



Indica que a chamada local está sendo conectada como longa distância porque o país ou a região tem chamada tarifada e o prefixo aparece no **TollPrefixList** do **CurrentLocation**.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT \_ local**
</dt> <dd> <dl> <dt>



Indica que a chamada está sendo tratada como uma chamada local (o código de país ou região e o código de área especificados no endereço de destino são os mesmos especificados para o **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT \_ LONGDISTANCE**
</dt> <dd> <dl> <dt>



Indica que a chamada está sendo tratada como uma chamada de longa distância (o código de país ou região especificado no endereço de destino é o mesmo, mas o código de área é diferente daqueles especificados para o **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT \_ NOTINTOLLLIST**
</dt> <dd> <dl> <dt>



Indica que o país ou região dá suporte à chamada tarifada, mas o prefixo não aparece no **TollPrefixList**, portanto, a chamada é discada como uma chamada local. Observe que, se tanto o inativor quanto o NOTINTOLLIST estiverem desligados, o país ou região atual não oferecerá suporte a prefixos de chamada e os elementos de interface do usuário relacionados aos prefixos de chamada não deverão ser apresentados ao usuário; Se qualquer um desses bits for ativado, o país ou região oferecerá suporte a listas de chamadas e os elementos de interface do usuário relacionados deverão ser habilitados.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT \_ NOtranslation**
</dt> <dd> <dl> <dt>



Indica que a conversão de endereço não está disponível. Esse elemento é exposto somente a aplicativos que negociam uma versão TAPI do 3,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT \_ VOICEDETECT**
</dt> <dd> <dl> <dt>



Indica que o endereço de discagem retornado contém um ":". Esse elemento é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou superior.

> [!Note]  
> O caractere ":" (dois-pontos) será adicionado à lista de caracteres que podem ser inseridos em uma cadeia de caracteres de discagem e passados para os endereços de destino. A tentativa de passá-lo de um aplicativo para um dispositivo de linha que dá suporte a uma versão de API anterior a 2,0 provavelmente resultará em LINEERR \_ INVALADDRESS ou possivelmente no caractere sendo ignorado inteiramente. O significado desse caractere é "Pause até que um prompt de voz seja detectado e continue discando"; Ele é destinado ao uso ao discar automaticamente para sistemas que fornecem prompts de voz, como processadores de cartão de chamada de longa distância.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




