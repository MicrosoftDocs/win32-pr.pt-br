---
description: Envia uma cadeia de caracteres Unicode para o depurador para exibição.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Função OutputDebugStringWrapW (Shlwapip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989018"
---
# <a name="outputdebugstringwrapw-function"></a><span data-ttu-id="970d9-103">Função OutputDebugStringWrapW</span><span class="sxs-lookup"><span data-stu-id="970d9-103">OutputDebugStringWrapW function</span></span>

<span data-ttu-id="970d9-104">\[Essa função está disponível para uso no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="970d9-104">\[This function is available for use in Windows XP.</span></span> <span data-ttu-id="970d9-105">Ele pode não estar disponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="970d9-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="970d9-106">Use [**OutputDebugStringWna**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) em seu lugar.\]</span><span class="sxs-lookup"><span data-stu-id="970d9-106">Use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in its place.\]</span></span>

<span data-ttu-id="970d9-107">Envia uma cadeia de caracteres Unicode para o depurador para exibição.</span><span class="sxs-lookup"><span data-stu-id="970d9-107">Sends a Unicode string to the debugger for display.</span></span>

> [!Note]  
> <span data-ttu-id="970d9-108">**OutputDebugStringWrapW** é um wrapper para a função **OutputDebugStringWna** .</span><span class="sxs-lookup"><span data-stu-id="970d9-108">**OutputDebugStringWrapW** is a wrapper for the **OutputDebugStringW** function.</span></span> <span data-ttu-id="970d9-109">Consulte a página [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) para ver mais observações de uso.</span><span class="sxs-lookup"><span data-stu-id="970d9-109">See the [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="970d9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="970d9-110">Syntax</span></span>


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a><span data-ttu-id="970d9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="970d9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="970d9-112">*lpOutputString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="970d9-112">*lpOutputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="970d9-113">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="970d9-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="970d9-114">Um ponteiro para a cadeia de caracteres Unicode terminada em nulo a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="970d9-114">A pointer to the null-terminated Unicode string to be displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="970d9-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="970d9-115">Return value</span></span>

<span data-ttu-id="970d9-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="970d9-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="970d9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="970d9-117">Remarks</span></span>

<span data-ttu-id="970d9-118">O **OutputDebugStringWrapW** fornece a capacidade de usar cadeias de caracteres Unicode em sistemas operacionais anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="970d9-118">**OutputDebugStringWrapW** provides the ability to use Unicode strings in operating systems prior to Windows XP.</span></span> <span data-ttu-id="970d9-119">O método preferencial é usar [**OutputDebugStringWna**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) em conjunto com a camada Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="970d9-119">The preferred method is to use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="970d9-120">**OutputDebugStringWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 115.</span><span class="sxs-lookup"><span data-stu-id="970d9-120">**OutputDebugStringWrapW** must be called directly from Shlwapi.dll, using ordinal 115.</span></span>

<span data-ttu-id="970d9-121">Se o aplicativo não tiver um depurador, o depurador do sistema exibirá a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="970d9-121">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="970d9-122">Se o aplicativo não tiver um depurador e o depurador do sistema não estiver ativo, o **OutputDebugStringWrapW** não fará nada.</span><span class="sxs-lookup"><span data-stu-id="970d9-122">If the application has no debugger and the system debugger is not active, **OutputDebugStringWrapW** does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="970d9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="970d9-123">Requirements</span></span>



| <span data-ttu-id="970d9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="970d9-124">Requirement</span></span> | <span data-ttu-id="970d9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="970d9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="970d9-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="970d9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="970d9-127">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="970d9-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="970d9-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="970d9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="970d9-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="970d9-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="970d9-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="970d9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="970d9-131"><dt>Shlwapip. h</dt></span><span class="sxs-lookup"><span data-stu-id="970d9-131"><dt>Shlwapip.h</dt></span></span> </dl>                         |
| <span data-ttu-id="970d9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="970d9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="970d9-133"><dt>Shlwapi.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="970d9-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="970d9-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="970d9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="970d9-135">**OutputDebugString**</span><span class="sxs-lookup"><span data-stu-id="970d9-135">**OutputDebugString**</span></span>](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
