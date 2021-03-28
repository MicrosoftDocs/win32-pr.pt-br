---
description: Formata o tempo como uma cadeia de hora para uma localidade especificada.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: Função GetTimeFormatWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 53f1bb88c2b3a79b58f3025daec31a7b1340b642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967924"
---
# <a name="gettimeformatwrapw-function"></a>Função GetTimeFormatWrapW

\[O **GetTimeFormatWrapW** está disponível para uso no Windows XP. Ele pode não estar disponível em versões subsequentes. Você deve usar [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) em seu lugar.\]

Formata o tempo como uma cadeia de hora para uma localidade especificada. A função formata uma hora especificada ou a hora do sistema local.

> [!Note]  
> **GetTimeFormatWrapW** é um wrapper para a função **GetTimeFormatW** . Consulte a página [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) para ver mais observações de uso.

 

## <a name="syntax"></a>Sintaxe


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localidade* \[ do no\]
</dt> <dd>

Tipo: **LCID**

Especifica a localidade para a qual a cadeia de caracteres de tempo deve ser formatada. Se *pwzFormat* for **NULL**, a função formatará a cadeia de caracteres de acordo com o formato de hora dessa localidade. Se *pwzFormat* não for **NULL**, a função usará a localidade somente para informações não especificadas na cadeia de caracteres de imagem de formato (por exemplo, os marcadores de tempo da localidade).

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

Especifica várias opções de função. Você pode especificar uma combinação dos valores a seguir.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**NOUSEROVERRIDE de localidade \_**


</dt> <dd>

Se definido, a função formata a cadeia de caracteres usando o formato de hora padrão do sistema para a localidade especificada. Se não for definido, a função formatará a cadeia de caracteres usando qualquer substituição de usuário para o formato de hora padrão da localidade. Esse sinalizador só poderá ser definido se *pwzFormat* for **nulo**.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALIDADE \_ use \_ CP \_ ACP**


</dt> <dd>

Usa a página de código ANSI do sistema para conversão de cadeia de caracteres em vez da página de código de localidade.

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**NOMINUTESORSECONDS de tempo \_**


</dt> <dd>

Não usa minutos ou segundos.

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TEMPO em \_ segundos**


</dt> <dd>

Não usa segundos.

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**NOTIMEMARKER de tempo \_**


</dt> <dd>

Não usa um marcador de tempo.

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**FORCE24HOURFORMAT de tempo \_**


</dt> <dd>

Sempre usa um formato de 24 horas.

</dd> </dl> </dd> <dt>

*lpTime* \[ no\]
</dt> <dd>

Tipo: **const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _

Um ponteiro para uma estrutura [_ *SYSTEMTIME* *](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contém as informações de hora a serem formatadas. Se esse ponteiro for **nulo**, a função usará a hora atual do sistema local.

</dd> <dt>

*pwzFormat* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para um formato a ser usado para formar a cadeia de caracteres de tempo. Se *pwzFormat* for **NULL**, a função usará o formato de hora da localidade especificada. Consulte [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) para obter mais detalhes.

</dd> <dt>

*pwzTimeStr* \[ fora\]
</dt> <dd>

Tipo: **LPWSTR**

Um ponteiro para um buffer que recebe a cadeia de caracteres de hora formatada.

</dd> <dt>

*cchTime* \[ no\]
</dt> <dd>

Tipo: **int**

O tamanho, em caracteres, do buffer *pwzTimeStr* . Se *cchTime* for zero, a função retornará o número de caracteres necessários para manter a cadeia de caracteres de tempo formatada e o buffer apontado por *pwzTimeStr* não será usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **int**

Se a função for realizada com sucesso, o valor de retorno será o número de caracteres gravados no buffer apontado por *pwzTimeStr*. Se o parâmetro *cchTime* for zero, o valor de retorno será o número de caracteres necessários para manter a cadeia de caracteres de tempo formatada. A contagem inclui o caractere nulo de terminação.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** pode retornar um dos seguintes códigos de erro.

<dl> <dt>

**ERRO \_ de \_ buffer insuficiente**
</dt> <dt>

**\_Sinalizadores inválidos de erro \_**
</dt> <dt>

**\_parâmetro inválido de erro \_**
</dt> </dl>

## <a name="remarks"></a>Comentários

O **GetTimeFormatWrapW** fornece a capacidade de usar cadeias de caracteres Unicode em sistemas operacionais anteriores ao Windows XP. O método preferencial é usar [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) em conjunto com a camada Microsoft para Unicode (MSLU).

**GetTimeFormatWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 310.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
