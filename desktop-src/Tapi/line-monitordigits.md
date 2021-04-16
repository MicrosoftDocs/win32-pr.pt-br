---
description: A mensagem de MONITORDIGITS de linha TAPI \_ é enviada quando um dígito é detectado. O envio dessa mensagem é controlado com a função lineMonitorDigits.
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: Mensagem de LINE_MONITORDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758405"
---
# <a name="line_monitordigits-message"></a>Mensagem de MONITORDIGITS de linha \_

A mensagem **de \_ MONITORDIGITS de linha** TAPI é enviada quando um dígito é detectado. O envio dessa mensagem é controlado com a função [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) .


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

O byte de ordem inferior contém o último dígito recebido em uma representação de texto.

</dd> <dt>

*dwParam2* 
</dt> <dd>

O modo de dígito que foi detectado. Esse parâmetro deve ser apenas uma das [**\_ constantes LINEDIGITMODE**](linedigitmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

A "contagem de tiques" (número de milissegundos desde o início do Windows) em que o dígito especificado foi detectado. Para versões TAPI anteriores a 2,0, esse parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A mensagem de **linha \_ MONITORDIGITS** é enviada para o aplicativo que tem o monitoramento de dígito habilitado.

Como esse carimbo de data/hora pode ter sido gerado em um computador diferente daquele em que o aplicativo está sendo executado, ele é útil somente para comparação com outras mensagens com carimbo de data/hora semelhantes geradas no mesmo dispositivo de linha ( [**linha \_ GATHERDIGITS**](line-gatherdigits.md), [**\_ GENERATE line**](line-generate.md), [**line \_ MONITORMEDIA**](line-monitormedia.md), [**line \_ MONITORTONE**](line-monitortone.md)), para determinar seu tempo relativo (separação entre os eventos). A contagem em escala pode "encapsule" depois de aproximadamente 49,7 dias; os aplicativos devem levar isso em conta ao executar cálculos.

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

[**MONITORMEDIA de linha \_**](line-monitormedia.md)
</dt> <dt>

[**MONITORTONE de linha \_**](line-monitortone.md)
</dt> <dt>

[**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




