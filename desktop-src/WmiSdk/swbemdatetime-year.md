---
description: Obtém ou define um valor que representa o componente de ano do valor DATETIME.
ms.assetid: eab3738a-c92a-4602-b1ee-e2547da88308
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. Year (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Year
- ISWbemDateTime.Year
- ISWbemDateTime.get_Year
- ISWbemDateTime.put_Year
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe8988b3772f0f5d976c38eb5e9cc44fb9c4ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789277"
---
# <a name="swbemdatetimeyear-property"></a>Propriedade SWbemDateTime. Year

A propriedade **year** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define um valor que representa o componente de ano do valor [**DateTime**](datetime.md) . O valor deve estar no intervalo de 0000-9999 ou o erro wbemErrValueOutOfRange é retornado.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
SWbemDateTime.Year As Long
```



## <a name="property-value"></a>Valor da propriedade

## <a name="error-codes"></a>Códigos do Erro

Depois de obter ou definir a propriedade **year** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) poderá conter o código de erro abaixo.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B)
</dt> <dd>

O valor não estava no intervalo de 0000 a 9999.

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

[**SWbemDateTime. YearSpecified**](swbemdatetime-yearspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**HORÁRIO**](datetime.md)
</dt> </dl>

 

