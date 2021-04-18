---
description: Converte um identificador de localidade em um nome de localidade.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: Função DownlevelLCIDToLocaleName (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 2f8e4ce9763348cf765522ebbd624a6e82f1071a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753288"
---
# <a name="downlevellcidtolocalename-function"></a><span data-ttu-id="ba8a5-103">Função DownlevelLCIDToLocaleName</span><span class="sxs-lookup"><span data-stu-id="ba8a5-103">DownlevelLCIDToLocaleName function</span></span>

<span data-ttu-id="ba8a5-104">Converte um [identificador de localidade](locale-identifiers.md) em um [nome de localidade](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="ba8a5-104">Converts a [locale identifier](locale-identifiers.md) to a [locale name](locale-names.md).</span></span>

> [!Note]  
> <span data-ttu-id="ba8a5-105">Essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="ba8a5-106">Seu uso requer um pacote de download.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-106">Its use requires a download package.</span></span> <span data-ttu-id="ba8a5-107">Os aplicativos que são executados somente no Windows Vista e posterior devem chamar [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) para recuperar um nome de localidade.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-107">Applications that run only on Windows Vista and later should call [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to retrieve a locale name.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ba8a5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba8a5-108">Syntax</span></span>


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ba8a5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba8a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba8a5-110">*Localidade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ba8a5-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba8a5-111">O identificador de localidade a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-111">The locale identifier to translate.</span></span> <span data-ttu-id="ba8a5-112">Você pode usar a macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para criar um identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier.</span></span> <span data-ttu-id="ba8a5-113">Esta função não oferece suporte a localidades neutras ou a valores de identificador de localidade específicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-113">This function does not support neutral locales or the following specific locale identifier values.</span></span>

-   [<span data-ttu-id="ba8a5-114">\_padrão do sistema de localidade \_</span><span class="sxs-lookup"><span data-stu-id="ba8a5-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="ba8a5-115">\_padrão de usuário de localidade \_</span><span class="sxs-lookup"><span data-stu-id="ba8a5-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)
-   [<span data-ttu-id="ba8a5-116">\_padrão personalizado de localidade \_</span><span class="sxs-lookup"><span data-stu-id="ba8a5-116">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="ba8a5-117">\_ \_ padrão da interface do usuário personalizada de localidade \_</span><span class="sxs-lookup"><span data-stu-id="ba8a5-117">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="ba8a5-118">LOCALIDADE \_ personalizada \_ não especificada</span><span class="sxs-lookup"><span data-stu-id="ba8a5-118">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="ba8a5-119">*lpName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ba8a5-119">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba8a5-120">Ponteiro para um buffer no qual essa função recupera o nome da localidade.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-120">Pointer to a buffer in which this function retrieves the locale name.</span></span> <span data-ttu-id="ba8a5-121">A função recupera **NULL** se *cchName* estiver definido como 0.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-121">The function retrieves **NULL** if *cchName* is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="ba8a5-122">*cchName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba8a5-122">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba8a5-123">Tamanho, em pontos de código UTF-16, do buffer de nome de localidade.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-123">Size, in UTF-16 code points, of the locale name buffer.</span></span> <span data-ttu-id="ba8a5-124">O aplicativo define esse parâmetro como 0 para retornar o tamanho necessário do buffer de nome de localidade.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-124">The application sets this parameter to 0 to return the required size of the locale name buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ba8a5-125">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba8a5-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba8a5-126">Sinalizadores que especificam o tipo de nome a recuperar.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-126">Flags specifying the type of name to retrieve.</span></span> <span data-ttu-id="ba8a5-127">O valor padrão é nome de localidade de nível inferior \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ba8a5-127">The default value is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba8a5-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba8a5-128">Return value</span></span>

<span data-ttu-id="ba8a5-129">Retorna a contagem de pontos de código UTF-16 no nome da localidade, incluindo o caractere nulo de terminação, se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-129">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span> <span data-ttu-id="ba8a5-130">Se a função for bem sucedido e o valor de *cchName* for 0, o valor de retorno será o tamanho necessário, em caracteres (incluindo caracteres nulos), para o buffer de nome de localidade.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-130">If the function succeeds and the value of *cchName* is 0, the return value is the required size, in characters (including null characters), for the locale name buffer.</span></span>

<span data-ttu-id="ba8a5-131">A função retornará 0 se não tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-131">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="ba8a5-132">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="ba8a5-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="ba8a5-133">ERRO \_ de \_ buffer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="ba8a5-134">Um tamanho de buffer fornecido não era grande o suficiente ou foi definido incorretamente como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="ba8a5-135">ERROS de \_ Sinalizadores inválidos \_ .</span><span class="sxs-lookup"><span data-stu-id="ba8a5-135">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="ba8a5-136">O valor de *dwFlags* não é válido.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-136">The value of *dwFlags* is not valid.</span></span>
-   <span data-ttu-id="ba8a5-137">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="ba8a5-137">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="ba8a5-138">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="ba8a5-138">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba8a5-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba8a5-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ba8a5-140">Essa função não oferece suporte a [localidades personalizadas](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="ba8a5-140">This function does not support [custom locales](custom-locales.md).</span></span>

 

<span data-ttu-id="ba8a5-141">O arquivo de cabeçalho e a DLL necessários fazem parte do download "APIs de mapeamento de dados de nível inferior do Microsoft NLS", disponível no [centro de download da Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="ba8a5-141">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba8a5-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba8a5-142">Requirements</span></span>



| <span data-ttu-id="ba8a5-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba8a5-143">Requirement</span></span> | <span data-ttu-id="ba8a5-144">Valor</span><span class="sxs-lookup"><span data-stu-id="ba8a5-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba8a5-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba8a5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ba8a5-146">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ba8a5-146">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="ba8a5-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba8a5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ba8a5-148">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba8a5-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ba8a5-149">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ba8a5-149">Redistributable</span></span><br/>          | <span data-ttu-id="ba8a5-150">APIs de mapeamento de dados de nível inferior do Microsoft NLS onwindows XP com SP2 e laterorWindows vista</span><span class="sxs-lookup"><span data-stu-id="ba8a5-150">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="ba8a5-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba8a5-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba8a5-152"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba8a5-152"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="ba8a5-153">DLL</span><span class="sxs-lookup"><span data-stu-id="ba8a5-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba8a5-154"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba8a5-154"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ba8a5-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba8a5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba8a5-156">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="ba8a5-156">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="ba8a5-157">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="ba8a5-157">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="ba8a5-158">Mapeando dados de localidade</span><span class="sxs-lookup"><span data-stu-id="ba8a5-158">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="ba8a5-159">**LCIDToLocaleName**</span><span class="sxs-lookup"><span data-stu-id="ba8a5-159">**LCIDToLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
