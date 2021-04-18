---
description: Preterido.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: Função GetCalendarDateFormatEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarDateFormatEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: b0130bf62c742d0565b1c98c138ac8c71ddf7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810337"
---
# <a name="getcalendardateformatex-function"></a>Função GetCalendarDateFormatEx

Preterido. Recupera uma cadeia de caracteres de data formatada corretamente para a localidade especificada usando a data e o calendário especificados. O usuário pode especificar o formato de data abreviada, o formato de data por extenso, o formato de mês de ano ou um padrão de formato personalizado.

> [!Note]  
> Essa função pode recuperar dados que são alterados entre as versões, por exemplo, devido a uma localidade personalizada. Se seu aplicativo precisar manter ou transmitir dados, consulte [usando dados de localidade persistente](using-persistent-locale-data.md).

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetCalendarDateFormatEx(
  _In_        LPCWSTR       lpszLocale,
  _In_        DWORD         dwFlags,
  _In_  const LPCALDATETIME lpCalDateTime,
  _In_        LPCWSTR       lpFormat,
  _Out_       LPWSTR        lpDateStr,
  _In_        int           cchDate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszLocale* \[ no\]
</dt> <dd>

Ponteiro para um nome de localidade ou um dos valores predefinidos a seguir.

-   [nome da localidade \_ \_ invariável](locale-name-constants.md)
-   [nome da localidade \_ \_ padrão do sistema \_](locale-name-constants.md)
-   [nome da localidade \_ \_ usuário \_ padrão](locale-name-constants.md)

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Sinalizadores que especificam opções de formato de data. Se *lpFormat* não estiver definido como **NULL**, esse parâmetro deverá ser definido como 0. Se *lpFormat* for definido como **NULL**, o aplicativo poderá especificar uma combinação dos seguintes valores e [ \_ NOUSEROVERRIDE de localidade](locale-nouseroverride.md).



| Valor                                                                                                                                                               | Significado                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <dt>**Data de \_ SHORTDATE**</dt> </dl>    | Use o formato de data abreviada. Esse é o padrão. Esse valor não pode ser usado com a data \_ LONGDATE ou a data \_ YEARMONTH. <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <dt>**Data de \_ LONGDATE**</dt> </dl>       | Use o formato de data por extenso. Esse valor não pode ser usado com a data \_ SHORTDATE ou a data \_ YEARMONTH. <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <dt>**Data de \_ YEARMONTH**</dt> </dl>    | Use o formato de ano/mês. Esse valor não pode ser usado com a data \_ SHORTDATE ou a data \_ LONGDATE.<br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <dt>**Data de \_ LTRREADING**</dt> </dl> | Adicionar marcas para layout de leitura da esquerda para a direita. Esse valor não pode ser usado com a data \_ RTLREADING.<br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <dt>**Data de \_ RTLREADING**</dt> </dl> | Adicionar marcas para layout de leitura da direita para a esquerda. Este valor não pode ser usado com a data \_ LTRREADING<br/>                        |



 

</dd> <dt>

*lpCalDateTime* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura [**CALDATETIME**](caldatetime.md) que contém as informações de data e calendário a serem formatadas.

</dd> <dt>

*lpFormat* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres de imagem de formato que é usada para formar a cadeia de caracteres de data. Os valores possíveis para a cadeia de caracteres de imagem de formato são definidos nas [imagens de formato dia, mês, ano e era](day--month--year--and-era-format-pictures.md).

A cadeia de caracteres de imagem de formato deve ser terminada em nulo. A função usa a localidade somente para informações não especificadas na cadeia de caracteres de imagem de formato, por exemplo, os nomes de dia e mês para a localidade. O aplicativo definirá esse parâmetro como **NULL** se a função for usar o formato de data da localidade especificada.

</dd> <dt>

*lpDateStr* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual essa função recebe a cadeia de caracteres de data formatada.

</dd> <dt>

*cchDate* \[ no\]
</dt> <dd>

Tamanho, em caracteres, do buffer *lpDateStr* . Como alternativa, o aplicativo pode definir esse parâmetro como 0. Nesse caso, a função retorna o número de caracteres necessários para manter a cadeia de caracteres de data formatada e o parâmetro *lpDateStr* não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de caracteres gravados no buffer *lpDateStr* se for bem-sucedido. Se o parâmetro *cchDate* for definido como 0, a função retornará o número de caracteres necessários para manter a cadeia de caracteres de data formatada, incluindo o caractere nulo de terminação.

Essa função retornará 0 se não tiver sucesso. Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   \_Data \_ de erro fora \_ do \_ intervalo. A data especificada estava fora do intervalo.
-   ERRO \_ de \_ buffer insuficiente. Um tamanho de buffer fornecido não era grande o suficiente ou foi definido incorretamente como **nulo**.
-   ERROS de \_ Sinalizadores inválidos \_ . Os valores fornecidos para sinalizadores não eram válidos.
-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

A data mais antiga com suporte nesta função é 1º de janeiro de 1601.

Essa função não tem um arquivo de cabeçalho ou arquivo de biblioteca associado. O aplicativo pode chamar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Kernel32.dll) para obter um identificador de módulo. Em seguida, ele pode chamar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse identificador de módulo e o nome dessa função para obter o endereço da função.

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

[Imagens de formato de dia, mês, ano e era](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[NLS: exemplo de APIs baseadas em nome](nls--name-based-apis-sample.md)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
