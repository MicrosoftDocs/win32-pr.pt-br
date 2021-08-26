---
description: A mensagem de CALLDEVSPECIFIC da linha TSPI \_ é enviada para a função de retorno de chamada LINEEVENT para notificar a TAPI sobre eventos específicos do dispositivo que ocorrem em uma chamada.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: Mensagem de LINE_CALLDEVSPECIFIC (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9930da3c30d51781b10b28ed7a712cb681950eaea1a387212a5e0894658a9125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012596"
---
# <a name="line_calldevspecific-message"></a>Mensagem de CALLDEVSPECIFIC de linha \_

A mensagem **de \_ CALLDEVSPECIFIC da linha** TSPI é enviada para a função de retorno de chamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) para notificar a TAPI sobre eventos específicos do dispositivo que ocorrem em uma chamada. O significado da mensagem e a interpretação dos parâmetros *dwParam1* por meio de *dwParam3* são específicos do dispositivo.


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

A linha de valor \_ CALLDEVSPECIFIC.

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

A **mensagem \_ CALLDEVSPECIFIC de linha** é usada por um provedor de serviços em conjunto com a função [**\_ lineDevSpecific do TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) . Seu significado é específico ao dispositivo.

A TAPI envia a mensagem de [**linha \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) para os aplicativos em resposta ao recebimento desta mensagem de um provedor de serviços. Os parâmetros *htLine* e *htCall* são convertidos para o *HCall* apropriado como o parâmetro *hDevice* no nível TAPI. Os parâmetros *dwParam1*, *dwParam2* e *dwParam3* são passados por meio de não modificado.

Não há nenhuma mensagem diretamente correspondente no nível de TAPI, embora essa mensagem seja muito semelhante à [**linha \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)). No nível de TSPI, as mensagens específicas do dispositivo são divididas entre os eventos de relatório em linhas e endereços, e os eventos de relatório em chamadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DEVSPECIFIC de linha \_**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 

