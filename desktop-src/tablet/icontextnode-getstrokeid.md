---
description: Recupera o identificador de traço para o traço referenciado por um valor de índice dentro do objeto IContextNode.
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: 'Método IContextNode:: getstrokeid (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b193b3719ac6b67284e3ff8c4297455888f6c9cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647235"
---
# <a name="icontextnodegetstrokeid-method"></a>Método IContextNode:: getstrokeid

Recupera o identificador de traço para o traço referenciado por um valor de índice dentro do objeto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulIndex* \[ no\]
</dt> <dd>

O índice do traço a ser retornado.

</dd> <dt>

*plStrokeId* \[ fora\]
</dt> <dd>

O identificador de traço para o traço referenciado pelo parâmetro *ulIndex* no objeto [**IContextNode**](icontextnode.md) atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

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
</dt> <dt>

[**IContextNode::GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[**IContextNode::GetStrokeCount**](icontextnode-getstrokecount.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




