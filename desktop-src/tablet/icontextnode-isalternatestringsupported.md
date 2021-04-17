---
description: Indica se a cadeia de caracteres reconhecida especificada veio do dicionário do sistema, do dicionário do usuário ou da lista de palavras.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'Método IContextNode:: IsAlternateStringSupported (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783215"
---
# <a name="icontextnodeisalternatestringsupported-method"></a>Método IContextNode:: IsAlternateStringSupported

Indica se a cadeia de caracteres reconhecida especificada veio do dicionário do sistema, do dicionário do usuário ou da lista de palavras. Qualquer dado de restrição, como listas de palavras, guias ou factores, em qualquer nó de dica correspondente será usado para determinar se há suporte para a cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrAlternateString* \[ no\]
</dt> <dd>

Cadeia de caracteres reconhecida para verificar.

</dd> <dt>

*pfIsSupported* \[ fora\]
</dt> <dd>

**Variante \_ TRUE** se a cadeia de caracteres especificada for suportada pelo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) com quaisquer nós de dica correspondentes aplicados; **Variante \_ FALSE** se não houver suporte.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> </dl>

 

 




