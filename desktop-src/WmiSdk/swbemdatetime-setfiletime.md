---
description: Converte uma data no formato FILETIME da cadeia de caracteres para o formato de data e hora CIM.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Método SWbemDateTime. SetFileTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 138685ba4d6b63591bf460da3cdba219685f015d54789ca60a52660845b2e41a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739453"
---
# <a name="swbemdatetimesetfiletime-method"></a>Método SWbemDateTime. SetFileTime

O método **SetFileTime** do objeto [**SWbemDateTime**](swbemdatetime.md) converte uma data no formato **FILETIME** da cadeia de caracteres para o formato de [data e hora CIM](date-and-time-format.md) .

O formato **FILETIME** é uma estrutura datetime de 64 bits que representa o número de unidades de 100 nanossegundos desde o início de 1º de janeiro de 1601. Windows A instrumentação de gerenciamento (WMI) trata os valores de **FILETIME** como representações de cadeia de caracteres de números de 64 bits sem sinal.

Para obter a explicação da sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strFileTime* \[ no\]
</dt> <dd>

Valor **FILETIME** usado para definir o objeto.

</dd> <dt>

*bIsLocal* \[ em, opcional\]
</dt> <dd>

Se for **true**, *strFileTime* será interpretado como uma hora local. A propriedade UTC (tempo Universal Coordenado) contém a hora local convertida para o deslocamento UTC correto. Quando *bIsLocal* é **false**, *strFileTime* é convertido diretamente em um valor UTC com um deslocamento de 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Depois de concluir o método **SetFileTime** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter o código de erro na lista a seguir.

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021)
</dt> <dd>

O formato de *strFileTime* não é válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Após uma chamada bem-sucedida para **SetFileTime**, o valor [**DateTime**](datetime.md) é sempre interpretado como um valor absoluto (**DateTime**) e [**isinterval**](swbemdatetime-isinterval.md) é definido como **false**.

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

[**SWbemDateTime. SetVarDate**](swbemdatetime-setvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**HORÁRIO**](datetime.md)
</dt> </dl>

 

