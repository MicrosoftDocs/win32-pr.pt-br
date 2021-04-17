---
description: As \_ constantes LINEFEATURE listam as operações que podem ser invocadas em uma linha usando essa API.
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: Constantes de LINEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754733"
---
# <a name="linefeature_-constants"></a>\_Constantes LINEFEATURE

As **\_ constantes LINEFEATURE** listam as operações que podem ser invocadas em uma linha usando essa API.

<dl> <dt>

<span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



Operações específicas do dispositivo podem ser usadas na linha.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE \_ DEVSPECIFICFEAT**
</dt> <dd> <dl> <dt>



Recursos específicos do dispositivo podem ser usados na linha.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**encaminhar LINEFEATURE \_**
</dt> <dd> <dl> <dt>



O encaminhamento de todos os endereços pode ser usado na linha.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



A função [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (com um endereço de destino vazio) pode ser usada para ativar o recurso não incomodar em todos os endereços na linha. O LINEFEATURE \_ Forward também será definido. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



A função [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) pode ser usada para encaminhar chamadas em todos os endereços na linha para outros números. O LINEFEATURE \_ Forward também será definido. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



Uma chamada de saída pode ser colocada nessa linha usando um endereço não especificado.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE \_ SETDEVSTATUS**
</dt> <dd> <dl> <dt>



A função [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) pode ser invocada no dispositivo de linha. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



O controle de mídia pode ser definido nessa linha.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE \_ SETterminal**
</dt> <dd> <dl> <dt>



Os modos de terminal para essa linha podem ser definidos.

> [!Note]  
> Se nenhum dos novos bits "encaminhar" modificados estiver definido no membro **dwLineFeatures** em [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) , mas o \_ bit de encaminhamento LINEFEATURE for definido, qualquer um dos modos de encaminhamento poderá funcionar; o provedor de serviços simplesmente não especificou quais deles.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

As \_ constantes LINEFEATURE são usadas em [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (retornado por [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)). [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) relatórios, para uma determinada linha, quais recursos de linha podem ser realmente invocados enquanto a linha está no estado atual. Um aplicativo tornaria essa determinação dinâmica após as alterações de estado de linha, geralmente causada por endereço ou atividades relacionadas à chamada na linha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




