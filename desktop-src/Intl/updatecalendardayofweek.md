---
description: Preterido. Obtém o dia da semana que corresponde a um dia especificado e popula o membro DayOfWeek na estrutura CALDATETIME especificada com esse valor.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: Função UpdateCalendarDayOfWeek
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 316af539e6ca0476f0f8d575a160fcd7c3219e90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780133"
---
# <a name="updatecalendardayofweek-function"></a><span data-ttu-id="ec726-104">Função UpdateCalendarDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="ec726-104">UpdateCalendarDayOfWeek function</span></span>

<span data-ttu-id="ec726-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="ec726-105">Deprecated.</span></span> <span data-ttu-id="ec726-106">Obtém o dia da semana que corresponde a um dia especificado e popula o membro **DayOfWeek** na estrutura [**CALDATETIME**](caldatetime.md) especificada com esse valor.</span><span class="sxs-lookup"><span data-stu-id="ec726-106">Gets the day of the week that corresponds to a specified day and populates the **DayOfWeek** member in the specified [**CALDATETIME**](caldatetime.md) structure with that value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec726-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec726-107">Syntax</span></span>


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="ec726-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec726-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec726-109">*lpCalDateTime* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ec726-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec726-110">Ponteiro para a estrutura [**CALDATETIME**](caldatetime.md) que contém a data para a qual definir o dia da semana.</span><span class="sxs-lookup"><span data-stu-id="ec726-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure containing the date for which to set the day of the week.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec726-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec726-111">Return value</span></span>

<span data-ttu-id="ec726-112">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ec726-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="ec726-113">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="ec726-113">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="ec726-114">\_Data \_ de erro fora \_ do \_ intervalo.</span><span class="sxs-lookup"><span data-stu-id="ec726-114">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="ec726-115">A data especificada estava fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="ec726-115">The specified date was out of range.</span></span>
-   <span data-ttu-id="ec726-116">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="ec726-116">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="ec726-117">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="ec726-117">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec726-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec726-118">Remarks</span></span>

<span data-ttu-id="ec726-119">Essa função não tem um arquivo de cabeçalho ou arquivo de biblioteca associado.</span><span class="sxs-lookup"><span data-stu-id="ec726-119">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="ec726-120">O aplicativo pode chamar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Kernel32.dll) para obter um identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="ec726-120">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="ec726-121">Em seguida, ele pode chamar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse identificador de módulo e o nome dessa função para obter o endereço da função.</span><span class="sxs-lookup"><span data-stu-id="ec726-121">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec726-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec726-122">Requirements</span></span>



| <span data-ttu-id="ec726-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec726-123">Requirement</span></span> | <span data-ttu-id="ec726-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ec726-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec726-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec726-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ec726-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec726-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ec726-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec726-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ec726-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ec726-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec726-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ec726-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec726-130"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec726-130"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec726-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec726-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec726-132">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="ec726-132">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="ec726-133">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="ec726-133">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="ec726-134">**CALDATETIME**</span><span class="sxs-lookup"><span data-stu-id="ec726-134">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
