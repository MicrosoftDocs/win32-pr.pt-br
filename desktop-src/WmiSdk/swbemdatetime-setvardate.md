---
description: Converte uma data no formato DATE da VT \_ para o formato datetime CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: Método SWbemDateTime.SetVarDate (Wbemdisp.h)
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
ms.openlocfilehash: 56d193bd2faffd51507ec4a913c7ee068b055dcf45ca756e801431659768c47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050094"
---
# <a name="swbemdatetimesetvardate-method"></a>Método SWbemDateTime.SetVarDate

O **método SetVarDate** do objeto [**SWbemDateTime**](swbemdatetime.md) converte uma data no formato **DATE da VT \_** para o [formato datetime CIM.](date-and-time-format.md)

Um **valor date \_ de VT** é um valor de datetime variante que Visual Basic e ActiveX usar.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vdate* \[ Em\]
</dt> <dd>

O valor de data variante para definir o objeto. Esse parâmetro deve estar no **formato DATE da VT. \_**

</dd> <dt>

*bIsLocal* \[ in, opcional\]
</dt> <dd>

Se **TRUE**, *vdate* será interpretado como uma hora local e a propriedade Tempo Universal Coordenado (UTC) conterá a hora local convertida no deslocamento UTC correto. Quando *bIsLocal* é **FALSE,** *vdate* é convertido diretamente em um valor UTC com um deslocamento de zero (0).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Depois de concluir o **método SetVarDate,** o [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter o código de erro na lista a seguir.

<dl> <dt>

**wbemErrInvalidSyntax** – 2147749921 (0x80041021)
</dt> <dd>

O formato de *vdate* não é válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Após uma chamada bem-sucedida para **SetVarDate**, o valor [**DATETIME**](datetime.md) é interpretado como um valor de datetime absoluto em vez de um intervalo e a [**propriedade IsInterval**](swbemdatetime-isinterval.md) é definida como **FALSE.**

A função Visual Basic ou VBScript [CDate](/previous-versions//2dt118h2(v=vs.85)) fornece um valor [**datetime**](datetime.md) no formato **DATE da VT \_** para entrada **em SetVarDate.**

## <a name="examples"></a>Exemplos

Para ver exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores CIM [**DATETIME**](datetime.md) de e para o formato **FILETIME** ou **VT \_ DATE,** consulte [Tarefas WMI:](wmi-tasks--dates-and-times.md)Datas e Horas . Para uma descrição do formato CIM **DATETIME,** consulte [Formato de data e hora.](date-and-time-format.md)

O exemplo de código VBScript converter data em [Date-Time WMI](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) na Galeria do TechNet usa SetVarDate para converter um valor de data/hora regular no formato de data/hora UTC.

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

[**SWbemDateTime.SetFileTime**](swbemdatetime-setfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

