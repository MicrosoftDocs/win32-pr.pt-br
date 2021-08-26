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
ms.openlocfilehash: 3f754d4c0e88ee860d112a6fb99d15c2690af0014951e77425d425b65ad16e39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929106"
---
# <a name="thunkconnect32-function"></a>Função ThunkConnect32

\[Essa função era compatível com compatibilidade com versões anteriores, mas não está presente nas versões atuais do Windows. Novos drivers de dispositivo devem ser de 32 ou 64 bits e não precisam dessa função.\]

A **função ThunkConnect32** é usada por drivers de dispositivo de 16 bits (para MS-DOS) que chamam o kernel de 32 bits.

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

*Dwreason* 
</dt> <dd>

Ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sempre retorna **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




