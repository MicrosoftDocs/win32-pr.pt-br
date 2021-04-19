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
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747628"
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

Um ponteiro para um buffer com um comprimento de *cbMax*. Cadeias de caracteres maiores que *cbMax* são truncadas.

</dd> <dt>

*cbmax* 
</dt> <dd>

O comprimento máximo da cadeia de caracteres a ser armazenada no parâmetro *LSZ* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retorna a cadeia de caracteres decodificada.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 
