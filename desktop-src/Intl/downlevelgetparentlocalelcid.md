---
description: Recupera o identificador de localidade para o pai da localidade fornecida.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Função DownlevelGetParentLocaleLCID (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297278"
---
# <a name="downlevelgetparentlocalelcid-function"></a><span data-ttu-id="cd3dc-103">Função DownlevelGetParentLocaleLCID</span><span class="sxs-lookup"><span data-stu-id="cd3dc-103">DownlevelGetParentLocaleLCID function</span></span>

<span data-ttu-id="cd3dc-104">Recupera o [identificador de localidade](locale-identifiers.md) para o pai da localidade fornecida.</span><span class="sxs-lookup"><span data-stu-id="cd3dc-104">Retrieves the [locale identifier](locale-identifiers.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="cd3dc-105">Essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cd3dc-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="cd3dc-106">Seu uso requer o pacote de download.</span><span class="sxs-lookup"><span data-stu-id="cd3dc-106">Its use requires the download package.</span></span> <span data-ttu-id="cd3dc-107">Os aplicativos que só são executados no Windows Vista e posterior devem chamar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) com *LCTYPE* definido como [localidade \_ SPARENT](locale-sparent.md).</span><span class="sxs-lookup"><span data-stu-id="cd3dc-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cd3dc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd3dc-108">Syntax</span></span>


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a><span data-ttu-id="cd3dc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd3dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd3dc-110">*Localidade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="cd3dc-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd3dc-111">Identificador de localidade da localidade para a qual recuperar o identificador de localidade pai.</span><span class="sxs-lookup"><span data-stu-id="cd3dc-111">Locale identifier of the locale for which to retrieve the parent locale identifier.</span></span> <span data-ttu-id="cd3dc-112">Você pode usar a macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para criar um identificador de localidade ou usar um dos valores predefinidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="cd3dc-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="cd3dc-113">LOCALIDADE \_ invariável</span><span class="sxs-lookup"><span data-stu-id="cd3dc-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="cd3dc-114">\_padrão do sistema de localidade \_</span><span class="sxs-lookup"><span data-stu-id="cd3dc-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="cd3dc-115">\_padrão de usuário de localidade \_</span><span class="sxs-lookup"><span data-stu-id="cd3dc-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="cd3dc-116">**Windows Vista e posterior:** Também há suporte para os seguintes identificadores de localidade personalizados.</span><span class="sxs-lookup"><span data-stu-id="cd3dc-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="cd3dc-117">\_padrão personalizado de localidade \_</span><span class="sxs-lookup"><span data-stu-id="cd3dc-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="cd3dc-118">\_ \_ padrão da interface do usuário personalizada de localidade \_</span><span class="sxs-lookup"><span data-stu-id="cd3dc-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="cd3dc-119">LOCALIDADE \_ personalizada \_ não especificada</span><span class="sxs-lookup"><span data-stu-id="cd3dc-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd3dc-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd3dc-120">Return value</span></span>

<span data-ttu-id="cd3dc-121">Retorna o identificador de localidade pai se for bem-sucedido ou 0 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="cd3dc-121">Returns the parent locale identifier if successful, or 0 otherwise.</span></span> <span data-ttu-id="cd3dc-122">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="cd3dc-122">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="cd3dc-123">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="cd3dc-123">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="cd3dc-124">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="cd3dc-124">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd3dc-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd3dc-125">Remarks</span></span>

<span data-ttu-id="cd3dc-126">O arquivo de cabeçalho e a DLL necessários fazem parte do download "APIs de mapeamento de dados de nível inferior do Microsoft NLS", disponível no [centro de download da Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="cd3dc-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd3dc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd3dc-127">Requirements</span></span>



| <span data-ttu-id="cd3dc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd3dc-128">Requirement</span></span> | <span data-ttu-id="cd3dc-129">Valor</span><span class="sxs-lookup"><span data-stu-id="cd3dc-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd3dc-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd3dc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cd3dc-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cd3dc-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cd3dc-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd3dc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cd3dc-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd3dc-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd3dc-134">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="cd3dc-134">Redistributable</span></span><br/>          | <span data-ttu-id="cd3dc-135">APIs de mapeamento de dados de nível inferior do Microsoft NLS onwindows XPor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd3dc-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XPor Windows Vista</span></span><br/>     |
| <span data-ttu-id="cd3dc-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd3dc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd3dc-137"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd3dc-137"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="cd3dc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cd3dc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd3dc-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd3dc-139"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd3dc-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd3dc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd3dc-141">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="cd3dc-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="cd3dc-142">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="cd3dc-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="cd3dc-143">Mapeando dados de localidade</span><span class="sxs-lookup"><span data-stu-id="cd3dc-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="cd3dc-144">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="cd3dc-144">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
