---
description: Indica se a cadeia de caracteres reconhecida deste IContextNode veio do dicionário do sistema, do dicionário do usuário ou da lista de palavras.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'Método IContextNode:: IsStringSupported (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2eef383f059897665c013e3575d452564295ccd9bd014ae8084fd1635892bd99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709106"
---
# <a name="icontextnodeisstringsupported-method"></a>Método IContextNode:: IsStringSupported

Indica se a cadeia de caracteres reconhecida deste [**IContextNode**](icontextnode.md) veio do dicionário do sistema, do dicionário do usuário ou da lista de palavras.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pfIsSupported* \[ out, retval\]
</dt> <dd>

**Variante \_ TRUE** se o valor de cadeia de caracteres reconhecido desse [**IContextNode**](icontextnode.md) for suportado pelo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) com quaisquer nós de dica correspondentes aplicados; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> </dl>

 

 




