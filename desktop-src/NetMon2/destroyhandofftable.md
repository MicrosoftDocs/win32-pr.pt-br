---
description: A função DestroyHandoffTable destrói uma tabela de entrega criada com createentregatable.
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: Função DestroyHandoffTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7afccfd1932c57b2a0d77dbb5467afc31726c6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921629"
---
# <a name="destroyhandofftable-function"></a>Função DestroyHandoffTable

A função **DestroyHandoffTable** destrói uma tabela de entrega criada com **createentregatable**.

## <a name="syntax"></a>Sintaxe


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hTable* \[ no\]
</dt> <dd>

Identificador para a tabela de entrega destruída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




