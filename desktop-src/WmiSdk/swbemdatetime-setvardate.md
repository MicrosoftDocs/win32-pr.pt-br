---
description: Converte uma data no formato de \_ Data VT para o formato de datahora CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: Método SWbemDateTime. SetVarDate (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8641bad2c59f100b689c74e23faf727bc80d2f49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297426"
---
# <a name="swbemdatetimesetvardate-method"></a>Método SWbemDateTime. SetVarDate

O método **SetVarDate** do objeto [**SWbemDateTime**](swbemdatetime.md) converte uma data no formato de **\_ Data VT** para o formato de [datahora CIM](date-and-time-format.md) .

Um valor de **\_ Data VT** é um valor DateTime de variante que Visual Basic e o uso do ActiveX.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vDate* \[ no\]
</dt> <dd>

O valor de data da variante para definir o objeto. Esse parâmetro deve estar no formato **de \_ Data VT** .

</dd> <dt>

*bIsLocal* \[ em, opcional\]
</dt> <dd>

Se for **true**, *vDate* será interpretado como uma hora local e a propriedade UTC (tempo Universal Coordenado) conterá a hora local que é convertida no deslocamento UTC correto. Quando *bIsLocal* é **false**, *vDate* é convertido diretamente em um valor UTC com um deslocamento de zero (0).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Depois de concluir o método **SetVarDate** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter o código de erro na lista a seguir.

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021)
</dt> <dd>

O formato de *vDate* não é válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Após uma chamada bem-sucedida para **SetVarDate**, o valor [**DateTime**](datetime.md) é interpretado como um valor de DateTime absoluto em vez de um intervalo, e a propriedade [**isinterval**](swbemdatetime-isinterval.md) é definida como **false**.

A função intrínseca Visual Basic ou VBScript [CDATA](/previous-versions//2dt118h2(v=vs.85)) fornece um valor [**DateTime**](datetime.md) no formato **de \_ Data VT** para entrada para **SetVarDate**.

## <a name="examples"></a>Exemplos

Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md). Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).

O exemplo de código de [conversão de data para WMI Date-Time formato](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript na galeria do TechNet usa SetVarDate para converter um valor de data e hora regular no formato de data e hora UTC.

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

[**SWbemDateTime. SetFileTime**](swbemdatetime-setfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**HORÁRIO**](datetime.md)
</dt> </dl>

 

