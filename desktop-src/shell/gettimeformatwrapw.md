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
# <a name="gettimeformatwrapw-function"></a><span data-ttu-id="0029d-103">Função GetTimeFormatWrapW</span><span class="sxs-lookup"><span data-stu-id="0029d-103">GetTimeFormatWrapW function</span></span>

<span data-ttu-id="0029d-104">\[O **GetTimeFormatWrapW** está disponível para uso no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0029d-104">\[**GetTimeFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="0029d-105">Ele pode não estar disponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0029d-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="0029d-106">Você deve usar [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) em seu lugar.\]</span><span class="sxs-lookup"><span data-stu-id="0029d-106">You should use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in its place.\]</span></span>

<span data-ttu-id="0029d-107">Formata o tempo como uma cadeia de hora para uma localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="0029d-107">Formats time as a time string for a specified locale.</span></span> <span data-ttu-id="0029d-108">A função formata uma hora especificada ou a hora do sistema local.</span><span class="sxs-lookup"><span data-stu-id="0029d-108">The function formats either a specified time or the local system time.</span></span>

> [!Note]  
> <span data-ttu-id="0029d-109">**GetTimeFormatWrapW** é um wrapper para a função **GetTimeFormatW** .</span><span class="sxs-lookup"><span data-stu-id="0029d-109">**GetTimeFormatWrapW** is a wrapper for the **GetTimeFormatW** function.</span></span> <span data-ttu-id="0029d-110">Consulte a página [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) para ver mais observações de uso.</span><span class="sxs-lookup"><span data-stu-id="0029d-110">See the [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0029d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0029d-111">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0029d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0029d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0029d-113">*Localidade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0029d-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0029d-114">Tipo: **LCID**</span><span class="sxs-lookup"><span data-stu-id="0029d-114">Type: **LCID**</span></span>

<span data-ttu-id="0029d-115">Especifica a localidade para a qual a cadeia de caracteres de tempo deve ser formatada.</span><span class="sxs-lookup"><span data-stu-id="0029d-115">Specifies the locale for which the time string is to be formatted.</span></span> <span data-ttu-id="0029d-116">Se *pwzFormat* for **NULL**, a função formatará a cadeia de caracteres de acordo com o formato de hora dessa localidade.</span><span class="sxs-lookup"><span data-stu-id="0029d-116">If *pwzFormat* is **NULL**, the function formats the string according to the time format for this locale.</span></span> <span data-ttu-id="0029d-117">Se *pwzFormat* não for **NULL**, a função usará a localidade somente para informações não especificadas na cadeia de caracteres de imagem de formato (por exemplo, os marcadores de tempo da localidade).</span><span class="sxs-lookup"><span data-stu-id="0029d-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's time markers).</span></span>

<span data-ttu-id="0029d-118">Esse parâmetro pode ser um identificador de localidade criado pela macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) ou um dos valores predefinidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0029d-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="0029d-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**\_padrão do sistema de localidade \_**</span><span class="sxs-lookup"><span data-stu-id="0029d-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="0029d-120">Localidade do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="0029d-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="0029d-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_padrão de usuário de localidade \_**</span><span class="sxs-lookup"><span data-stu-id="0029d-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="0029d-122">Localidade do usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="0029d-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0029d-123">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0029d-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0029d-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0029d-124">Type: **DWORD**</span></span>

<span data-ttu-id="0029d-125">Especifica várias opções de função.</span><span class="sxs-lookup"><span data-stu-id="0029d-125">Specifies various function options.</span></span> <span data-ttu-id="0029d-126">Você pode especificar uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0029d-126">You can specify a combination of the following values.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="0029d-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**NOUSEROVERRIDE de localidade \_**</span><span class="sxs-lookup"><span data-stu-id="0029d-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="0029d-128">Se definido, a função formata a cadeia de caracteres usando o formato de hora padrão do sistema para a localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="0029d-128">If set, the function formats the string using the system default time format for the specified locale.</span></span> <span data-ttu-id="0029d-129">Se não for definido, a função formatará a cadeia de caracteres usando qualquer substituição de usuário para o formato de hora padrão da localidade.</span><span class="sxs-lookup"><span data-stu-id="0029d-129">If not set, the function formats the string using any user overrides to the locale's default time format.</span></span> <span data-ttu-id="0029d-130">Esse sinalizador só poderá ser definido se *pwzFormat* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0029d-130">This flag can only be set if *pwzFormat* is **NULL**.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="0029d-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALIDADE \_ use \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="0029d-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="0029d-132">Usa a página de código ANSI do sistema para conversão de cadeia de caracteres em vez da página de código de localidade.</span><span class="sxs-lookup"><span data-stu-id="0029d-132">Uses the system ANSI code page for string translation instead of the locale code page.</span></span>

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span data-ttu-id="0029d-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**NOMINUTESORSECONDS de tempo \_**</span><span class="sxs-lookup"><span data-stu-id="0029d-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TIME\_NOMINUTESORSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="0029d-134">Não usa minutos ou segundos.</span><span class="sxs-lookup"><span data-stu-id="0029d-134">Does not use minutes or seconds.</span></span>

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span data-ttu-id="0029d-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TEMPO em \_ segundos**</span><span class="sxs-lookup"><span data-stu-id="0029d-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TIME\_NOSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="0029d-136">Não usa segundos.</span><span class="sxs-lookup"><span data-stu-id="0029d-136">Does not use seconds.</span></span>

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span data-ttu-id="0029d-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**NOTIMEMARKER de tempo \_**</span><span class="sxs-lookup"><span data-stu-id="0029d-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TIME\_NOTIMEMARKER**</span></span>


</dt> <dd>

<span data-ttu-id="0029d-138">Não usa um marcador de tempo.</span><span class="sxs-lookup"><span data-stu-id="0029d-138">Does not use a time marker.</span></span>

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span data-ttu-id="0029d-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**FORCE24HOURFORMAT de tempo \_**</span><span class="sxs-lookup"><span data-stu-id="0029d-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TIME\_FORCE24HOURFORMAT**</span></span>


</dt> <dd>

<span data-ttu-id="0029d-140">Sempre usa um formato de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="0029d-140">Always uses a 24-hour time format.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0029d-141">*lpTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0029d-141">*lpTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0029d-142">Tipo: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="0029d-142">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="0029d-143">Um ponteiro para uma estrutura [_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contém as informações de hora a serem formatadas.</span><span class="sxs-lookup"><span data-stu-id="0029d-143">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the time information to be formatted.</span></span> <span data-ttu-id="0029d-144">Se esse ponteiro for **nulo**, a função usará a hora atual do sistema local.</span><span class="sxs-lookup"><span data-stu-id="0029d-144">If this pointer is **NULL**, the function uses the current local system time.</span></span>

</dd> <dt>

<span data-ttu-id="0029d-145">*pwzFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0029d-145">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0029d-146">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="0029d-146">Type: **LPCWSTR**</span></span>

<span data-ttu-id="0029d-147">Um ponteiro para um formato a ser usado para formar a cadeia de caracteres de tempo.</span><span class="sxs-lookup"><span data-stu-id="0029d-147">A pointer to a format to use to form the time string.</span></span> <span data-ttu-id="0029d-148">Se *pwzFormat* for **NULL**, a função usará o formato de hora da localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="0029d-148">If *pwzFormat* is **NULL**, the function uses the time format of the specified locale.</span></span> <span data-ttu-id="0029d-149">Consulte [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="0029d-149">See [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="0029d-150">*pwzTimeStr* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0029d-150">*pwzTimeStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0029d-151">Tipo: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="0029d-151">Type: **LPWSTR**</span></span>

<span data-ttu-id="0029d-152">Um ponteiro para um buffer que recebe a cadeia de caracteres de hora formatada.</span><span class="sxs-lookup"><span data-stu-id="0029d-152">A pointer to a buffer that receives the formatted time string.</span></span>

</dd> <dt>

<span data-ttu-id="0029d-153">*cchTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0029d-153">*cchTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0029d-154">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0029d-154">Type: **int**</span></span>

<span data-ttu-id="0029d-155">O tamanho, em caracteres, do buffer *pwzTimeStr* .</span><span class="sxs-lookup"><span data-stu-id="0029d-155">The size, in characters, of the *pwzTimeStr* buffer.</span></span> <span data-ttu-id="0029d-156">Se *cchTime* for zero, a função retornará o número de caracteres necessários para manter a cadeia de caracteres de tempo formatada e o buffer apontado por *pwzTimeStr* não será usado.</span><span class="sxs-lookup"><span data-stu-id="0029d-156">If *cchTime* is zero, the function returns the number of characters required to hold the formatted time string, and the buffer pointed to by *pwzTimeStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0029d-157">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0029d-157">Return value</span></span>

<span data-ttu-id="0029d-158">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0029d-158">Type: **int**</span></span>

<span data-ttu-id="0029d-159">Se a função for realizada com sucesso, o valor de retorno será o número de caracteres gravados no buffer apontado por *pwzTimeStr*.</span><span class="sxs-lookup"><span data-stu-id="0029d-159">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzTimeStr*.</span></span> <span data-ttu-id="0029d-160">Se o parâmetro *cchTime* for zero, o valor de retorno será o número de caracteres necessários para manter a cadeia de caracteres de tempo formatada.</span><span class="sxs-lookup"><span data-stu-id="0029d-160">If the *cchTime* parameter is zero, the return value is the number of characters required to hold the formatted time string.</span></span> <span data-ttu-id="0029d-161">A contagem inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="0029d-161">The count includes the terminating null character.</span></span>

<span data-ttu-id="0029d-162">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="0029d-162">If the function fails, the return value is zero.</span></span> <span data-ttu-id="0029d-163">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="0029d-163">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="0029d-164">**GetLastError** pode retornar um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="0029d-164">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="0029d-165">**ERRO \_ de \_ buffer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="0029d-165">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="0029d-166">**\_Sinalizadores inválidos de erro \_**</span><span class="sxs-lookup"><span data-stu-id="0029d-166">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="0029d-167">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="0029d-167">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0029d-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="0029d-168">Remarks</span></span>

<span data-ttu-id="0029d-169">O **GetTimeFormatWrapW** fornece a capacidade de usar cadeias de caracteres Unicode em sistemas operacionais anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0029d-169">**GetTimeFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="0029d-170">O método preferencial é usar [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) em conjunto com a camada Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="0029d-170">The preferred method is to use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="0029d-171">**GetTimeFormatWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 310.</span><span class="sxs-lookup"><span data-stu-id="0029d-171">**GetTimeFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 310.</span></span>

## <a name="requirements"></a><span data-ttu-id="0029d-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0029d-172">Requirements</span></span>



| <span data-ttu-id="0029d-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="0029d-173">Requirement</span></span> | <span data-ttu-id="0029d-174">Valor</span><span class="sxs-lookup"><span data-stu-id="0029d-174">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0029d-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0029d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="0029d-176">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0029d-176">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0029d-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0029d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="0029d-178">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0029d-178">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0029d-179">DLL</span><span class="sxs-lookup"><span data-stu-id="0029d-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0029d-180"><dt>Shlwapi.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="0029d-180"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0029d-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="0029d-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0029d-182">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="0029d-182">**GetTimeFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
