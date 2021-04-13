---
title: Classe IMemoryAllocator
description: Implementado pelo alocador de memória para a função StgConvertPropertyToVariant.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Armazenamento estruturado da classe IMemoryAllocator
- Armazenamento estruturado da classe IMemoryAllocator, descrito
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369669"
---
# <a name="imemoryallocator-class"></a>Classe IMemoryAllocator

A classe **IMemoryAllocator** é implementada pelo alocador de memória para a função [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .

## <a name="methods"></a>Métodos



| Nome                                                     | Descrição                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aloca**](imemoryallocator-allocate.md)<br/> | Aloca memória para a função [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) quando a função converte um tipo de dados **SERIALIZEDPROPERTYVALUE** para um tipo de dados **PROPVARIANT** .<br/> |
| [**Gratuita**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | Libera a memória alocada pelo método [**ALLOCATE**](imemoryallocator-allocate.md) .<br/>                                                                                                                 |



 

## <a name="remarks"></a>Comentários

Essa classe é usada somente pela função [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

