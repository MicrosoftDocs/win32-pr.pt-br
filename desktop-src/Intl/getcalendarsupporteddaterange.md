---
description: Preterido. Obtém o intervalo de datas com suporte para um calendário especificado.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: Função GetCalendarSupportedDateRange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: cf665b2591702b1b833cccb392c7345c1d76d44d324fabc214192c012c60f785
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765446"
---
# <a name="getcalendarsupporteddaterange-function"></a>Função GetCalendarSupportedDateRange

Preterido. Obtém o intervalo de datas com suporte para um calendário especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Calendário* \[ do no\]
</dt> <dd>

[Identificador de calendário](calendar-identifiers.md) para o qual obter o intervalo de datas com suporte.

</dd> <dt>

*lpCalMinDateTime* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura [**CALDATETIME**](caldatetime.md) que define a data mínima com suporte.

</dd> <dt>

*lpCalMaxDateTime* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura [**CALDATETIME**](caldatetime.md) que define a data máxima com suporte.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário. Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

A data mais antiga com suporte nesta função é 1º de janeiro de 1601.

Essa função não tem um arquivo de cabeçalho ou arquivo de biblioteca associado. O aplicativo pode chamar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Kernel32.dll) para obter um identificador de módulo. Em seguida, ele pode chamar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com a alça do módulo e o nome dessa função para obter o endereço da função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao idioma nacional](national-language-support.md)
</dt> <dt>

[Funções de suporte ao idioma nacional](national-language-support-functions.md)
</dt> <dt>

[NLS: exemplo de APIs baseadas em nome](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
