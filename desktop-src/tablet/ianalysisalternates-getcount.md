---
description: Recupera o número de objetos IAnalysisAlternate contidos na coleção IAnalysisAlternates.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: 'Método IAnalysisAlternates:: GetCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84ff5941d4db6ca569c8a7a10a622e4b3dcdfc947284064fa009e030adae1493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967485"
---
# <a name="ianalysisalternatesgetcount-method"></a>Método IAnalysisAlternates:: GetCount

Recupera o número de objetos [**IAnalysisAlternate**](ianalysisalternate.md) contidos na coleção [**IAnalysisAlternates**](ianalysisalternates.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulCount* \[ fora\]
</dt> <dd>

Um inteiro de 32 bits não assinado que é definido como o número de objetos [**IAnalysisAlternate**](ianalysisalternate.md) contidos na coleção [**IAnalysisAlternates**](ianalysisalternates.md) .

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

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




