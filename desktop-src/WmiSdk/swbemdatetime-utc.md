---
description: Obtém ou define a representação UTC (tempo Universal Coordenado) do valor DateTime.
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. UTC (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80a4c32e47b94289f66999fdbf1f7daf5f9f03cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810864"
---
# <a name="swbemdatetimeutc-property"></a>Propriedade SWbemDateTime. UTC

A propriedade **UTC** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define a representação UTC (tempo Universal Coordenado) do valor **DateTime** . O UTC é o tempo definido pelo padrão de tempo mundial. O UTC substituiu o horário de Greenwich (GMT). Um valor UTC com um deslocamento zero é o mesmo que GMT com um deslocamento zero. O número assinado deve estar no intervalo de-720 até 720 ou o erro **wbemErrValueOutOfRange** é retornado.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a>Valor da propriedade

## <a name="error-codes"></a>Códigos do Erro

Depois de obter ou definir a propriedade **UTC** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) poderá conter o código de erro abaixo.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B)
</dt> <dd>

O valor não estava no intervalo de-720 até 720.

</dd> </dl>

## <a name="examples"></a>Exemplos

Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md). Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMDATETIME CLSID<br/>                                                         |
| IID<br/>                      | ISWbemDateTime de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemDateTime. UTCSpecified**](swbemdatetime-utcspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**HORÁRIO**](datetime.md)
</dt> </dl>

 

