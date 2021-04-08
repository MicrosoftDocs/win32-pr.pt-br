---
description: Recupera o nome da localidade para o pai da localidade fornecida.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Função DownlevelGetParentLocaleName (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: d3a556d68c33249d2e6b49c48035cc58d8bac8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922549"
---
# <a name="downlevelgetparentlocalename-function"></a><span data-ttu-id="a9798-103">Função DownlevelGetParentLocaleName</span><span class="sxs-lookup"><span data-stu-id="a9798-103">DownlevelGetParentLocaleName function</span></span>

<span data-ttu-id="a9798-104">Recupera o [nome da localidade](locale-names.md) para o pai da localidade fornecida.</span><span class="sxs-lookup"><span data-stu-id="a9798-104">Retrieves the [locale name](locale-names.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="a9798-105">Essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a9798-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="a9798-106">Seu uso requer o pacote de download.</span><span class="sxs-lookup"><span data-stu-id="a9798-106">Its use requires the download package.</span></span> <span data-ttu-id="a9798-107">Os aplicativos que só são executados no Windows Vista e posterior devem chamar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) com *LCTYPE* definido como [localidade \_ SPARENT](locale-sparent.md).</span><span class="sxs-lookup"><span data-stu-id="a9798-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a9798-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9798-108">Syntax</span></span>


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a><span data-ttu-id="a9798-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9798-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9798-110">*Localidade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a9798-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9798-111">[Identificador de localidade](locale-identifiers.md) da localidade.</span><span class="sxs-lookup"><span data-stu-id="a9798-111">[Locale identifier](locale-identifiers.md) of the locale.</span></span> <span data-ttu-id="a9798-112">Você pode usar a macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para criar um identificador de localidade ou usar um dos valores predefinidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a9798-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="a9798-113">LOCALIDADE \_ invariável</span><span class="sxs-lookup"><span data-stu-id="a9798-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="a9798-114">\_padrão do sistema de localidade \_</span><span class="sxs-lookup"><span data-stu-id="a9798-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="a9798-115">\_padrão de usuário de localidade \_</span><span class="sxs-lookup"><span data-stu-id="a9798-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="a9798-116">**Windows Vista e posterior:** Também há suporte para os seguintes identificadores de localidade personalizados.</span><span class="sxs-lookup"><span data-stu-id="a9798-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="a9798-117">\_padrão personalizado de localidade \_</span><span class="sxs-lookup"><span data-stu-id="a9798-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="a9798-118">\_ \_ padrão da interface do usuário personalizada de localidade \_</span><span class="sxs-lookup"><span data-stu-id="a9798-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="a9798-119">LOCALIDADE \_ personalizada \_ não especificada</span><span class="sxs-lookup"><span data-stu-id="a9798-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="a9798-120">*lpName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a9798-120">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9798-121">Ponteiro para um buffer no qual a função recupera o nome da localidade pai ou um dos valores predefinidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a9798-121">Pointer to a buffer in which the function retrieves the parent locale name, or one of the following predefined values.</span></span> <span data-ttu-id="a9798-122">Esse parâmetro será definido como **NULL** se *cchName* for definido como 0.</span><span class="sxs-lookup"><span data-stu-id="a9798-122">This parameter is set to **NULL** if *cchName* is set to 0.</span></span>

-   [<span data-ttu-id="a9798-123">nome da localidade \_ \_ invariável</span><span class="sxs-lookup"><span data-stu-id="a9798-123">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="a9798-124">nome da localidade \_ \_ padrão do sistema \_</span><span class="sxs-lookup"><span data-stu-id="a9798-124">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="a9798-125">nome da localidade \_ \_ usuário \_ padrão</span><span class="sxs-lookup"><span data-stu-id="a9798-125">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="a9798-126">*cchName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9798-126">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9798-127">Tamanho do buffer indicado por *lpName*, em pontos de código UTF-16.</span><span class="sxs-lookup"><span data-stu-id="a9798-127">Size of the buffer indicated by *lpName*, in UTF-16 code points.</span></span> <span data-ttu-id="a9798-128">Um valor de 0 para esse parâmetro faz com que a função ignore o buffer *lpName* e retorne o tamanho do buffer, em caracteres (caracteres nulos incluídos), necessário para conter o nome da localidade pai.</span><span class="sxs-lookup"><span data-stu-id="a9798-128">A value of 0 for this parameter causes the function to ignore the *lpName* buffer and return the size of the buffer, in characters (null characters included), required to contain the parent locale name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9798-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9798-129">Return value</span></span>

<span data-ttu-id="a9798-130">Retorna a contagem de pontos de código UTF-16 no nome da localidade, incluindo o caractere nulo de terminação, se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a9798-130">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span>

<span data-ttu-id="a9798-131">Essa função retornará 0 se não tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="a9798-131">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="a9798-132">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="a9798-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="a9798-133">ERRO \_ de \_ buffer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="a9798-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="a9798-134">Um tamanho de buffer fornecido não era grande o suficiente ou foi definido incorretamente como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a9798-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="a9798-135">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="a9798-135">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="a9798-136">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="a9798-136">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9798-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9798-137">Remarks</span></span>

<span data-ttu-id="a9798-138">O arquivo de cabeçalho e a DLL necessários fazem parte do download "APIs de mapeamento de dados de nível inferior do Microsoft NLS", disponível no [centro de download da Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="a9798-138">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9798-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9798-139">Requirements</span></span>



| <span data-ttu-id="a9798-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9798-140">Requirement</span></span> | <span data-ttu-id="a9798-141">Valor</span><span class="sxs-lookup"><span data-stu-id="a9798-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9798-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9798-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a9798-143">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a9798-143">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a9798-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9798-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a9798-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a9798-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9798-146">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a9798-146">Redistributable</span></span><br/>          | <span data-ttu-id="a9798-147">APIs de mapeamento de dados de nível inferior do Microsoft NLS no Windows XP com SP2 e posterior</span><span class="sxs-lookup"><span data-stu-id="a9798-147">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and later</span></span><br/>  |
| <span data-ttu-id="a9798-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9798-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9798-149"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9798-149"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="a9798-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a9798-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9798-151"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9798-151"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9798-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9798-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9798-153">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="a9798-153">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="a9798-154">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="a9798-154">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="a9798-155">Mapeando dados de localidade</span><span class="sxs-lookup"><span data-stu-id="a9798-155">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="a9798-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="a9798-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
