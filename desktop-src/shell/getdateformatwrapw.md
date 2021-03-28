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
ms.openlocfilehash: c9c369584fd15a27d5e684452b2277104b5b1da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169436"
---
# <a name="getdateformatwrapw-function"></a><span data-ttu-id="33492-103">Função GetDateFormatWrapW</span><span class="sxs-lookup"><span data-stu-id="33492-103">GetDateFormatWrapW function</span></span>

<span data-ttu-id="33492-104">\[O **GetDateFormatWrapW** está disponível para uso no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="33492-104">\[**GetDateFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="33492-105">Ele não estará disponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="33492-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="33492-106">Você deve usar [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) em seu lugar.\]</span><span class="sxs-lookup"><span data-stu-id="33492-106">You should use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in its place.\]</span></span>

<span data-ttu-id="33492-107">Formata uma data como uma cadeia de caracteres de data para uma localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="33492-107">Formats a date as a date string for a specified locale.</span></span> <span data-ttu-id="33492-108">A função formata uma data especificada ou a data do sistema local.</span><span class="sxs-lookup"><span data-stu-id="33492-108">The function formats either a specified date or the local system date.</span></span>

> [!Note]  
> <span data-ttu-id="33492-109">**GetDateFormatWrapW** é um wrapper para a função **GetDateFormatW** .</span><span class="sxs-lookup"><span data-stu-id="33492-109">**GetDateFormatWrapW** is a wrapper for the **GetDateFormatW** function.</span></span> <span data-ttu-id="33492-110">Consulte a página [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) para ver mais observações de uso.</span><span class="sxs-lookup"><span data-stu-id="33492-110">See the [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="33492-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33492-111">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="33492-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33492-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33492-113">*Localidade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="33492-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33492-114">Tipo: **LCID**</span><span class="sxs-lookup"><span data-stu-id="33492-114">Type: **LCID**</span></span>

<span data-ttu-id="33492-115">A localidade para a qual a cadeia de caracteres de data deve ser formatada.</span><span class="sxs-lookup"><span data-stu-id="33492-115">The locale for which the date string is to be formatted.</span></span> <span data-ttu-id="33492-116">Se *pwzFormat* for **NULL**, a função formatará a cadeia de caracteres de acordo com o formato de data dessa localidade.</span><span class="sxs-lookup"><span data-stu-id="33492-116">If *pwzFormat* is **NULL**, the function formats the string according to the date format for this locale.</span></span> <span data-ttu-id="33492-117">Se *pwzFormat* não for **NULL**, a função usará a localidade somente para informações não especificadas na cadeia de caracteres de imagem de formato (por exemplo, os nomes de dia e mês da localidade).</span><span class="sxs-lookup"><span data-stu-id="33492-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's day and month names).</span></span>

<span data-ttu-id="33492-118">Esse parâmetro pode ser um identificador de localidade criado pela macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) ou um dos valores predefinidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="33492-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="33492-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**\_padrão do sistema de localidade \_**</span><span class="sxs-lookup"><span data-stu-id="33492-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="33492-120">Localidade do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="33492-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="33492-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_padrão de usuário de localidade \_**</span><span class="sxs-lookup"><span data-stu-id="33492-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="33492-122">Localidade do usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="33492-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="33492-123">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33492-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33492-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="33492-124">Type: **DWORD**</span></span>

<span data-ttu-id="33492-125">Especifica várias opções de função.</span><span class="sxs-lookup"><span data-stu-id="33492-125">Specifies various function options.</span></span> <span data-ttu-id="33492-126">Se *pwzFormat* não for **NULL**, esse parâmetro deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="33492-126">If *pwzFormat* is not **NULL**, this parameter must be zero.</span></span> <span data-ttu-id="33492-127">Se *pwzFormat* for **nulo**, você poderá especificar uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="33492-127">If *pwzFormat* is **NULL**, you can specify a combination of the following values.</span></span> <span data-ttu-id="33492-128">Se você não especificar a data \_ YEARMONTH, a data \_ SHORTDATE ou a data \_ LONGDATE e *pwzFormat* for **NULL**, \_ a data SHORTDATE será usada como padrão.</span><span class="sxs-lookup"><span data-stu-id="33492-128">If you do not specify either DATE\_YEARMONTH, DATE\_SHORTDATE, or DATE\_LONGDATE, and *pwzFormat* is **NULL**, then DATE\_SHORTDATE is used as the default.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="33492-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**NOUSEROVERRIDE de localidade \_**</span><span class="sxs-lookup"><span data-stu-id="33492-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="33492-130">Se definido, a função formata a cadeia de caracteres usando o formato de data padrão do sistema para a localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="33492-130">If set, the function formats the string using the system default date format for the specified locale.</span></span> <span data-ttu-id="33492-131">Se não for definido, a função formatará a cadeia de caracteres usando qualquer substituição de usuário para o formato de data padrão da localidade.</span><span class="sxs-lookup"><span data-stu-id="33492-131">If not set, the function formats the string using any user overrides to the locale's default date format.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="33492-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALIDADE \_ use \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="33492-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="33492-133">Usa a página de código ANSI do sistema para conversão de cadeia de caracteres em vez da página de código da localidade.</span><span class="sxs-lookup"><span data-stu-id="33492-133">Uses the system ANSI code page for string translation instead of the locale's code page.</span></span>

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span data-ttu-id="33492-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**Data de \_ SHORTDATE**</span><span class="sxs-lookup"><span data-stu-id="33492-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**DATE\_SHORTDATE**</span></span>


</dt> <dd>

<span data-ttu-id="33492-135">Usa o formato de data abreviada.</span><span class="sxs-lookup"><span data-stu-id="33492-135">Uses the short date format.</span></span> <span data-ttu-id="33492-136">Esse valor não pode ser usado com a data \_ LONGDATE ou a data \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="33492-136">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span data-ttu-id="33492-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**Data de \_ LONGDATE**</span><span class="sxs-lookup"><span data-stu-id="33492-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**DATE\_LONGDATE**</span></span>


</dt> <dd>

<span data-ttu-id="33492-138">Usa o formato de data por extenso.</span><span class="sxs-lookup"><span data-stu-id="33492-138">Uses the long date format.</span></span> <span data-ttu-id="33492-139">Esse valor não pode ser usado com a data \_ SHORTDATE ou a data \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="33492-139">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span data-ttu-id="33492-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**Data de \_ YEARMONTH**</span><span class="sxs-lookup"><span data-stu-id="33492-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**DATE\_YEARMONTH**</span></span>


</dt> <dd>

<span data-ttu-id="33492-141">Usa o formato de ano/mês.</span><span class="sxs-lookup"><span data-stu-id="33492-141">Uses the year/month format.</span></span> <span data-ttu-id="33492-142">Esse valor não pode ser usado com a data \_ SHORTDATE ou a data \_ LONGDATE.</span><span class="sxs-lookup"><span data-stu-id="33492-142">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span>

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span data-ttu-id="33492-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**\_ \_ calendário Alt de uso de data \_**</span><span class="sxs-lookup"><span data-stu-id="33492-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**DATE\_USE\_ALT\_CALENDAR**</span></span>


</dt> <dd>

<span data-ttu-id="33492-144">Usa o calendário alternativo, se houver, para formatar a cadeia de caracteres de data.</span><span class="sxs-lookup"><span data-stu-id="33492-144">Uses the alternate calendar, if one exists, to format the date string.</span></span> <span data-ttu-id="33492-145">Se esse sinalizador for definido, a função usará o formato padrão para esse calendário alternativo, em vez de usar qualquer substituição de usuário.</span><span class="sxs-lookup"><span data-stu-id="33492-145">If this flag is set, the function uses the default format for that alternate calendar, rather than using any user overrides.</span></span> <span data-ttu-id="33492-146">As substituições de usuário serão usadas somente no caso de não haver nenhum formato padrão para o calendário alternativo especificado.</span><span class="sxs-lookup"><span data-stu-id="33492-146">The user overrides will be used only in the event that there is no default format for the specified alternate calendar.</span></span>

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span data-ttu-id="33492-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**Data de \_ LTRREADING**</span><span class="sxs-lookup"><span data-stu-id="33492-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**DATE\_LTRREADING**</span></span>


</dt> <dd>

<span data-ttu-id="33492-148">Adiciona marcas para layout de leitura da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="33492-148">Adds marks for left-to-right reading layout.</span></span> <span data-ttu-id="33492-149">Esse valor não pode ser usado com a data \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="33492-149">This value cannot be used with DATE\_RTLREADING.</span></span>

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span data-ttu-id="33492-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**Data de \_ RTLREADING**</span><span class="sxs-lookup"><span data-stu-id="33492-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**DATE\_RTLREADING**</span></span>


</dt> <dd>

<span data-ttu-id="33492-151">Adiciona marcas para layout de leitura da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="33492-151">Adds marks for right-to-left reading layout.</span></span> <span data-ttu-id="33492-152">Esse valor não pode ser usado com a data \_ LTRREADING.</span><span class="sxs-lookup"><span data-stu-id="33492-152">This value cannot be used with DATE\_LTRREADING.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="33492-153">*lpDate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33492-153">*lpDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33492-154">Tipo: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="33492-154">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="33492-155">Um ponteiro para uma estrutura [_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contém as informações de data a serem formatadas.</span><span class="sxs-lookup"><span data-stu-id="33492-155">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date information to be formatted.</span></span> <span data-ttu-id="33492-156">Se esse ponteiro for **nulo**, a função usará a data atual do sistema local.</span><span class="sxs-lookup"><span data-stu-id="33492-156">If this pointer is **NULL**, the function uses the current local system date.</span></span>

</dd> <dt>

<span data-ttu-id="33492-157">*pwzFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33492-157">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33492-158">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="33492-158">Type: **LPCWSTR**</span></span>

<span data-ttu-id="33492-159">Um ponteiro para uma imagem de formato a ser usada para formar a cadeia de caracteres de data.</span><span class="sxs-lookup"><span data-stu-id="33492-159">A pointer to a format picture to use to form the date string.</span></span> <span data-ttu-id="33492-160">Se *pwzFormat* for **NULL**, a função usará o formato de data da localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="33492-160">If *pwzFormat* is **NULL**, the function uses the date format of the specified locale.</span></span> <span data-ttu-id="33492-161">Consulte [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="33492-161">See [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="33492-162">*pwzDateStr* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="33492-162">*pwzDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33492-163">Tipo: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="33492-163">Type: **LPWSTR**</span></span>

<span data-ttu-id="33492-164">Um ponteiro para um buffer que recebe a cadeia de caracteres de data formatada.</span><span class="sxs-lookup"><span data-stu-id="33492-164">A pointer to a buffer that receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="33492-165">*cchDate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33492-165">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33492-166">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="33492-166">Type: **int**</span></span>

<span data-ttu-id="33492-167">Especifica o tamanho, em caracteres, do buffer *pwzDateStr* .</span><span class="sxs-lookup"><span data-stu-id="33492-167">Specifies the size, in characters, of the *pwzDateStr* buffer.</span></span> <span data-ttu-id="33492-168">Se *cchDate* for zero, a função retornará o número de caracteres necessários para manter a cadeia de caracteres de data formatada e o buffer apontado por *pwzDateStr* não será usado.</span><span class="sxs-lookup"><span data-stu-id="33492-168">If *cchDate* is zero, the function returns the number of characters required to hold the formatted date string, and the buffer pointed to by *pwzDateStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33492-169">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33492-169">Return value</span></span>

<span data-ttu-id="33492-170">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="33492-170">Type: **int**</span></span>

<span data-ttu-id="33492-171">Se a função for realizada com sucesso, o valor de retorno será o número de caracteres gravados no buffer apontado por *pwzDateStr*.</span><span class="sxs-lookup"><span data-stu-id="33492-171">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzDateStr*.</span></span> <span data-ttu-id="33492-172">Se o parâmetro *cchDate* for zero, o valor de retorno será o número de caracteres necessários para manter a cadeia de caracteres de data formatada.</span><span class="sxs-lookup"><span data-stu-id="33492-172">If the *cchDate* parameter is zero, the return value is the number of characters required to hold the formatted date string.</span></span> <span data-ttu-id="33492-173">A contagem inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="33492-173">The count includes the terminating null character.</span></span>

<span data-ttu-id="33492-174">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="33492-174">If the function fails, the return value is zero.</span></span> <span data-ttu-id="33492-175">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="33492-175">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="33492-176">**GetLastError** pode retornar um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="33492-176">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="33492-177">**ERRO \_ de \_ buffer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="33492-177">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="33492-178">**\_Sinalizadores inválidos de erro \_**</span><span class="sxs-lookup"><span data-stu-id="33492-178">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="33492-179">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="33492-179">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="33492-180">Comentários</span><span class="sxs-lookup"><span data-stu-id="33492-180">Remarks</span></span>

<span data-ttu-id="33492-181">O **GetDateFormatWrapW** fornece a capacidade de usar cadeias de caracteres Unicode em sistemas operacionais anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="33492-181">**GetDateFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="33492-182">O método preferencial é usar [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) em conjunto com a camada Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="33492-182">The preferred method is to use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="33492-183">**GetDateFormatWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 311.</span><span class="sxs-lookup"><span data-stu-id="33492-183">**GetDateFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 311.</span></span>

## <a name="requirements"></a><span data-ttu-id="33492-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33492-184">Requirements</span></span>



| <span data-ttu-id="33492-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="33492-185">Requirement</span></span> | <span data-ttu-id="33492-186">Valor</span><span class="sxs-lookup"><span data-stu-id="33492-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33492-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33492-187">Minimum supported client</span></span><br/> | <span data-ttu-id="33492-188">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="33492-188">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33492-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33492-189">Minimum supported server</span></span><br/> | <span data-ttu-id="33492-190">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33492-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="33492-191">DLL</span><span class="sxs-lookup"><span data-stu-id="33492-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33492-192"><dt>Shlwapi.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="33492-192"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33492-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="33492-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33492-194">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="33492-194">**GetDateFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
