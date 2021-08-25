---
description: A mensagem de geração de linha TAPI \_ é enviada para notificar o aplicativo que o dígito atual ou a geração de Tom foi encerrada.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: Mensagem de LINE_GENERATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3ab0d503d7515fec2cdbd1676eed235cced88e2adfa9fcc1dd354663929e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774236"
---
# <a name="line_generate-message"></a>Mensagem de geração de linha \_

A mensagem **de \_ geração de linha** TAPI é enviada para notificar o aplicativo que o dígito atual ou a geração de Tom foi encerrada. Somente uma solicitação de geração desse tipo pode estar em andamento em uma chamada específica a qualquer momento. Essa mensagem também é enviada quando a geração de dígitos ou tons é cancelada.


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

O motivo pelo qual a geração de dígitos ou tons foi encerrada. Esse parâmetro deve ser apenas uma das [**\_ constantes LINEGENERATETERM**](linegenerateterm--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

a "contagem de tiques" (número de milissegundos desde Windows iniciado) em que a geração de dígitos ou tons foi concluída. Para versões de API anteriores a 2,0, esse parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A mensagem de **\_ geração de linha** é enviada somente para o aplicativo que solicitou a geração de dígito ou de Tom.

Como o carimbo de data/hora especificado por *dwParam3* pode ter sido gerado em um computador diferente daquele em que o aplicativo está sendo executado, ele é útil somente para comparação com outras mensagens de carimbo de data/hora semelhantes geradas no mesmo dispositivo de linha ( [**line \_ GATHERDIGITS**](line-gatherdigits.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), line [**\_ MONITORMEDIA**](line-monitormedia.md), [**line \_ MONITORTONE**](line-monitortone.md)), a fim de determinar seu tempo relativo (separação entre eventos). A contagem em escala pode "encapsule" depois de aproximadamente 49,7 dias; os aplicativos devem levar isso em conta ao executar cálculos.

Se o provedor de serviços não gerar o carimbo de data/hora (por exemplo, se ele foi criado usando uma versão anterior da TAPI), a TAPI fornecerá um carimbo de data/hora no ponto mais próximo do provedor de serviços que gera o evento para que o carimbo de data/hora sintetizado seja o mais preciso possível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GATHERDIGITS de linha \_**](line-gatherdigits.md)
</dt> <dt>

[**MONITORDIGITS de linha \_**](line-monitordigits.md)
</dt> <dt>

[**MONITORMEDIA de linha \_**](line-monitormedia.md)
</dt> <dt>

[**MONITORTONE de linha \_**](line-monitortone.md)
</dt> </dl>

 

 




