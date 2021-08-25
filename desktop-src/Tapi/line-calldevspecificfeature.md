---
description: A mensagem de CALLDEVSPECIFICFEATURE da linha TSPI \_ é enviada para a função de retorno de chamada LINEEVENT para notificar a TAPI sobre eventos específicos do dispositivo que ocorrem em uma linha ou endereço.
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: Mensagem de LINE_CALLDEVSPECIFICFEATURE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8dde8377f952f02f021209b01f846ba323cc7dbf8795743422e2c83e457b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873626"
---
# <a name="line_calldevspecificfeature-message"></a>Mensagem de CALLDEVSPECIFICFEATURE de linha \_

A mensagem **de \_ CALLDEVSPECIFICFEATURE da linha** TSPI é enviada para a função de retorno de chamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) para notificar a TAPI sobre eventos específicos do dispositivo que ocorrem em uma linha ou endereço. O significado da mensagem e a interpretação dos parâmetros *dwParam1* por meio de *dwParam3* são específicos do dispositivo.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*htLine* 
</dt> <dd>

O identificador de objeto TAPI opaco para o dispositivo de linha.

</dd> <dt>

*htCall* 
</dt> <dd>

O identificador de objeto TAPI opaco para o dispositivo de chamada.

</dd> <dt>

*dwMsg* 
</dt> <dd>

A linha de valor \_ CALLDEVSPECIFICFEATURE.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Específico do dispositivo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Específico do dispositivo.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico do dispositivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **mensagem \_ CALLDEVSPECIFICFEATURE de linha** é usada por um provedor de serviços em conjunto com a função [**\_ lineDevSpecificFeature do TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) . Seu significado é específico ao dispositivo.

A TAPI envia a mensagem de [**linha \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) para os aplicativos em resposta ao recebimento desta mensagem de um provedor de serviços. Os parâmetros *htLine* e *htCall* são convertidos para o *HCall* apropriado como o parâmetro *hDevice* no nível TAPI. Os parâmetros *dwParam1*, *dwParam2* e *dwParam3* são passados por meio de não modificado.

Não há nenhuma mensagem diretamente correspondente no nível de TAPI, embora essa mensagem seja muito semelhante à linha \_ DEVSPECIFICFEATURE. No nível de TSPI, as mensagens de recurso específicas do dispositivo são divididas entre os eventos de relatório em linhas e endereços, e os eventos de relatório em chamadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DEVSPECIFICFEATURE de linha \_**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))
</dt> <dt>

[**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 

