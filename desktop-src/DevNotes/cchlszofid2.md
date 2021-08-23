---
description: Decodifica e armazena uma cadeia de caracteres.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: Função CchLszOfId2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: 0377b8507507b40c5b17c3d9bb6861e5077f8c7bb763b51c66289ab1819f9cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815466"
---
# <a name="cchlszofid2-function"></a>Função CchLszOfId2

Decodifica e armazena uma cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*id* 
</dt> <dd>

O identificador da cadeia de caracteres no arquivo de recurso a ser decodificado e armazenado. A validade da cadeia de caracteres não é verificada.

</dd> <dt>

*lsz* 
</dt> <dd>

Um ponteiro para um buffer com um comprimento *de cbmax.* Cadeias de caracteres maiores que *cbmax* são truncadas.

</dd> <dt>

*cbmax* 
</dt> <dd>

O comprimento máximo da cadeia de caracteres a ser armazenada no *parâmetro lsz.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retorna a cadeia de caracteres decodificada.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 
