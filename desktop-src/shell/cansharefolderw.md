---
description: Usado para determinar se a opção compartilhar esta pasta deve ser mostrada na exibição da Web.
title: Função CanShareFolderW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: cf7d0feb31666f3a918c0307a0b0983bff246fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501439"
---
# <a name="cansharefolderw-function"></a><span data-ttu-id="5f77d-103">Função CanShareFolderW</span><span class="sxs-lookup"><span data-stu-id="5f77d-103">CanShareFolderW function</span></span>

<span data-ttu-id="5f77d-104">\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5f77d-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="5f77d-105">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5f77d-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="5f77d-106">Usado para determinar se a opção **compartilhar esta pasta** deve ser mostrada na exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="5f77d-106">Used to determine whether to show the **Share this folder** option in web view.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f77d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f77d-107">Syntax</span></span>


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="5f77d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f77d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f77d-109">*pszPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f77d-109">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f77d-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="5f77d-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="5f77d-111">Um ponteiro para uma cadeia de caracteres que especifica o caminho da pasta a ser testada.</span><span class="sxs-lookup"><span data-stu-id="5f77d-111">A pointer to a string that specifies the path of the folder to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f77d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f77d-112">Return value</span></span>

<span data-ttu-id="5f77d-113">Tipo: **STDAPI**</span><span class="sxs-lookup"><span data-stu-id="5f77d-113">Type: **STDAPI**</span></span>

<span data-ttu-id="5f77d-114">Os valores de retorno incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="5f77d-114">Return values include the following.</span></span>



| <span data-ttu-id="5f77d-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5f77d-115">Return code/value</span></span>                                                                        | <span data-ttu-id="5f77d-116">Description</span><span class="sxs-lookup"><span data-stu-id="5f77d-116">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f77d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5f77d-117"><dt>**S\_OK**</dt></span></span> </dl>     | <span data-ttu-id="5f77d-118">O caminho apontado por *pszPath* especifica uma pasta que pode ser compartilhada.</span><span class="sxs-lookup"><span data-stu-id="5f77d-118">The path pointed to by *pszPath* specifies a folder that can be shared.</span></span><br/>    |
| <dl> <span data-ttu-id="5f77d-119"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="5f77d-119"><dt>**S\_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="5f77d-120">O caminho apontado por *pszPath* especifica uma pasta que não pode ser compartilhada.</span><span class="sxs-lookup"><span data-stu-id="5f77d-120">The path pointed to by *pszPath* specifies a folder that cannot be shared.</span></span><br/> |
| <dl> <span data-ttu-id="5f77d-121"><dt>Erro HRESULT</dt></span><span class="sxs-lookup"><span data-stu-id="5f77d-121"><dt>HRESULT error</dt></span></span> </dl> | <span data-ttu-id="5f77d-122">Ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="5f77d-122">An error has occurred.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="5f77d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f77d-123">Remarks</span></span>

<span data-ttu-id="5f77d-124">Esta função não tem nenhum arquivo. lib associado.</span><span class="sxs-lookup"><span data-stu-id="5f77d-124">This function has no associated .lib file.</span></span> <span data-ttu-id="5f77d-125">Você deve usar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usá-lo.</span><span class="sxs-lookup"><span data-stu-id="5f77d-125">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f77d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f77d-126">Requirements</span></span>



| <span data-ttu-id="5f77d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f77d-127">Requirement</span></span> | <span data-ttu-id="5f77d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5f77d-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f77d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f77d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5f77d-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5f77d-130">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5f77d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f77d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5f77d-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5f77d-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5f77d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5f77d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f77d-134"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f77d-134"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="5f77d-135">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5f77d-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5f77d-136">**CanShareFolderW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="5f77d-136">**CanShareFolderW** (Unicode)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="5f77d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f77d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f77d-138">**ShowShareFolderUI**</span><span class="sxs-lookup"><span data-stu-id="5f77d-138">**ShowShareFolderUI**</span></span>](./showsharefolderui.md)
</dt> </dl>

 

 
