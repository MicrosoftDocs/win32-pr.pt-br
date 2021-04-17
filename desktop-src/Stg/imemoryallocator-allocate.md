---
title: Método IMemoryAllocator Allocate
description: O método Allocate aloca memória para a função StgConvertPropertyToVariant quando a função converte um tipo de dados SERIALIZEDPROPERTYVALUE para um tipo de dados PROPVARIANT.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Alocar o armazenamento estruturado do método
- Alocar o armazenamento estruturado do método, interface IMemoryAllocator
- Armazenamento estruturado da interface IMemoryAllocator, método Allocate
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755779"
---
# <a name="imemoryallocatorallocate-method"></a>Método IMemoryAllocator:: Allocate

O método **ALLOCATE aloca** memória para a função [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) quando a função converte um tipo de dados **SERIALIZEDPROPERTYVALUE** para um tipo de dados **PROPVARIANT** .

## <a name="syntax"></a>Sintaxe


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cbSize* \[ no\]
</dt> <dd>

Especifica o tamanho da memória a ser alocada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

