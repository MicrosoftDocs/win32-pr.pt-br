---
description: Preterido. Converte uma estrutura SYSTEMTIME especificada em uma estrutura CALDATETIME.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: Função ConvertSystemTimeToCalDateTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 01eb78f9045e43db3e97b252a8fdf8fe8ed7297905174efeff2f3b2bbe1a5171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746036"
---
# <a name="convertsystemtimetocaldatetime-function"></a>Função ConvertSystemTimeToCalDateTime

Preterido. Converte uma estrutura [**SYSTEMTIME especificada**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) em uma [**estrutura CALDATETIME.**](caldatetime.md)

## <a name="syntax"></a>Sintaxe


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpSysTime* \[ Em\]
</dt> <dd>

Ponteiro para a [**estrutura SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) a ser convertida.

</dd> <dt>

*calId* \[ Em\]
</dt> <dd>

O [identificador de calendário do sistema](calendar-identifiers.md) a ser usado na conversão.

</dd> <dt>

*lpCalDateTime* \[ out\]
</dt> <dd>

Ponteiro para a estrutura [**CALDATETIME**](caldatetime.md) equivalente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário. Para obter informações de erro estendidas, o aplicativo pode [**chamar GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   ERRO \_ PARÂMETRO \_ INVÁLIDO. Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

A data mais antiga com suporte por essa função é 1º de janeiro de 1601.

Essa função não tem um arquivo de header ou arquivo de biblioteca associado. O aplicativo pode chamar [**LoadLibrary com**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o nome da DLL (Kernel32.dll) para obter um handle de módulo. Em seguida, ele [**pode chamar GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com o alça do módulo e o nome dessa função para obter o endereço da função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte a idiomas nacionais](national-language-support.md)
</dt> <dt>

[Funções de suporte a idiomas nacionais](national-language-support-functions.md)
</dt> <dt>

[Recuperando informações de data e hora](time-and-date.md)
</dt> </dl>

 

 
