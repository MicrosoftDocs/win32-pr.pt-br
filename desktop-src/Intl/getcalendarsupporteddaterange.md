---
description: Preterido. Obtém o intervalo de datas com suporte para um calendário especificado.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: Função GetCalendarSupportedDateRange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 57b1175ef7bcf5b6b5d91af63682ca565bc0f1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922146"
---
# <a name="getcalendarsupporteddaterange-function"></a><span data-ttu-id="f8911-104">Função GetCalendarSupportedDateRange</span><span class="sxs-lookup"><span data-stu-id="f8911-104">GetCalendarSupportedDateRange function</span></span>

<span data-ttu-id="f8911-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="f8911-105">Deprecated.</span></span> <span data-ttu-id="f8911-106">Obtém o intervalo de datas com suporte para um calendário especificado.</span><span class="sxs-lookup"><span data-stu-id="f8911-106">Gets the supported date range for a specified calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8911-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8911-107">Syntax</span></span>


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="f8911-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8911-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8911-109">*Calendário* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f8911-109">*Calendar* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8911-110">[Identificador de calendário](calendar-identifiers.md) para o qual obter o intervalo de datas com suporte.</span><span class="sxs-lookup"><span data-stu-id="f8911-110">[Calendar identifier](calendar-identifiers.md) for which to get the supported date range.</span></span>

</dd> <dt>

<span data-ttu-id="f8911-111">*lpCalMinDateTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f8911-111">*lpCalMinDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8911-112">Ponteiro para uma estrutura [**CALDATETIME**](caldatetime.md) que define a data mínima com suporte.</span><span class="sxs-lookup"><span data-stu-id="f8911-112">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the minimum supported date.</span></span>

</dd> <dt>

<span data-ttu-id="f8911-113">*lpCalMaxDateTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f8911-113">*lpCalMaxDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8911-114">Ponteiro para uma estrutura [**CALDATETIME**](caldatetime.md) que define a data máxima com suporte.</span><span class="sxs-lookup"><span data-stu-id="f8911-114">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the maximum supported date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8911-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8911-115">Return value</span></span>

<span data-ttu-id="f8911-116">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f8911-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="f8911-117">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="f8911-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="f8911-118">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="f8911-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="f8911-119">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="f8911-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8911-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8911-120">Remarks</span></span>

<span data-ttu-id="f8911-121">A data mais antiga com suporte nesta função é 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="f8911-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="f8911-122">Essa função não tem um arquivo de cabeçalho ou arquivo de biblioteca associado.</span><span class="sxs-lookup"><span data-stu-id="f8911-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="f8911-123">O aplicativo pode chamar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Kernel32.dll) para obter um identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="f8911-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="f8911-124">Em seguida, ele pode chamar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com a alça do módulo e o nome dessa função para obter o endereço da função.</span><span class="sxs-lookup"><span data-stu-id="f8911-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8911-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8911-125">Requirements</span></span>



| <span data-ttu-id="f8911-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8911-126">Requirement</span></span> | <span data-ttu-id="f8911-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f8911-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8911-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8911-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f8911-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8911-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f8911-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8911-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f8911-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8911-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f8911-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f8911-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8911-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8911-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8911-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8911-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8911-135">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="f8911-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="f8911-136">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="f8911-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="f8911-137">NLS: exemplo de APIs baseadas em nome</span><span class="sxs-lookup"><span data-stu-id="f8911-137">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
