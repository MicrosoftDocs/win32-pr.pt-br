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
# <a name="getcalendardateformatex-function"></a><span data-ttu-id="0fd73-103">Função GetCalendarDateFormatEx</span><span class="sxs-lookup"><span data-stu-id="0fd73-103">GetCalendarDateFormatEx function</span></span>

<span data-ttu-id="0fd73-104">Preterido.</span><span class="sxs-lookup"><span data-stu-id="0fd73-104">Deprecated.</span></span> <span data-ttu-id="0fd73-105">Recupera uma cadeia de caracteres de data formatada corretamente para a localidade especificada usando a data e o calendário especificados.</span><span class="sxs-lookup"><span data-stu-id="0fd73-105">Retrieves a properly formatted date string for the specified locale using the specified date and calendar.</span></span> <span data-ttu-id="0fd73-106">O usuário pode especificar o formato de data abreviada, o formato de data por extenso, o formato de mês de ano ou um padrão de formato personalizado.</span><span class="sxs-lookup"><span data-stu-id="0fd73-106">The user can specify the short date format, the long date format, the year month format, or a custom format pattern.</span></span>

> [!Note]  
> <span data-ttu-id="0fd73-107">Essa função pode recuperar dados que são alterados entre as versões, por exemplo, devido a uma localidade personalizada.</span><span class="sxs-lookup"><span data-stu-id="0fd73-107">This function can retrieve data that changes between releases, for example, due to a custom locale.</span></span> <span data-ttu-id="0fd73-108">Se seu aplicativo precisar manter ou transmitir dados, consulte [usando dados de localidade persistente](using-persistent-locale-data.md).</span><span class="sxs-lookup"><span data-stu-id="0fd73-108">If your application must persist or transmit data, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0fd73-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fd73-109">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0fd73-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fd73-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fd73-111">*lpszLocale* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0fd73-111">*lpszLocale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd73-112">Ponteiro para um nome de localidade ou um dos valores predefinidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0fd73-112">Pointer to a locale name, or one of the following predefined values.</span></span>

-   [<span data-ttu-id="0fd73-113">nome da localidade \_ \_ invariável</span><span class="sxs-lookup"><span data-stu-id="0fd73-113">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="0fd73-114">nome da localidade \_ \_ padrão do sistema \_</span><span class="sxs-lookup"><span data-stu-id="0fd73-114">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="0fd73-115">nome da localidade \_ \_ usuário \_ padrão</span><span class="sxs-lookup"><span data-stu-id="0fd73-115">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="0fd73-116">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0fd73-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd73-117">Sinalizadores que especificam opções de formato de data.</span><span class="sxs-lookup"><span data-stu-id="0fd73-117">Flags specifying date format options.</span></span> <span data-ttu-id="0fd73-118">Se *lpFormat* não estiver definido como **NULL**, esse parâmetro deverá ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="0fd73-118">If *lpFormat* is not set to **NULL**, this parameter must be set to 0.</span></span> <span data-ttu-id="0fd73-119">Se *lpFormat* for definido como **NULL**, o aplicativo poderá especificar uma combinação dos seguintes valores e [ \_ NOUSEROVERRIDE de localidade](locale-nouseroverride.md).</span><span class="sxs-lookup"><span data-stu-id="0fd73-119">If *lpFormat* is set to **NULL**, the application can specify a combination of the following values and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md).</span></span>



| <span data-ttu-id="0fd73-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0fd73-120">Value</span></span>                                                                                                                                                               | <span data-ttu-id="0fd73-121">Significado</span><span class="sxs-lookup"><span data-stu-id="0fd73-121">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <span data-ttu-id="0fd73-122"><dt>**Data de \_ SHORTDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="0fd73-122"><dt>**DATE\_SHORTDATE**</dt></span></span> </dl>    | <span data-ttu-id="0fd73-123">Use o formato de data abreviada.</span><span class="sxs-lookup"><span data-stu-id="0fd73-123">Use the short date format.</span></span> <span data-ttu-id="0fd73-124">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="0fd73-124">This is the default.</span></span> <span data-ttu-id="0fd73-125">Esse valor não pode ser usado com a data \_ LONGDATE ou a data \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="0fd73-125">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span> <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <span data-ttu-id="0fd73-126"><dt>**Data de \_ LONGDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="0fd73-126"><dt>**DATE\_LONGDATE**</dt></span></span> </dl>       | <span data-ttu-id="0fd73-127">Use o formato de data por extenso.</span><span class="sxs-lookup"><span data-stu-id="0fd73-127">Use the long date format.</span></span> <span data-ttu-id="0fd73-128">Esse valor não pode ser usado com a data \_ SHORTDATE ou a data \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="0fd73-128">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span> <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <span data-ttu-id="0fd73-129"><dt>**Data de \_ YEARMONTH**</dt></span><span class="sxs-lookup"><span data-stu-id="0fd73-129"><dt>**DATE\_YEARMONTH**</dt></span></span> </dl>    | <span data-ttu-id="0fd73-130">Use o formato de ano/mês.</span><span class="sxs-lookup"><span data-stu-id="0fd73-130">Use the year/month format.</span></span> <span data-ttu-id="0fd73-131">Esse valor não pode ser usado com a data \_ SHORTDATE ou a data \_ LONGDATE.</span><span class="sxs-lookup"><span data-stu-id="0fd73-131">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span><br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <span data-ttu-id="0fd73-132"><dt>**Data de \_ LTRREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="0fd73-132"><dt>**DATE\_LTRREADING**</dt></span></span> </dl> | <span data-ttu-id="0fd73-133">Adicionar marcas para layout de leitura da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="0fd73-133">Add marks for left-to-right reading layout.</span></span> <span data-ttu-id="0fd73-134">Esse valor não pode ser usado com a data \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="0fd73-134">This value cannot be used with DATE\_RTLREADING.</span></span><br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <span data-ttu-id="0fd73-135"><dt>**Data de \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="0fd73-135"><dt>**DATE\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="0fd73-136">Adicionar marcas para layout de leitura da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="0fd73-136">Add marks for right-to-left reading layout.</span></span> <span data-ttu-id="0fd73-137">Este valor não pode ser usado com a data \_ LTRREADING</span><span class="sxs-lookup"><span data-stu-id="0fd73-137">This value cannot be used with DATE\_LTRREADING</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="0fd73-138">*lpCalDateTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0fd73-138">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd73-139">Ponteiro para uma estrutura [**CALDATETIME**](caldatetime.md) que contém as informações de data e calendário a serem formatadas.</span><span class="sxs-lookup"><span data-stu-id="0fd73-139">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to format.</span></span>

</dd> <dt>

<span data-ttu-id="0fd73-140">*lpFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0fd73-140">*lpFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd73-141">Ponteiro para uma cadeia de caracteres de imagem de formato que é usada para formar a cadeia de caracteres de data.</span><span class="sxs-lookup"><span data-stu-id="0fd73-141">Pointer to a format picture string that is used to form the date string.</span></span> <span data-ttu-id="0fd73-142">Os valores possíveis para a cadeia de caracteres de imagem de formato são definidos nas [imagens de formato dia, mês, ano e era](day--month--year--and-era-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="0fd73-142">Possible values for the format picture string are defined in [Day, Month, Year, and Era Format Pictures](day--month--year--and-era-format-pictures.md).</span></span>

<span data-ttu-id="0fd73-143">A cadeia de caracteres de imagem de formato deve ser terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="0fd73-143">The format picture string must be null-terminated.</span></span> <span data-ttu-id="0fd73-144">A função usa a localidade somente para informações não especificadas na cadeia de caracteres de imagem de formato, por exemplo, os nomes de dia e mês para a localidade.</span><span class="sxs-lookup"><span data-stu-id="0fd73-144">The function uses the locale only for information not specified in the format picture string, for example, the day and month names for the locale.</span></span> <span data-ttu-id="0fd73-145">O aplicativo definirá esse parâmetro como **NULL** se a função for usar o formato de data da localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="0fd73-145">The application sets this parameter to **NULL** if the function is to use the date format of the specified locale.</span></span>

</dd> <dt>

<span data-ttu-id="0fd73-146">*lpDateStr* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0fd73-146">*lpDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd73-147">Ponteiro para um buffer no qual essa função recebe a cadeia de caracteres de data formatada.</span><span class="sxs-lookup"><span data-stu-id="0fd73-147">Pointer to a buffer in which this function receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="0fd73-148">*cchDate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0fd73-148">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd73-149">Tamanho, em caracteres, do buffer *lpDateStr* .</span><span class="sxs-lookup"><span data-stu-id="0fd73-149">Size, in characters, of the *lpDateStr* buffer.</span></span> <span data-ttu-id="0fd73-150">Como alternativa, o aplicativo pode definir esse parâmetro como 0.</span><span class="sxs-lookup"><span data-stu-id="0fd73-150">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="0fd73-151">Nesse caso, a função retorna o número de caracteres necessários para manter a cadeia de caracteres de data formatada e o parâmetro *lpDateStr* não é usado.</span><span class="sxs-lookup"><span data-stu-id="0fd73-151">In this case, the function returns the number of characters required to hold the formatted date string, and the *lpDateStr* parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fd73-152">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0fd73-152">Return value</span></span>

<span data-ttu-id="0fd73-153">Retorna o número de caracteres gravados no buffer *lpDateStr* se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0fd73-153">Returns the number of characters written to the *lpDateStr* buffer if successful.</span></span> <span data-ttu-id="0fd73-154">Se o parâmetro *cchDate* for definido como 0, a função retornará o número de caracteres necessários para manter a cadeia de caracteres de data formatada, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="0fd73-154">If the *cchDate* parameter is set to 0, the function returns the number of characters required to hold the formatted date string, including the terminating null character.</span></span>

<span data-ttu-id="0fd73-155">Essa função retornará 0 se não tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="0fd73-155">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="0fd73-156">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="0fd73-156">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="0fd73-157">\_Data \_ de erro fora \_ do \_ intervalo.</span><span class="sxs-lookup"><span data-stu-id="0fd73-157">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="0fd73-158">A data especificada estava fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="0fd73-158">The specified date was out of range.</span></span>
-   <span data-ttu-id="0fd73-159">ERRO \_ de \_ buffer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="0fd73-159">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="0fd73-160">Um tamanho de buffer fornecido não era grande o suficiente ou foi definido incorretamente como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0fd73-160">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="0fd73-161">ERROS de \_ Sinalizadores inválidos \_ .</span><span class="sxs-lookup"><span data-stu-id="0fd73-161">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="0fd73-162">Os valores fornecidos para sinalizadores não eram válidos.</span><span class="sxs-lookup"><span data-stu-id="0fd73-162">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="0fd73-163">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="0fd73-163">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="0fd73-164">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="0fd73-164">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fd73-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fd73-165">Remarks</span></span>

<span data-ttu-id="0fd73-166">A data mais antiga com suporte nesta função é 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="0fd73-166">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="0fd73-167">Essa função não tem um arquivo de cabeçalho ou arquivo de biblioteca associado.</span><span class="sxs-lookup"><span data-stu-id="0fd73-167">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="0fd73-168">O aplicativo pode chamar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Kernel32.dll) para obter um identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="0fd73-168">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="0fd73-169">Em seguida, ele pode chamar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse identificador de módulo e o nome dessa função para obter o endereço da função.</span><span class="sxs-lookup"><span data-stu-id="0fd73-169">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd73-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fd73-170">Requirements</span></span>



| <span data-ttu-id="0fd73-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fd73-171">Requirement</span></span> | <span data-ttu-id="0fd73-172">Valor</span><span class="sxs-lookup"><span data-stu-id="0fd73-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd73-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fd73-173">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd73-174">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fd73-174">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0fd73-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fd73-175">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd73-176">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0fd73-176">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0fd73-177">DLL</span><span class="sxs-lookup"><span data-stu-id="0fd73-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fd73-178"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fd73-178"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fd73-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fd73-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd73-180">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="0fd73-180">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="0fd73-181">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="0fd73-181">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="0fd73-182">Imagens de formato de dia, mês, ano e era</span><span class="sxs-lookup"><span data-stu-id="0fd73-182">Day, Month, Year, and Era Format Pictures</span></span>](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[<span data-ttu-id="0fd73-183">NLS: exemplo de APIs baseadas em nome</span><span class="sxs-lookup"><span data-stu-id="0fd73-183">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> <dt>

[<span data-ttu-id="0fd73-184">**EnumDateFormatsExEx**</span><span class="sxs-lookup"><span data-stu-id="0fd73-184">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[<span data-ttu-id="0fd73-185">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="0fd73-185">**GetDateFormat**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[<span data-ttu-id="0fd73-186">**GetDateFormatEx**</span><span class="sxs-lookup"><span data-stu-id="0fd73-186">**GetDateFormatEx**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[<span data-ttu-id="0fd73-187">**CALDATETIME**</span><span class="sxs-lookup"><span data-stu-id="0fd73-187">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
