---
description: Determina o local de um recurso com o tipo e o nome especificados no módulo especificado.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: Função FindResourceWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169446"
---
# <a name="findresourcewrapw-function"></a><span data-ttu-id="41c7d-103">Função FindResourceWrapW</span><span class="sxs-lookup"><span data-stu-id="41c7d-103">FindResourceWrapW function</span></span>

<span data-ttu-id="41c7d-104">\[O **FindResourceWrapW** está disponível para uso no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="41c7d-104">\[**FindResourceWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="41c7d-105">Ele pode não estar disponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="41c7d-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="41c7d-106">Em vez disso, você deve usar [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) .\]</span><span class="sxs-lookup"><span data-stu-id="41c7d-106">You should use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) instead.\]</span></span>

<span data-ttu-id="41c7d-107">Determina o local de um recurso com o tipo e o nome especificados no módulo especificado.</span><span class="sxs-lookup"><span data-stu-id="41c7d-107">Determines the location of a resource with the specified type and name, in the specified module.</span></span>

> [!Note]  
> <span data-ttu-id="41c7d-108">**FindResourceWrapW** é um wrapper para a função **FindResourceW** .</span><span class="sxs-lookup"><span data-stu-id="41c7d-108">**FindResourceWrapW** is a wrapper for the **FindResourceW** function.</span></span> <span data-ttu-id="41c7d-109">Consulte [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) para ver mais observações de uso.</span><span class="sxs-lookup"><span data-stu-id="41c7d-109">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="41c7d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41c7d-110">Syntax</span></span>


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a><span data-ttu-id="41c7d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41c7d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41c7d-112">*HMODULE* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41c7d-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c7d-113">Tipo: **HMODULE**</span><span class="sxs-lookup"><span data-stu-id="41c7d-113">Type: **HMODULE**</span></span>

<span data-ttu-id="41c7d-114">Um identificador para o módulo cujo arquivo executável contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="41c7d-114">A handle to the module whose executable file contains the resource.</span></span> <span data-ttu-id="41c7d-115">Um valor **NULL** especifica o identificador de módulo associado ao arquivo de imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="41c7d-115">A value of **NULL** specifies the module handle associated with the image file that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="41c7d-116">*lpName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41c7d-116">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c7d-117">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="41c7d-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="41c7d-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="41c7d-118">The name of the resource.</span></span> <span data-ttu-id="41c7d-119">Para obter mais informações, consulte [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="41c7d-119">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="41c7d-120">*lpType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41c7d-120">*lpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c7d-121">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="41c7d-121">Type: **LPCWSTR**</span></span>

<span data-ttu-id="41c7d-122">Um ponteiro para uma cadeia de caracteres que especifica o tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="41c7d-122">A pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="41c7d-123">Para obter mais informações, consulte [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="41c7d-123">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41c7d-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41c7d-124">Return value</span></span>

<span data-ttu-id="41c7d-125">Tipo: **HRSRC**</span><span class="sxs-lookup"><span data-stu-id="41c7d-125">Type: **HRSRC**</span></span>

<span data-ttu-id="41c7d-126">Se a função for realizada com sucesso, o valor de retorno será um identificador para o bloco de informações do recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="41c7d-126">If the function succeeds, the return value is a handle to the specified resource's information block.</span></span> <span data-ttu-id="41c7d-127">Para obter um identificador para o recurso, passe esse identificador para a função [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .</span><span class="sxs-lookup"><span data-stu-id="41c7d-127">To obtain a handle to the resource, pass this handle to the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

<span data-ttu-id="41c7d-128">Se a função falhar, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="41c7d-128">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="41c7d-129">Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="41c7d-129">To get extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="41c7d-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="41c7d-130">Remarks</span></span>

<span data-ttu-id="41c7d-131">Se você precisar especificar uma localização específica, use a função [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) em vez de **FindResourceWrapW**.</span><span class="sxs-lookup"><span data-stu-id="41c7d-131">If you need to specify a particular localization, use the [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) function rather than **FindResourceWrapW**.</span></span>

<span data-ttu-id="41c7d-132">O **FindResourceWrapW** fornece a capacidade de usar cadeias de caracteres Unicode em sistemas operacionais mais antigos.</span><span class="sxs-lookup"><span data-stu-id="41c7d-132">**FindResourceWrapW** provides the ability to use Unicode strings in older operating systems.</span></span> <span data-ttu-id="41c7d-133">O método preferencial é usar [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) em conjunto com a camada Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="41c7d-133">The preferred method is to use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="41c7d-134">**FindResourceWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 66.</span><span class="sxs-lookup"><span data-stu-id="41c7d-134">**FindResourceWrapW** must be called directly from Shlwapi.dll, using ordinal 66.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c7d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41c7d-135">Requirements</span></span>



| <span data-ttu-id="41c7d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c7d-136">Requirement</span></span> | <span data-ttu-id="41c7d-137">Valor</span><span class="sxs-lookup"><span data-stu-id="41c7d-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41c7d-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41c7d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="41c7d-139">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="41c7d-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41c7d-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41c7d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="41c7d-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41c7d-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="41c7d-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41c7d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="41c7d-143"><dt>Nenhum</dt></span><span class="sxs-lookup"><span data-stu-id="41c7d-143"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="41c7d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="41c7d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41c7d-145"><dt>Shlwapi.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="41c7d-145"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="41c7d-146">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="41c7d-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="41c7d-147">**FindResourceWrapW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="41c7d-147">**FindResourceWrapW** (Unicode)</span></span><br/>                                                                    |



## <a name="see-also"></a><span data-ttu-id="41c7d-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="41c7d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c7d-149">**FindResource**</span><span class="sxs-lookup"><span data-stu-id="41c7d-149">**FindResource**</span></span>](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
