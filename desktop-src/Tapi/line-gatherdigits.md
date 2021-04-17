---
description: A mensagem de GATHERDIGITS de linha TAPI \_ é enviada quando a solicitação de coleta de dígitos em buffer atual termina ou é cancelada. O buffer de dígitos pode ser examinado depois que essa mensagem tiver sido recebida pelo aplicativo.
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: Mensagem de LINE_GATHERDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754736"
---
# <a name="line_gatherdigits-message"></a>Mensagem de GATHERDIGITS de linha \_

A mensagem **de \_ GATHERDIGITS de linha** TAPI é enviada quando a solicitação de coleta de dígitos em buffer atual termina ou é cancelada. O buffer de dígitos pode ser examinado depois que essa mensagem tiver sido recebida pelo aplicativo.


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

O motivo pelo qual a coleta de dígitos foi encerrada. Esse parâmetro deve ser apenas uma das [**\_ constantes LINEGATHERTERM**](linegatherterm--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

A "contagem de tiques" (número de milissegundos desde o início do Windows) em que a coleta de dígitos foi concluída. Para versões TAPI anteriores a 2,0, esse parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A mensagem de **linha \_ GATHERDIGITS** é enviada somente para o aplicativo que iniciou a coleta de dígitos na chamada usando [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).

Se a função [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) for usada para cancelar uma solicitação anterior para coletar dígitos, a TAPI enviará uma mensagem **\_ GATHERDIGITS de linha** com *dwParam1* definido como LINEGATHERTERM \_ Cancelar para o aplicativo indicando que o buffer originalmente especificado contém os dígitos coletados até o cancelamento.

Como o carimbo de data/hora especificado por *dwParam3* pode ter sido gerado em um computador diferente daquele em que o aplicativo está sendo executado, ele é útil somente para comparação com outras mensagens de carimbo de data/hora semelhantes geradas no mesmo dispositivo de linha ( [**\_ geração de linha**](line-generate.md), [**linha \_ MONITORDIGITS**](line-monitordigits.md), linha [**\_ MONITORMEDIA**](line-monitormedia.md), [**linha \_ MONITORTONE**](line-monitortone.md)), para determinar seu tempo relativo (separação entre eventos). A contagem em escala pode "encapsule" depois de aproximadamente 49,7 dias; os aplicativos devem levar isso em conta ao executar cálculos.

Se o provedor de serviços não gerar o carimbo de data/hora (por exemplo, se ele foi criado usando uma versão anterior da TAPI), a TAPI fornecerá um carimbo de data/hora no ponto mais próximo do provedor de serviços que gera o evento para que o carimbo de data/hora sintetizado seja o mais preciso possível.

> [!Note]  
> Quando um aplicativo invoca qualquer operação assíncrona que grava dados de volta na memória do aplicativo, o aplicativo deve manter essa memória disponível para gravação até que uma mensagem de [**\_ resposta**](line-reply.md) ou de **linha \_ GATHERDIGITS** seja recebida.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**geração de linha \_**](line-generate.md)
</dt> <dt>

[**MONITORDIGITS de linha \_**](line-monitordigits.md)
</dt> <dt>

[**MONITORMEDIA de linha \_**](line-monitormedia.md)
</dt> <dt>

[**MONITORTONE de linha \_**](line-monitortone.md)
</dt> <dt>

[**resposta de linha \_**](line-reply.md)
</dt> <dt>

[**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




