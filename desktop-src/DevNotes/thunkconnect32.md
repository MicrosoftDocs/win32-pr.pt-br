---
description: A função ThunkConnect32 é usada por drivers de dispositivo de 16 bits (para MS-DOS) que chamam o kernel de 32 bits.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: Função ThunkConnect32
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747903"
---
# <a name="thunkconnect32-function"></a>Função ThunkConnect32

\[Essa função foi suportada para compatibilidade com versões anteriores, mas não está presente nas versões atuais do Windows. Os novos drivers de dispositivo devem ser 32 ou 64 bits e não precisam dessa função.\]

A função **ThunkConnect32** é usada por drivers de dispositivo de 16 bits (para MS-dos) que chamam o kernel de 32 bits.

## <a name="syntax"></a>Sintaxe


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpThunkData32* 
</dt> <dd>

Ignorado.

</dd> <dt>

*pszThunkData16Name* 
</dt> <dd>

Ignorado.

</dd> <dt>

*pszDll16* 
</dt> <dd>

Ignorado.

</dd> <dt>

*pszDll32* 
</dt> <dd>

Ignorado.

</dd> <dt>

*hInstance* 
</dt> <dd>

Ignorado.

</dd> <dt>

*dwReason* 
</dt> <dd>

Ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sempre retorna **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




