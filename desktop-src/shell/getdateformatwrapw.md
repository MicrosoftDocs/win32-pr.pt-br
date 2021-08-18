---
description: Formata uma data como uma cadeia de caracteres de data para uma localidade especificada.
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: Função GetDateFormatWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDateFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 9a45222c316d321ee151c19464d453827437514dd93ffe3da5b1a9849e8a7196
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119395876"
---
# <a name="getdateformatwrapw-function"></a>Função GetDateFormatWrapW

\[o **GetDateFormatWrapW** está disponível para uso no Windows XP. Ele não estará disponível nas versões subsequentes. Você deve usar [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) em seu lugar.\]

Formata uma data como uma cadeia de caracteres de data para uma localidade especificada. A função formata uma data especificada ou a data do sistema local.

> [!Note]  
> **GetDateFormatWrapW** é um wrapper para a função **GetDateFormatW** . Consulte a página [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) para ver mais observações de uso.

 

## <a name="syntax"></a>Sintaxe


```C++
int GetDateFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpDate,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzDateStr,
  _In_        int        cchDate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localidade* \[ do no\]
</dt> <dd>

Tipo: **LCID**

A localidade para a qual a cadeia de caracteres de data deve ser formatada. Se *pwzFormat* for **NULL**, a função formatará a cadeia de caracteres de acordo com o formato de data dessa localidade. Se *pwzFormat* não for **NULL**, a função usará a localidade somente para informações não especificadas na cadeia de caracteres de imagem de formato (por exemplo, os nomes de dia e mês da localidade).

Esse parâmetro pode ser um identificador de localidade criado pela macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) ou um dos valores predefinidos a seguir.

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**\_padrão do sistema de localidade \_**


</dt> <dd>

Localidade do sistema padrão.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_padrão de usuário de localidade \_**


</dt> <dd>

Localidade do usuário padrão.

</dd> </dl> </dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Especifica várias opções de função. Se *pwzFormat* não for **NULL**, esse parâmetro deverá ser zero. Se *pwzFormat* for **nulo**, você poderá especificar uma combinação dos valores a seguir. Se você não especificar a data \_ YEARMONTH, a data \_ SHORTDATE ou a data \_ LONGDATE e *pwzFormat* for **NULL**, \_ a data SHORTDATE será usada como padrão.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**NOUSEROVERRIDE de localidade \_**


</dt> <dd>

Se definido, a função formata a cadeia de caracteres usando o formato de data padrão do sistema para a localidade especificada. Se não for definido, a função formatará a cadeia de caracteres usando qualquer substituição de usuário para o formato de data padrão da localidade.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALIDADE \_ use \_ CP \_ ACP**


</dt> <dd>

Usa a página de código ANSI do sistema para conversão de cadeia de caracteres em vez da página de código da localidade.

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**Data de \_ SHORTDATE**


</dt> <dd>

Usa o formato de data abreviada. Esse valor não pode ser usado com a data \_ LONGDATE ou a data \_ YEARMONTH.

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**Data de \_ LONGDATE**


</dt> <dd>

Usa o formato de data por extenso. Esse valor não pode ser usado com a data \_ SHORTDATE ou a data \_ YEARMONTH.

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**Data de \_ YEARMONTH**


</dt> <dd>

Usa o formato de ano/mês. Esse valor não pode ser usado com a data \_ SHORTDATE ou a data \_ LONGDATE.

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**\_ \_ calendário Alt de uso de data \_**


</dt> <dd>

Usa o calendário alternativo, se houver, para formatar a cadeia de caracteres de data. Se esse sinalizador for definido, a função usará o formato padrão para esse calendário alternativo, em vez de usar qualquer substituição de usuário. As substituições de usuário serão usadas somente no caso de não haver nenhum formato padrão para o calendário alternativo especificado.

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**Data de \_ LTRREADING**


</dt> <dd>

Adiciona marcas para layout de leitura da esquerda para a direita. Esse valor não pode ser usado com a data \_ RTLREADING.

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**Data de \_ RTLREADING**


</dt> <dd>

Adiciona marcas para layout de leitura da direita para a esquerda. Esse valor não pode ser usado com a data \_ LTRREADING.

</dd> </dl> </dd> <dt>

*lpDate* \[ no\]
</dt> <dd>

Tipo: **const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \***

Um ponteiro para uma estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contém as informações de data a serem formatadas. Se esse ponteiro for **nulo**, a função usará a data atual do sistema local.

</dd> <dt>

*pwzFormat* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para uma imagem de formato a ser usada para formar a cadeia de caracteres de data. Se *pwzFormat* for **NULL**, a função usará o formato de data da localidade especificada. Consulte [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) para obter mais detalhes.

</dd> <dt>

*pwzDateStr* \[ fora\]
</dt> <dd>

Tipo: **LPWSTR**

Um ponteiro para um buffer que recebe a cadeia de caracteres de data formatada.

</dd> <dt>

*cchDate* \[ no\]
</dt> <dd>

Tipo: **int**

Especifica o tamanho, em caracteres, do buffer *pwzDateStr* . Se *cchDate* for zero, a função retornará o número de caracteres necessários para manter a cadeia de caracteres de data formatada e o buffer apontado por *pwzDateStr* não será usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **int**

Se a função for realizada com sucesso, o valor de retorno será o número de caracteres gravados no buffer apontado por *pwzDateStr*. Se o parâmetro *cchDate* for zero, o valor de retorno será o número de caracteres necessários para manter a cadeia de caracteres de data formatada. A contagem inclui o caractere nulo de terminação.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** pode retornar um dos seguintes códigos de erro.

<dl> <dt>

**ERRO \_ de \_ buffer insuficiente**
</dt> <dt>

**\_Sinalizadores inválidos de erro \_**
</dt> <dt>

**\_parâmetro inválido de erro \_**
</dt> </dl>

## <a name="remarks"></a>Comentários

o **GetDateFormatWrapW** fornece a capacidade de usar cadeias de caracteres Unicode em sistemas operacionais anteriores ao Windows XP. O método preferencial é usar [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) em conjunto com a camada Microsoft para Unicode (MSLU).

**GetDateFormatWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 311.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
