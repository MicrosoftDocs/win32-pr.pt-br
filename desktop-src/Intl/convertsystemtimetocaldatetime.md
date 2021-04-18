---
description: Preterido. Converte uma estrutura SYSTEMTIME especificada em uma estrutura CALDATETIME.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: Função ConvertSystemTimeToCalDateTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 738899c7307797f0edeade93f7e4e706919be900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752673"
---
# <a name="convertsystemtimetocaldatetime-function"></a><span data-ttu-id="6dccf-104">Função ConvertSystemTimeToCalDateTime</span><span class="sxs-lookup"><span data-stu-id="6dccf-104">ConvertSystemTimeToCalDateTime function</span></span>

<span data-ttu-id="6dccf-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="6dccf-105">Deprecated.</span></span> <span data-ttu-id="6dccf-106">Converte uma estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) especificada em uma estrutura [**CALDATETIME**](caldatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="6dccf-106">Converts a specified [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to a [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dccf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6dccf-107">Syntax</span></span>


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a><span data-ttu-id="6dccf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dccf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dccf-109">*lpSysTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6dccf-109">*lpSysTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dccf-110">Ponteiro para a estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="6dccf-110">Pointer to the [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="6dccf-111">*calId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6dccf-111">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dccf-112">O [identificador de calendário](calendar-identifiers.md) do sistema a ser usado na conversão.</span><span class="sxs-lookup"><span data-stu-id="6dccf-112">The system [calendar identifier](calendar-identifiers.md) to use in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="6dccf-113">*lpCalDateTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6dccf-113">*lpCalDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dccf-114">Ponteiro para a estrutura [**CALDATETIME**](caldatetime.md) equivalente.</span><span class="sxs-lookup"><span data-stu-id="6dccf-114">Pointer to the equivalent [**CALDATETIME**](caldatetime.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dccf-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6dccf-115">Return value</span></span>

<span data-ttu-id="6dccf-116">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6dccf-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="6dccf-117">Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="6dccf-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="6dccf-118">\_parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="6dccf-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="6dccf-119">Qualquer um dos valores de parâmetro era inválido.</span><span class="sxs-lookup"><span data-stu-id="6dccf-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dccf-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6dccf-120">Remarks</span></span>

<span data-ttu-id="6dccf-121">A data mais antiga com suporte nesta função é 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="6dccf-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="6dccf-122">Essa função não tem um arquivo de cabeçalho ou arquivo de biblioteca associado.</span><span class="sxs-lookup"><span data-stu-id="6dccf-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="6dccf-123">O aplicativo pode chamar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Kernel32.dll) para obter um identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="6dccf-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="6dccf-124">Em seguida, ele pode chamar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com a alça do módulo e o nome dessa função para obter o endereço da função.</span><span class="sxs-lookup"><span data-stu-id="6dccf-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dccf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dccf-125">Requirements</span></span>



| <span data-ttu-id="6dccf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dccf-126">Requirement</span></span> | <span data-ttu-id="6dccf-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6dccf-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dccf-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dccf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6dccf-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6dccf-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6dccf-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dccf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6dccf-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6dccf-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6dccf-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6dccf-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dccf-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dccf-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dccf-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dccf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dccf-135">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="6dccf-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="6dccf-136">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="6dccf-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="6dccf-137">Recuperando informações de data e hora</span><span class="sxs-lookup"><span data-stu-id="6dccf-137">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
