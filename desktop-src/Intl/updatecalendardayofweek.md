---
description: Preterido. Obtém o dia da semana que corresponde a um dia especificado e popula o membro DayOfWeek na estrutura CALDATETIME especificada com esse valor.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: Função UpdateCalendarDayOfWeek
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 0e7060c03b06fe855c096e94469797dedb20d74ec1d9de43e11b866c3afb0ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560646"
---
# <a name="updatecalendardayofweek-function"></a>Função UpdateCalendarDayOfWeek

Preterido. Obtém o dia da semana que corresponde a um dia especificado e popula o membro **DayOfWeek** na estrutura [**CALDATETIME**](caldatetime.md) especificada com esse valor.

## <a name="syntax"></a>Sintaxe


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpCalDateTime* \[ entrada, saída\]
</dt> <dd>

Ponteiro para a estrutura [**CALDATETIME**](caldatetime.md) que contém a data para a qual definir o dia da semana.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário. Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   \_Data \_ de erro fora \_ do \_ intervalo. A data especificada estava fora do intervalo.
-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

Essa função não tem um arquivo de cabeçalho ou arquivo de biblioteca associado. O aplicativo pode chamar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Kernel32.dll) para obter um identificador de módulo. Em seguida, ele pode chamar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse identificador de módulo e o nome dessa função para obter o endereço da função.

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

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
