---
description: Valor booliana que indica se o componente UTC (Tempo Coordenado Universal) no valor datetime cim contém um intervalo ou um valor curinga.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime.UTCSpecified (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80c8ab92d07c2ef75ea57a66f6bae26c428780e15beeae31c9e5bd883407f03f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640366"
---
# <a name="swbemdatetimeutcspecified-property"></a>Propriedade SWbemDateTime.UTCSpecified

A **propriedade UTCSpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliana que indica se o componente UTC (Tempo Coordenado Universal) no valor datetime cim contém um intervalo ou um valor curinga. Se **UTCSpecified** for **TRUE** e [**IsInterval**](swbemdatetime-isinterval.md) for **FALSE,** [**SWbemDateTime.UTC**](swbemdatetime-utc.md) conterá um [**valor DATETIME.**](datetime.md) Um **valor DATETIME** que contém um intervalo não pode ser convertido no **formato DATE da VT \_** ou **no formato FILETIME.** Se **UTCSpecified for** **FALSE** e **IsInterval** for **TRUE,** **SWbemDateTime.UTC** conterá um intervalo.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a>Valor da propriedade

## <a name="examples"></a>Exemplos

Para ver exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores CIM [**DATETIME**](datetime.md) de e para o formato **FILETIME** ou **VT \_ DATE,** consulte [Tarefas WMI:](wmi-tasks--dates-and-times.md)Datas e Horas . Para ver uma descrição do formato datetime CIM, consulte [Formato de data e hora.](date-and-time-format.md)

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

[**SWbemDateTime.UTC**](swbemdatetime-utc.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




