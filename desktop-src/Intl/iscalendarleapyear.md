---
description: Preterido. Identifica se o ano especificado é um ano bissexão dentro da era determinada para o calendário específico.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: Função IsCalendarLeapYear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: fe89f11bbaf41235449e882626680cf4d4af075d93f76c2d2aacd90d8d38707a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948714"
---
# <a name="iscalendarleapyear-function"></a>Função IsCalendarLeapYear

Preterido. Identifica se o ano especificado é um ano bissexão dentro da era determinada para o calendário específico.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*calId* \[ Em\]
</dt> <dd>

O [identificador de calendário a](calendar-identifiers.md) ser usado para verificar o ano bissexo.

</dd> <dt>

*ano* \[ Em\]
</dt> <dd>

O ano a ser verificar.

</dd> <dt>

*era* \[ Em\]
</dt> <dd>

A era a ser verificada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se o ano especificado for um ano bissexco ou **FALSE** caso contrário. Para obter informações de erro estendidas, o aplicativo pode [**chamar GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   ERRO \_ PARÂMETRO \_ INVÁLIDO. Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

Essa função não tem um arquivo de header ou arquivo de biblioteca associado. O aplicativo pode chamar [**LoadLibrary com**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o nome da DLL (Kernel32.dll) para obter um handle de módulo. Em seguida, ele [**pode chamar GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse alçamento de módulo e o nome dessa função para obter o endereço da função.

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
</dt> </dl>

 

 
