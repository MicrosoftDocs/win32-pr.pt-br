---
description: Desativa a subclasse do controle especificado.
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Função Ctl3dUnsubclassCtl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnsubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: ec62c2ecab6d8c90a9c9b7b2570bf5d76afd0589
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750527"
---
# <a name="ctl3dunsubclassctl-function"></a><span data-ttu-id="16bf9-103">Função Ctl3dUnsubclassCtl</span><span class="sxs-lookup"><span data-stu-id="16bf9-103">Ctl3dUnsubclassCtl function</span></span>

<span data-ttu-id="16bf9-104">Desativa a subclasse do controle especificado.</span><span class="sxs-lookup"><span data-stu-id="16bf9-104">Turns off subclassing for the specified control.</span></span>

## <a name="syntax"></a><span data-ttu-id="16bf9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16bf9-105">Syntax</span></span>


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="16bf9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16bf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16bf9-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="16bf9-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="16bf9-108">Um identificador para a janela de controle.</span><span class="sxs-lookup"><span data-stu-id="16bf9-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16bf9-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16bf9-109">Return value</span></span>

<span data-ttu-id="16bf9-110">Retornará **true** se o controle tiver uma subclasse com êxito; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="16bf9-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="16bf9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="16bf9-111">Remarks</span></span>

<span data-ttu-id="16bf9-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="16bf9-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="16bf9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16bf9-113">Requirements</span></span>



| <span data-ttu-id="16bf9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="16bf9-114">Requirement</span></span> | <span data-ttu-id="16bf9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="16bf9-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16bf9-116">DLL</span><span class="sxs-lookup"><span data-stu-id="16bf9-116">DLL</span></span><br/> | <dl> <span data-ttu-id="16bf9-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16bf9-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16bf9-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="16bf9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16bf9-119">**Ctl3dSubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="16bf9-119">**Ctl3dSubclassCtl**</span></span>](ctl3dsubclassctl.md)
</dt> </dl>

 

 
