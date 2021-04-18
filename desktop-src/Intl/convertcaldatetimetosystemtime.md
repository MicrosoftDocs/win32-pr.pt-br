---
description: Preterido. Converte uma estrutura CALDATETIME especificada em uma estrutura SYSTEMTIME.
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: Função ConvertCalDateTimeToSystemTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 9c317a31904e2d1b0b2110f6b2dc367ac3e2e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813083"
---
# <a name="convertcaldatetimetosystemtime-function"></a><span data-ttu-id="9f8a6-104">Função ConvertCalDateTimeToSystemTime</span><span class="sxs-lookup"><span data-stu-id="9f8a6-104">ConvertCalDateTimeToSystemTime function</span></span>

<span data-ttu-id="9f8a6-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="9f8a6-105">Deprecated.</span></span> <span data-ttu-id="9f8a6-106">Converte uma estrutura [**CALDATETIME**](caldatetime.md) especificada em uma estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="9f8a6-106">Converts a specified [**CALDATETIME**](caldatetime.md) structure to a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f8a6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f8a6-107">Syntax</span></span>


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a><span data-ttu-id="9f8a6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f8a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f8a6-109">*lpCalDateTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f8a6-109">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f8a6-110">Ponteiro para a estrutura [**CALDATETIME**](caldatetime.md) a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="9f8a6-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="9f8a6-111">*lpSysTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9f8a6-111">*lpSysTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f8a6-112">Ponteiro para a estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) equivalente.</span><span class="sxs-lookup"><span data-stu-id="9f8a6-112">Pointer to the equivalent [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f8a6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f8a6-113">Return value</span></span>

<span data-ttu-id="9f8a6-114">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9f8a6-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="9f8a6-115">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="9f8a6-115">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="9f8a6-116">\_Data \_ de erro fora \_ do \_ intervalo.</span><span class="sxs-lookup"><span data-stu-id="9f8a6-116">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="9f8a6-117">A data especificada estava fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="9f8a6-117">The specified date was out of range.</span></span>
-   <span data-ttu-id="9f8a6-118">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="9f8a6-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="9f8a6-119">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="9f8a6-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f8a6-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f8a6-120">Remarks</span></span>

<span data-ttu-id="9f8a6-121">Essa função não tem um arquivo de cabeçalho ou arquivo de biblioteca associado.</span><span class="sxs-lookup"><span data-stu-id="9f8a6-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="9f8a6-122">O aplicativo pode chamar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Kernel32.dll) para obter um identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="9f8a6-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="9f8a6-123">Em seguida, ele pode chamar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com a alça do módulo e o nome dessa função para obter o endereço da função.</span><span class="sxs-lookup"><span data-stu-id="9f8a6-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f8a6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f8a6-124">Requirements</span></span>



| <span data-ttu-id="9f8a6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f8a6-125">Requirement</span></span> | <span data-ttu-id="9f8a6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9f8a6-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f8a6-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f8a6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9f8a6-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f8a6-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9f8a6-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f8a6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9f8a6-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9f8a6-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9f8a6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9f8a6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f8a6-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f8a6-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f8a6-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f8a6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f8a6-134">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="9f8a6-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="9f8a6-135">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="9f8a6-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="9f8a6-136">Recuperando informações de data e hora</span><span class="sxs-lookup"><span data-stu-id="9f8a6-136">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
