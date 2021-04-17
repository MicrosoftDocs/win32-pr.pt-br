---
description: A mensagem de MONITORTONE de linha TAPI \_ é enviada quando um tom é detectado. O envio dessa mensagem é controlado com a função lineMonitorTones.
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: Mensagem de LINE_MONITORTONE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769409"
---
# <a name="line_monitortone-message"></a>Mensagem de MONITORTONE de linha \_

A mensagem **de \_ MONITORTONE de linha** TAPI é enviada quando um tom é detectado. O envio dessa mensagem é controlado com a função [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) .


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

A instância de retorno de chamada fornecida ao abrir a linha do telefonema.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O membro **dwAppSpecific** específico do aplicativo da estrutura [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) para o Tom que foi detectado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

A "contagem de tiques" (número de milissegundos desde o início do Windows) em que o Tom foi detectado. Para versões de API anteriores a 2,0, esse parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A mensagem de **linha \_ MONITORTONE** é enviada somente para o aplicativo que solicitou o monitoramento do Tom.

Como esse carimbo de data/hora pode ter sido gerado em um computador diferente daquele em que o aplicativo está sendo executado, ele é útil somente para comparação com outras mensagens com carimbo de data/hora semelhantes geradas no mesmo dispositivo de linha ( [**linha \_ GATHERDIGITS**](line-gatherdigits.md), [**\_ GENERATE line**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), **line \_ MONITORTONE**), para determinar seu tempo relativo (separação entre os eventos). A contagem em escala pode "encapsule" depois de aproximadamente 49,7 dias; os aplicativos devem levar isso em conta ao executar cálculos.

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

[**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




