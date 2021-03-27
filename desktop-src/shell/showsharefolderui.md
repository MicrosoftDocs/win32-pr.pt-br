---
description: Exibe a guia compartilhamento de pasta na folha de propriedades da pasta especificada.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: Função ShowShareFolderUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296934"
---
# <a name="showsharefolderui-function"></a><span data-ttu-id="14098-103">Função ShowShareFolderUI</span><span class="sxs-lookup"><span data-stu-id="14098-103">ShowShareFolderUI function</span></span>

<span data-ttu-id="14098-104">Exibe a guia **compartilhamento de pasta** na folha de propriedades da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="14098-104">Displays the **Folder Sharing** tab on the properties sheet for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="14098-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14098-105">Syntax</span></span>


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="14098-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14098-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14098-107">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14098-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14098-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="14098-108">Type: **HWND**</span></span>

<span data-ttu-id="14098-109">Um identificador para a janela pai da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="14098-109">A handle to the parent window for the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="14098-110">*pszPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14098-110">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14098-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="14098-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="14098-112">Um ponteiro para uma cadeia de caracteres que especifica o caminho para a pasta que exibe sua guia de **compartilhamento de pasta** .</span><span class="sxs-lookup"><span data-stu-id="14098-112">A pointer to a string that specifies the path to the folder that displays its **Folder Sharing** tab.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14098-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14098-113">Return value</span></span>

<span data-ttu-id="14098-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="14098-114">Type: **HRESULT**</span></span>

<span data-ttu-id="14098-115">Essa função sempre retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="14098-115">This function always returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="14098-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="14098-116">Remarks</span></span>

<span data-ttu-id="14098-117">Esta função não tem nenhum arquivo. lib associado.</span><span class="sxs-lookup"><span data-stu-id="14098-117">This function has no associated .lib file.</span></span> <span data-ttu-id="14098-118">Você deve usar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usá-lo.</span><span class="sxs-lookup"><span data-stu-id="14098-118">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="14098-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14098-119">Requirements</span></span>



| <span data-ttu-id="14098-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="14098-120">Requirement</span></span> | <span data-ttu-id="14098-121">Valor</span><span class="sxs-lookup"><span data-stu-id="14098-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14098-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14098-122">Minimum supported client</span></span><br/> | <span data-ttu-id="14098-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="14098-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="14098-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14098-124">Minimum supported server</span></span><br/> | <span data-ttu-id="14098-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14098-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="14098-126">DLL</span><span class="sxs-lookup"><span data-stu-id="14098-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14098-127"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14098-127"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="14098-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="14098-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="14098-129">**ShowShareFolderUIW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="14098-129">**ShowShareFolderUIW** (Unicode)</span></span><br/>                                            |



## <a name="see-also"></a><span data-ttu-id="14098-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="14098-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14098-131">**CanShareFolderW**</span><span class="sxs-lookup"><span data-stu-id="14098-131">**CanShareFolderW**</span></span>](cansharefolderw.md)
</dt> </dl>

 

 
