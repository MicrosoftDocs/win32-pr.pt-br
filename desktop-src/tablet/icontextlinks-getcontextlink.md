---
description: Recupera o IContextLink no índice especificado.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'Método IContextLinks:: GetContextLink (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 01cf3b971b8533f21185a9b6e65c3cfb25109e657e2c9e2a931253d86c51dbdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940306"
---
# <a name="icontextlinksgetcontextlink-method"></a>Método IContextLinks:: GetContextLink

Recupera o [**IContextLink**](icontextlink.md) no índice especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulIndex* \[ no\]
</dt> <dd>

O índice de base zero do objeto [**IContextLink**](icontextlink.md) a ser obtido.

</dd> <dt>

*ppContextLink* \[ fora\]
</dt> <dd>

Um ponteiro para o objeto [**IContextLink**](icontextlink.md) no índice especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextLink* quando você não precisar mais usar o link de contexto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

