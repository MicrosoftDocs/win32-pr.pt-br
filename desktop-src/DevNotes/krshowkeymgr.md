---
description: Abre a caixa de diálogo do Gerenciador de chaves na interface do usuário.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: Função KRShowKeyMgr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748355"
---
# <a name="krshowkeymgr-function"></a><span data-ttu-id="7056b-103">Função KRShowKeyMgr</span><span class="sxs-lookup"><span data-stu-id="7056b-103">KRShowKeyMgr function</span></span>

<span data-ttu-id="7056b-104">\[Essa função está incluída apenas no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7056b-104">\[This function is included only in Windows XP.</span></span> <span data-ttu-id="7056b-105">No momento, ele não está incluído em nenhuma outra versão do Windows, nem é esperado que ele seja incluído em versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7056b-105">It is not currently included in any other version of Windows, nor is it expected to be included in any future versions of Windows.\]</span></span>

<span data-ttu-id="7056b-106">Abre a caixa de diálogo do Gerenciador de chaves na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7056b-106">Brings up the key manager dialog into the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7056b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7056b-107">Syntax</span></span>


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="7056b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7056b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7056b-109">*hwParent*</span><span class="sxs-lookup"><span data-stu-id="7056b-109">*hwParent*</span></span> 
</dt> <dd>

<span data-ttu-id="7056b-110">Um identificador para a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7056b-110">A handle to the parent window of the dialog.</span></span> <span data-ttu-id="7056b-111">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7056b-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7056b-112">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="7056b-112">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="7056b-113">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7056b-113">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7056b-114">*pszCmdLine*</span><span class="sxs-lookup"><span data-stu-id="7056b-114">*pszCmdLine*</span></span> 
</dt> <dd>

<span data-ttu-id="7056b-115">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7056b-115">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7056b-116">*CmdShow*</span><span class="sxs-lookup"><span data-stu-id="7056b-116">*CmdShow*</span></span> 
</dt> <dd>

<span data-ttu-id="7056b-117">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7056b-117">This parameter is not used and should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7056b-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7056b-118">Return value</span></span>

<span data-ttu-id="7056b-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7056b-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7056b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="7056b-120">Remarks</span></span>

<span data-ttu-id="7056b-121">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7056b-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7056b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7056b-122">Requirements</span></span>



| <span data-ttu-id="7056b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7056b-123">Requirement</span></span> | <span data-ttu-id="7056b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7056b-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7056b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7056b-125">DLL</span></span><br/> | <dl> <span data-ttu-id="7056b-126"><dt>Keymgr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7056b-126"><dt>Keymgr.dll</dt></span></span> </dl> |



 

 
