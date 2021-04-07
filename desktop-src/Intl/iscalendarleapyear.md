---
description: Preterido. Identifica se o ano especificado é um ano bissexto dentro da era determinada para o calendário específico.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: Função IsCalendarLeapYear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 484531f8107bacb70f9e24ba2537090317825e26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828575"
---
# <a name="iscalendarleapyear-function"></a><span data-ttu-id="314f7-104">Função IsCalendarLeapYear</span><span class="sxs-lookup"><span data-stu-id="314f7-104">IsCalendarLeapYear function</span></span>

<span data-ttu-id="314f7-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="314f7-105">Deprecated.</span></span> <span data-ttu-id="314f7-106">Identifica se o ano especificado é um ano bissexto dentro da era determinada para o calendário específico.</span><span class="sxs-lookup"><span data-stu-id="314f7-106">Identifies whether the specified year is a leap year within the given era for the specific calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="314f7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="314f7-107">Syntax</span></span>


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a><span data-ttu-id="314f7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="314f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="314f7-109">*calId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="314f7-109">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314f7-110">O [identificador de calendário](calendar-identifiers.md) a ser usado para verificar o ano bissexto.</span><span class="sxs-lookup"><span data-stu-id="314f7-110">The [calendar identifier](calendar-identifiers.md) to use for checking leap year.</span></span>

</dd> <dt>

<span data-ttu-id="314f7-111">*ano* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="314f7-111">*year* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314f7-112">O ano a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="314f7-112">The year to check.</span></span>

</dd> <dt>

<span data-ttu-id="314f7-113">*era* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="314f7-113">*era* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314f7-114">A era a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="314f7-114">The era to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="314f7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="314f7-115">Return value</span></span>

<span data-ttu-id="314f7-116">Retornará **true** se o ano especificado for um ano bissexto ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="314f7-116">Returns **TRUE** if the specified year is a leap year, or **FALSE** otherwise.</span></span> <span data-ttu-id="314f7-117">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="314f7-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="314f7-118">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="314f7-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="314f7-119">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="314f7-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="314f7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="314f7-120">Remarks</span></span>

<span data-ttu-id="314f7-121">Essa função não tem um arquivo de cabeçalho ou arquivo de biblioteca associado.</span><span class="sxs-lookup"><span data-stu-id="314f7-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="314f7-122">O aplicativo pode chamar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Kernel32.dll) para obter um identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="314f7-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="314f7-123">Em seguida, ele pode chamar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse identificador de módulo e o nome dessa função para obter o endereço da função.</span><span class="sxs-lookup"><span data-stu-id="314f7-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="314f7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="314f7-124">Requirements</span></span>



| <span data-ttu-id="314f7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="314f7-125">Requirement</span></span> | <span data-ttu-id="314f7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="314f7-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="314f7-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="314f7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="314f7-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="314f7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="314f7-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="314f7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="314f7-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="314f7-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="314f7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="314f7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="314f7-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="314f7-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="314f7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="314f7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314f7-134">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="314f7-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="314f7-135">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="314f7-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> </dl>

 

 
