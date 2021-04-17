---
description: Converte um nome de localidade em um identificador de localidade que pode ser usado para obter informações do sistema operacional.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Função DownlevelLocaleNameToLCID (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748607"
---
# <a name="downlevellocalenametolcid-function"></a><span data-ttu-id="5453a-103">Função DownlevelLocaleNameToLCID</span><span class="sxs-lookup"><span data-stu-id="5453a-103">DownlevelLocaleNameToLCID function</span></span>

<span data-ttu-id="5453a-104">Converte um [nome de localidade](locale-names.md) em um [identificador de localidade](locale-identifiers.md) que pode ser usado para obter informações do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5453a-104">Converts a [locale name](locale-names.md) to a [locale identifier](locale-identifiers.md) that can be used to get information from the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="5453a-105">Essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5453a-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="5453a-106">Seu uso requer um pacote de download.</span><span class="sxs-lookup"><span data-stu-id="5453a-106">Its use requires a download package.</span></span> <span data-ttu-id="5453a-107">Os aplicativos que só são executados no Windows Vista e posterior devem chamar [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) para recuperar um identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="5453a-107">Applications that only run on Windows Vista and later should call [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) to retrieve a locale identifier.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5453a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5453a-108">Syntax</span></span>


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5453a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5453a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5453a-110">*lpName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5453a-110">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5453a-111">Ponteiro para uma cadeia de caracteres terminada em nulo que representa um [nome de localidade](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="5453a-111">Pointer to a null-terminated string representing a [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="5453a-112">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5453a-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5453a-113">Sinalizadores que especificam o tipo de nome.</span><span class="sxs-lookup"><span data-stu-id="5453a-113">Flags specifying the type of name.</span></span> <span data-ttu-id="5453a-114">O padrão é nome de localidade de nível inferior \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5453a-114">The default is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5453a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5453a-115">Return value</span></span>

<span data-ttu-id="5453a-116">Retorna o identificador de localidade que corresponde ao nome da localidade, se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5453a-116">Returns the locale identifier that corresponds to the locale name if successful.</span></span>

<span data-ttu-id="5453a-117">A função retornará 0 se não tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="5453a-117">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="5453a-118">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="5453a-118">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="5453a-119">ERROS de \_ Sinalizadores inválidos \_ .</span><span class="sxs-lookup"><span data-stu-id="5453a-119">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="5453a-120">Os valores fornecidos para sinalizadores não eram válidos.</span><span class="sxs-lookup"><span data-stu-id="5453a-120">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="5453a-121">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="5453a-121">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="5453a-122">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="5453a-122">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="5453a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5453a-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5453a-124">Esta função não oferece suporte a localidades neutras.</span><span class="sxs-lookup"><span data-stu-id="5453a-124">This function does not support neutral locales.</span></span> <span data-ttu-id="5453a-125">A função [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) equivalente dá suporte a [localidades personalizadas](custom-locales.md), mas apenas para o Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="5453a-125">The equivalent [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function supports [custom locales](custom-locales.md), but only for Windows Vista and later.</span></span>

 

<span data-ttu-id="5453a-126">O arquivo de cabeçalho e a DLL necessários fazem parte do download "APIs de mapeamento de dados de nível inferior do Microsoft NLS", disponível no [centro de download da Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="5453a-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="5453a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5453a-127">Requirements</span></span>



| <span data-ttu-id="5453a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5453a-128">Requirement</span></span> | <span data-ttu-id="5453a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5453a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5453a-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5453a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5453a-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5453a-131">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="5453a-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5453a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5453a-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5453a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5453a-134">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5453a-134">Redistributable</span></span><br/>          | <span data-ttu-id="5453a-135">APIs de mapeamento de dados de nível inferior do Microsoft NLS onwindows XP com SP2 e laterorWindows vista</span><span class="sxs-lookup"><span data-stu-id="5453a-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="5453a-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5453a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5453a-137"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5453a-137"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="5453a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5453a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5453a-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5453a-139"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5453a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="5453a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5453a-141">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="5453a-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="5453a-142">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="5453a-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="5453a-143">Mapeando dados de localidade</span><span class="sxs-lookup"><span data-stu-id="5453a-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="5453a-144">**LocaleNameToLCID**</span><span class="sxs-lookup"><span data-stu-id="5453a-144">**LocaleNameToLCID**</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
