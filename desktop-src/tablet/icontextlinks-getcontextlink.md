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
ms.openlocfilehash: ecc0ed9ba457a7a91cb2e1b615ac7419ce5a94c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090551"
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

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextLink* quando você não precisar mais usar o link de contexto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

