---
description: A mensagem de LINE_MONITORMEDIA TAPI é enviada quando uma alteração no tipo de mídia de chamadas é detectada. O envio dessa mensagem é controlado com a função lineMonitorMedia
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: Mensagem de LINE_MONITORMEDIA (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b6e3d0d2928ab3256b844a27727657978dbe0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789453"
---
# <a name="line_monitormedia-message"></a>Mensagem de MONITORMEDIA de linha \_

A mensagem **de \_ MONITORMEDIA de linha** TAPI é enviada quando uma alteração no tipo de mídia da chamada é detectada. O envio dessa mensagem é controlado com a função [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) .


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para a chamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O novo tipo de mídia (ou modo). Esse parâmetro deve ser apenas uma das [**\_ constantes LINEMEDIAMODE**](linemediamode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

A "contagem de tiques" (número de milissegundos desde o início do Windows) em que a mídia especificada foi detectada. Para versões TAPI anteriores a 2,0, esse parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A mensagem de **linha \_ MONITORMEDIA** é enviada para o aplicativo que habilitou o monitoramento de mídia para o tipo de mídia detectado.

Como esse carimbo de data/hora pode ter sido gerado em um computador diferente daquele em que o aplicativo está sendo executado, ele é útil somente para comparação com outras mensagens com carimbo de data/hora semelhantes geradas no mesmo dispositivo de linha ( [**linha \_ GATHERDIGITS**](line-gatherdigits.md), [**\_ GENERATE line**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), [**line \_ MONITORTONE**](line-monitortone.md)), para determinar seu tempo relativo (separação entre os eventos). A contagem em escala pode "encapsule" depois de aproximadamente 49,7 dias; os aplicativos devem levar isso em conta ao executar cálculos.

Se o provedor de serviços não gerar o carimbo de data/hora (por exemplo, se ele foi criado usando uma versão anterior da TAPI), a TAPI fornecerá um carimbo de data/hora no ponto mais próximo do provedor de serviços que gera o evento para que o carimbo de data/hora sintetizado seja o mais preciso possível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GATHERDIGITS de linha \_**](line-gatherdigits.md)
</dt> <dt>

[**geração de linha \_**](line-generate.md)
</dt> <dt>

[**MONITORDIGITS de linha \_**](line-monitordigits.md)
</dt> <dt>

[**MONITORTONE de linha \_**](line-monitortone.md)
</dt> </dl>

 

 




