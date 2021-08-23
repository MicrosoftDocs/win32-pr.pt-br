---
description: Preterido. Converte uma estrutura CALDATETIME especificada em uma estrutura SYSTEMTIME.
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: Função ConvertCalDateTimeToSystemTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: cb579eb80c421d6f206045889edfe3f1b64130f58d02d96c61b3867abcaabb75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631926"
---
# <a name="convertcaldatetimetosystemtime-function"></a>Função ConvertCalDateTimeToSystemTime

Preterido. Converte uma estrutura [**CALDATETIME especificada**](caldatetime.md) em uma [**estrutura SYSTEMTIME.**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)

## <a name="syntax"></a>Sintaxe


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpCalDateTime* \[ Em\]
</dt> <dd>

Ponteiro para a [**estrutura CALDATETIME**](caldatetime.md) a ser convertida.

</dd> <dt>

*lpSysTime* \[ out\]
</dt> <dd>

Ponteiro para a estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) equivalente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário. Para obter informações de erro estendidas, o aplicativo pode [**chamar GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   DATA \_ DE ERRO FORA DO \_ \_ \_ INTERVALO. A data especificada estava fora do intervalo.
-   ERRO \_ PARÂMETRO \_ INVÁLIDO. Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

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

 

 
