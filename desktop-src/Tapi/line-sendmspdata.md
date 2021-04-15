---
description: A mensagem de SENDMSPDATA da linha TSPI \_ é enviada quando o provedor de serviços de telefonia (TSP) deseja passar informações para o MSP (provedor de serviços de mídia).
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: Mensagem de LINE_SENDMSPDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761354"
---
# <a name="line_sendmspdata-message"></a>Mensagem de SENDMSPDATA de linha \_

A mensagem **de \_ SENDMSPDATA da linha** TSPI é enviada quando o provedor de serviços de telefonia (TSP) deseja passar informações para o MSP (provedor de serviços de mídia).


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*htLine* 
</dt> <dd>

O identificador TAPI para a linha.

</dd> <dt>

*htCall* 
</dt> <dd>

O identificador TAPI para a chamada.

</dd> <dt>

*dwMsg* 
</dt> <dd>

A linha de valor \_ SENDMSPDATA.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identifica o MSP que deve receber a mensagem. Se for 0, a mensagem será enviada a todos os MSPs. Esse é o identificador que é passado para a função [**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) .

</dd> <dt>

*dwParam2* 
</dt> <dd>

O buffer a ser passado para o MSP. O buffer não é interpretado pela TAPI.

</dd> <dt>

*dwParam3* 
</dt> <dd>

O tamanho, em bytes, do buffer em *dwParam2*.

</dd> </dl>

## <a name="remarks"></a>Comentários

O provedor de serviços deve negociar uma TAPI versão 3,0 ou posterior para que essa mensagem opere.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| parâmetro<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre o MSP (provedor de serviços de mídia)](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[**TSPI \_ lineCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[**TSPI \_ lineRecieveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

