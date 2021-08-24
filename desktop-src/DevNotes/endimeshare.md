---
description: Encerra o compartilhamento do IME.
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: Função EndIMEShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 079a8719aa8e48e8ae880f2ce2a83d5e4d0f89fda85298ec015a3f77acebeb9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653436"
---
# <a name="endimeshare-function"></a>Função EndIMEShare

Encerra o compartilhamento do IME.

## <a name="syntax"></a>Sintaxe


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

Essa função deve ser chamada depois que a última função de compartilhamento do IME for chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FInitIMEShare**](finitimeshare.md)
</dt> </dl>

 

 
