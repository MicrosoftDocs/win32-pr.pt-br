---
description: Recupera um nome de tipo legível por humanos deste IContextNode.
ms.assetid: 02031efd-1e9c-4e96-8dc1-280cc1a6e58f
title: 'Método IContextNode:: getTypeName (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetTypeName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9d7bc4a24b7abc3ee507d7bda0c547f4c55a787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090542"
---
# <a name="icontextnodegettypename-method"></a>Método IContextNode:: getTypeName

Recupera um nome de tipo legível por humanos deste [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTypeName(
  [out] BSTR *pbstrContextNodeType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbstrContextNodeType* \[ fora\]
</dt> <dd>

Um nome de tipo legível por humanos deste [**IContextNode**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) no \* *pbstrContextNodeType* quando você não precisar mais usar a cadeia de caracteres.

 

Por exemplo, esse método define *pbstrContextNodeType* como "InkWordNode" para um nó de palavra à tinta (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [tipos de nó de contexto](context-node-types.md)).

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

[**IContextNode:: GetType**](icontextnode-gettype.md)
</dt> <dt>

[Tipos de nó de contexto](context-node-types.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

