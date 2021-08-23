---
description: Recupera um valor que indica se o confirmtype passado para esse método foi definido neste IContextNode.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'Método IContextNode:: isconfirmed (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2e378aaf344e177514115c82b1179f8d1ebe25faefa0d5d840d5a0af62ff1c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967355"
---
# <a name="icontextnodeisconfirmed-method"></a>Método IContextNode:: isconfirmed

Recupera um valor que indica se o confirmtype passado para esse método foi definido neste IContextNode.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*confirmable* \[ no\]
</dt> <dd>

O tipo de confirmação que está sendo testado para.

</dd> <dt>

*pfTypeConfirmed* \[ fora\]
</dt> <dd>

**Variante \_ TRUE** se o tipo transmitido em confirmated tiver sido definido neste objeto [**IContextNode**](icontextnode.md) ; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Esse valor é definido pelo método [**IContextNode:: Confirm**](icontextnode-confirm.md) .

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
</dt> <dt>

[**IContextNode:: confirmar**](icontextnode-confirm.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




