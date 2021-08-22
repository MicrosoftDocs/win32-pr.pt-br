---
description: Indica se a cadeia de caracteres reconhecida especificada veio do dicionário do sistema, dicionário de usuário ou lista de palavras.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: Método IContextNode::IsAlternateStringSupported (IACom.h)
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
ms.openlocfilehash: cbf18c63ce81a439092ba3bdabfae38c5f52882ec5364ef5c8fbd67cab5d81a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119266296"
---
# <a name="icontextnodeisalternatestringsupported-method"></a>Método IContextNode::IsAlternateStringSupported

Indica se a cadeia de caracteres reconhecida especificada veio do dicionário do sistema, dicionário de usuário ou lista de palavras. Qualquer restrição de dados, como listas de palavras, guias ou factoids, em qualquer nó de dica correspondente será usado para determinar se há suporte para a cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrAlternateString* \[ Em\]
</dt> <dd>

Cadeia de caracteres reconhecida para verificar.

</dd> <dt>

*pfIsSupported* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** se a cadeia de caracteres especificada for suportada pelo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) com todos os nós de dica correspondentes aplicados; **VARIANT \_ FALSE** se não tiver suporte.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> </dl>

 

 




