---
description: Obtém ou define um valor que representa o componente de dia do valor datetime.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime.Day (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d2483e52d9b40978a28f96bb5352df4f9abf4f89becf52550b82fd931580d7e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640496"
---
# <a name="swbemdatetimeday-property"></a>Propriedade SWbemDateTime.Day

A **propriedade Day** do objeto [**SWbemDateTime**](swbemdatetime.md) obtém ou define um valor que representa o componente day do valor datetime. O valor deverá estar no intervalo de 1 a 31 se [**IsInterval**](swbemdatetime-isinterval.md) for **FALSE.** No entanto, a verificação de erro não é sensível ao valor do mês. Portanto, o valor no intervalo de 31 não retornará um erro nos casos em que o valor [**de SWbemDateTime.Month**](swbemdatetime-month.md) for for a month of than 31 days (Fevereiro, abril, junho, setembro, novembro).

O valor padrão para **Day** é 01.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a>Valor da propriedade

## <a name="error-codes"></a>Códigos do Erro

Depois de obter ou definir a **propriedade Day,** o [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter o código de erro abaixo.

<dl> <dt>

**wbemErrValueOutOfRange** – 2147749931 (0x8004102B)
</dt> <dd>

Se [**IsInterval**](swbemdatetime-isinterval.md) for **TRUE** e o intervalo de valores corretos exceder 0 a 99999999.

</dd> </dl>

## <a name="examples"></a>Exemplos

Para ver exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores CIM [**DATETIME**](datetime.md) de e para o formato **FILETIME** ou **VT \_ DATE,** consulte [Tarefas WMI:](wmi-tasks--dates-and-times.md)Datas e Horas . Para uma descrição do formato CIM **DATETIME,** consulte [Formato de data e hora.](date-and-time-format.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

