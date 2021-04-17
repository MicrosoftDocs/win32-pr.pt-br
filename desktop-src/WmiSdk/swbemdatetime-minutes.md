---
description: Obtém ou define um valor que representa o componente de minutos do valor DateTime.
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. Minutes (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cce55d731916d0e8180de1bde495566d4ed22c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763301"
---
# <a name="swbemdatetimeminutes-property"></a>Propriedade SWbemDateTime. Minutes

A propriedade **minutes** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define um valor que representa o componente de minutos do valor DateTime.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a>Valor da propriedade

## <a name="error-codes"></a>Códigos do Erro

Depois de obter ou definir a propriedade **minutes** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) poderá conter o código de erro abaixo.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B)
</dt> <dd>

O valor não estava no intervalo de 0 a 59.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se a propriedade **SWbemDateTime. Minutes** for definida como 1, a propriedade [**SWbemDateTime. Seconds**](swbemdatetime-seconds.md) conterá um valor que é deslocado por um segundo um erro de arredondamento que ocorre quando um valor **DateTime** de CIM é convertido em um valor de **\_ Data VT** . Se a propriedade **minutes** for definida como 0 em vez disso, a propriedade **Seconds** retornará o valor correto.

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

[**SWbemDateTime. MinutesSpecified**](swbemdatetime-minutesspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**HORÁRIO**](datetime.md)
</dt> </dl>

 

