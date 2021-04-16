---
description: Recupera o nome do reconhecedor.
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: 'Método IInkAnalysisRecognizer:: GetName (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fe263878d1fd5e914cf033111997d297a20c54f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750401"
---
# <a name="iinkanalysisrecognizergetname-method"></a>Método IInkAnalysisRecognizer:: GetName

Recupera o nome do reconhecedor.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbstrName* \[ fora\]
</dt> <dd>

O nome do reconhecedor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) no \* *pbstrName* quando você não precisar mais usar a cadeia de caracteres.

 

O nome é localizado para a linguagem neutra de região para a qual o reconhecedor dá suporte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

