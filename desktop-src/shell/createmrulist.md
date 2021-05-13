---
description: Cria uma nova lista MRU (usada mais recentemente).
title: Função CreateMRUListW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843377"
---
# <a name="createmrulistw-function"></a>Função CreateMRUListW

Cria uma nova lista MRU (usada mais recentemente).

## <a name="syntax"></a>Sintaxe


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpmi* \[ no\]
</dt> <dd>

Tipo: **LPMRUINFO**

Um ponteiro para uma estrutura [**MRUINFO**](mruinfo.md) que define a lista MRU.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **int**

Retorna um identificador para a nova lista MRU ou 0 em caso de erro.

## <a name="remarks"></a>Comentários

Essa função não está incluída em um cabeçalho ou biblioteca pública. Ele pode ser acessado por meio de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extraído de comctl32.dll por seu ordinal, que é 400 para **CreateMRUListW**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 5,0 ou posterior)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **CreateMRUListW** (Unicode)<br/>                                                                        |



 

 
