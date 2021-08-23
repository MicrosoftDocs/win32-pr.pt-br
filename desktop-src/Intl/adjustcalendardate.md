---
description: Preterido. Ajusta uma data por um número especificado de anos, meses, semanas ou dias.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: Função AdjustCalendarDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 061d0e246f7839345b0f1e55221d26d276f52af4997a7cb47d62b680d2638fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520616"
---
# <a name="adjustcalendardate-function"></a>Função AdjustCalendarDate

Preterido. Ajusta uma data por um número especificado de anos, meses, semanas ou dias.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpCalDateTime* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma estrutura [**CALDATETIME**](caldatetime.md) que contém as informações de data e calendário a serem ajustadas.

</dd> <dt>

*calUnit* \[ no\]
</dt> <dd>

O valor de enumeração [**CALDATETIME \_ DATEUNIT**](caldatetime-dateunit.md) que indica a unidade de data, por exemplo, DayUnit.

</dd> <dt>

*valor* \[ fora\]
</dt> <dd>

O valor pelo qual ajustar a data especificada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário. Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   \_Data \_ de erro fora \_ do \_ intervalo. A data especificada estava fora do intervalo.
-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

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

 

 
