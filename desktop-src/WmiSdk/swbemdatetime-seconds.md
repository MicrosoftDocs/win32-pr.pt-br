---
description: Obtém ou define um valor que representa o componente de segundos do valor DateTime.
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. Seconds (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4d30095e5464736b3db984b71f94a216c29f4327227a5e5b99becfbcae5e1a58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816177"
---
# <a name="swbemdatetimeseconds-property"></a>Propriedade SWbemDateTime. Seconds

A propriedade **Seconds** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define um valor que representa o componente de segundos do valor DateTime.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a>Valor da propriedade

## <a name="error-codes"></a>Códigos do Erro

Depois de obter ou definir a propriedade **Seconds** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) poderá conter o código de erro abaixo.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B)
</dt> <dd>

O valor não estava no intervalo de 0 a 59.

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade **SWbemDateTime. Seconds** pode conter um valor incorreto se a propriedade [**SWbemDateTime. Minutes**](swbemdatetime-minutes.md) tiver sido definida como 1. Ele contém um valor que é deslocado em um segundo devido a um erro de arredondamento que ocorre quando um valor [**DateTime**](datetime.md) de CIM é convertido em um valor de **\_ Data VT** . Se a propriedade **minutes** for definida como 0 (zero) em vez disso, a propriedade **segundos** retornará o valor correto.

## <a name="examples"></a>Exemplos

Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md). Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMDATETIME CLSID<br/>                                                         |
| IID<br/>                      | ISWbemDateTime de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemDateTime. SecondsSpecified**](swbemdatetime-secondsspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**HORÁRIO**](datetime.md)
</dt> </dl>

 

