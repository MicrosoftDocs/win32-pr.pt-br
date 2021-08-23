---
description: A mensagem tapi LINE_MONITORMEDIA é enviada quando uma alteração no tipo de mídia de chamadas é detectada. O envio dessa mensagem é controlado com a função lineMonitorMedia
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: LINE_MONITORMEDIA mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fec42f0e8aa630b518f989a9237762edc71281767b281f7af78eb54210138d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519016"
---
# <a name="line_monitormedia-message"></a>Mensagem LINE \_ MONITORMEDIA

A mensagem TAPI **LINE \_ MONITORMEDIA** é enviada quando uma alteração no tipo de mídia da chamada é detectada. O envio dessa mensagem é controlado com a [**função lineMonitorMedia.**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia)


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um alça para a chamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

O novo tipo de mídia (ou modo). Esse parâmetro deve ser uma e apenas uma das [**\_ constantes LINEMEDIAMODE**](linemediamode--constants.md).

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

A "contagem de tiques" (número de milissegundos desde Windows iniciada) na qual a mídia especificada foi detectada. Para versões TAPI anteriores à 2.0, esse parâmetro não éusado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem LINE \_ MONITORMEDIA** é enviada ao aplicativo que habilitar o monitoramento de mídia para o tipo de mídia detectado.

Como esse timestamp pode ter sido gerado em um computador que não seja aquele em que o aplicativo está sendo executado, ele é útil apenas para comparação com outras mensagens com data/hora semelhante geradas no mesmo dispositivo de linha [**(LINE \_ GATHERDIGITS,**](line-gatherdigits.md) [**LINE \_ GENERATE,**](line-generate.md) [**LINE \_ MONITORDIGITS,**](line-monitordigits.md) [**LINE \_ MONITORTONE**](line-monitortone.md)), para determinar o tempo relativo (separação entre eventos). A contagem de tiques pode "envolver" após aproximadamente 49,7 dias; os aplicativos devem levar isso em conta ao executar cálculos.

Se o provedor de serviços não gerar o timestamp (por exemplo, se ele tiver sido criado usando uma versão anterior da TAPI), a TAPI fornece um timestamp no ponto mais próximo do provedor de serviços que gera o evento para que o timestamp sintetizado seja o mais preciso possível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GATHERDIGITS DE LINHA**](line-gatherdigits.md)
</dt> <dt>

[**GERAÇÃO DE \_ LINHA**](line-generate.md)
</dt> <dt>

[**MONITOR \_ DE LINHADIGITS**](line-monitordigits.md)
</dt> <dt>

[**MONITORTONE \_ DE LINHA**](line-monitortone.md)
</dt> </dl>

 

 




