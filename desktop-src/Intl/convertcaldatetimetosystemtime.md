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
ms.openlocfilehash: 9c317a31904e2d1b0b2110f6b2dc367ac3e2e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813083"
---
# <a name="convertcaldatetimetosystemtime-function"></a>Função ConvertCalDateTimeToSystemTime

Preterido. Converte uma estrutura [**CALDATETIME**](caldatetime.md) especificada em uma estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .

## <a name="syntax"></a>Sintaxe


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpCalDateTime* \[ no\]
</dt> <dd>

Ponteiro para a estrutura [**CALDATETIME**](caldatetime.md) a ser convertida.

</dd> <dt>

*lpSysTime* \[ fora\]
</dt> <dd>

Ponteiro para a estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) equivalente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido ou **false** caso contrário. Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   \_Data \_ de erro fora \_ do \_ intervalo. A data especificada estava fora do intervalo.
-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

Essa função não tem um arquivo de cabeçalho ou arquivo de biblioteca associado. O aplicativo pode chamar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Kernel32.dll) para obter um identificador de módulo. Em seguida, ele pode chamar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com a alça do módulo e o nome dessa função para obter o endereço da função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao idioma nacional](national-language-support.md)
</dt> <dt>

[Funções de suporte ao idioma nacional](national-language-support-functions.md)
</dt> <dt>

[Recuperando informações de data e hora](time-and-date.md)
</dt> </dl>

 

 
