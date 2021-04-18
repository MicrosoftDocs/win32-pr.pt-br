---
description: Preterido. Ajusta uma data por um número especificado de anos, meses, semanas ou dias.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: Função AdjustCalendarDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: ce2f61fd7d7d6354130873b5b2b2376c856e3958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810487"
---
# <a name="adjustcalendardate-function"></a><span data-ttu-id="b3073-104">Função AdjustCalendarDate</span><span class="sxs-lookup"><span data-stu-id="b3073-104">AdjustCalendarDate function</span></span>

<span data-ttu-id="b3073-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="b3073-105">Deprecated.</span></span> <span data-ttu-id="b3073-106">Ajusta uma data por um número especificado de anos, meses, semanas ou dias.</span><span class="sxs-lookup"><span data-stu-id="b3073-106">Adjusts a date by a specified number of years, months, weeks, or days.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3073-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3073-107">Syntax</span></span>


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a><span data-ttu-id="b3073-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3073-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3073-109">*lpCalDateTime* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b3073-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3073-110">Ponteiro para uma estrutura [**CALDATETIME**](caldatetime.md) que contém as informações de data e calendário a serem ajustadas.</span><span class="sxs-lookup"><span data-stu-id="b3073-110">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to adjust.</span></span>

</dd> <dt>

<span data-ttu-id="b3073-111">*calUnit* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3073-111">*calUnit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3073-112">O valor de enumeração [**CALDATETIME \_ DATEUNIT**](caldatetime-dateunit.md) que indica a unidade de data, por exemplo, DayUnit.</span><span class="sxs-lookup"><span data-stu-id="b3073-112">The [**CALDATETIME\_DATEUNIT**](caldatetime-dateunit.md) enumeration value indicating the date unit, for example, DayUnit.</span></span>

</dd> <dt>

<span data-ttu-id="b3073-113">*valor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b3073-113">*amount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3073-114">O valor pelo qual ajustar a data especificada.</span><span class="sxs-lookup"><span data-stu-id="b3073-114">The amount by which to adjust the specified date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3073-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3073-115">Return value</span></span>

<span data-ttu-id="b3073-116">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b3073-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="b3073-117">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="b3073-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="b3073-118">\_Data \_ de erro fora \_ do \_ intervalo.</span><span class="sxs-lookup"><span data-stu-id="b3073-118">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="b3073-119">A data especificada estava fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="b3073-119">The specified date was out of range.</span></span>
-   <span data-ttu-id="b3073-120">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="b3073-120">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="b3073-121">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="b3073-121">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3073-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3073-122">Remarks</span></span>

<span data-ttu-id="b3073-123">Essa função não tem um arquivo de cabeçalho ou arquivo de biblioteca associado.</span><span class="sxs-lookup"><span data-stu-id="b3073-123">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="b3073-124">O aplicativo pode chamar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Kernel32.dll) para obter um identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="b3073-124">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="b3073-125">Em seguida, ele pode chamar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com a alça do módulo e o nome dessa função para obter o endereço da função.</span><span class="sxs-lookup"><span data-stu-id="b3073-125">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3073-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3073-126">Requirements</span></span>



| <span data-ttu-id="b3073-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3073-127">Requirement</span></span> | <span data-ttu-id="b3073-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b3073-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3073-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3073-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b3073-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3073-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b3073-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3073-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b3073-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3073-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3073-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b3073-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3073-134"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3073-134"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3073-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3073-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3073-136">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="b3073-136">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="b3073-137">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="b3073-137">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="b3073-138">NLS: exemplo de APIs baseadas em nome</span><span class="sxs-lookup"><span data-stu-id="b3073-138">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
