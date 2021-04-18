---
description: Subclasses de um controle individual, a menos que o controle seja exibido em uma caixa de diálogo.
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Função Ctl3dSubclassCtl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 0ff6c6744c4ddda203149981218b8143fb78bce7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749510"
---
# <a name="ctl3dsubclassctl-function"></a><span data-ttu-id="d6880-103">Função Ctl3dSubclassCtl</span><span class="sxs-lookup"><span data-stu-id="d6880-103">Ctl3dSubclassCtl function</span></span>

<span data-ttu-id="d6880-104">Subclasses de um controle individual, a menos que o controle seja exibido em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d6880-104">Subclasses an individual control unless the control appears in a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6880-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6880-105">Syntax</span></span>


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="d6880-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6880-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6880-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d6880-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d6880-108">Um identificador para a janela de controle.</span><span class="sxs-lookup"><span data-stu-id="d6880-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6880-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6880-109">Return value</span></span>

<span data-ttu-id="d6880-110">Retornará **true** se o controle tiver uma subclasse com êxito; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="d6880-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6880-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6880-111">Remarks</span></span>

<span data-ttu-id="d6880-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d6880-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6880-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6880-113">Requirements</span></span>



| <span data-ttu-id="d6880-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6880-114">Requirement</span></span> | <span data-ttu-id="d6880-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d6880-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6880-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d6880-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d6880-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6880-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6880-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6880-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6880-119">**Ctl3dUnsubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="d6880-119">**Ctl3dUnsubclassCtl**</span></span>](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
