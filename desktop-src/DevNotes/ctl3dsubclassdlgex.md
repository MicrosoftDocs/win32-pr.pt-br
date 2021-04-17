---
description: Subclasses todos os controles em uma caixa de diálogo e na janela da caixa de diálogo.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Função Ctl3dSubclassDlgEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 6e29f65d5ddc3d0d9a7de05eef88b7a662e0e43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749530"
---
# <a name="ctl3dsubclassdlgex-function"></a><span data-ttu-id="6fb46-103">Função Ctl3dSubclassDlgEx</span><span class="sxs-lookup"><span data-stu-id="6fb46-103">Ctl3dSubclassDlgEx function</span></span>

<span data-ttu-id="6fb46-104">Subclasses todos os controles em uma caixa de diálogo e na janela da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6fb46-104">Subclasses all controls in a dialog box and in the dialog window itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb46-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fb46-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a><span data-ttu-id="6fb46-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fb46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fb46-107">*hwndDlg*</span><span class="sxs-lookup"><span data-stu-id="6fb46-107">*hwndDlg*</span></span> 
</dt> <dd>

<span data-ttu-id="6fb46-108">Um identificador para a janela da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6fb46-108">A handle to the dialog window.</span></span>

</dd> <dt>

<span data-ttu-id="6fb46-109">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6fb46-109">*grbit*</span></span> 
</dt> <dd>

<span data-ttu-id="6fb46-110">Os tipos de controle a serem subclasses.</span><span class="sxs-lookup"><span data-stu-id="6fb46-110">The control types to be subclassed.</span></span> <span data-ttu-id="6fb46-111">Esse valor pode ser qualquer um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="6fb46-111">This value can be any of the following.</span></span>



| <span data-ttu-id="6fb46-112">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb46-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="6fb46-113">Significado</span><span class="sxs-lookup"><span data-stu-id="6fb46-113">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <span data-ttu-id="6fb46-114"><dt>**CTL3D \_**</dt> <dt>0X0001</dt> de botões</span><span class="sxs-lookup"><span data-stu-id="6fb46-114"><dt>**CTL3D\_BUTTONS**</dt> <dt>0x0001</dt></span></span> </dl>                 | <span data-ttu-id="6fb46-115">Botões de subclasse.</span><span class="sxs-lookup"><span data-stu-id="6fb46-115">Subclass buttons.</span></span><br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <span data-ttu-id="6fb46-116"><dt>**CTL3D \_**</dt> <dt>0X0002</dt> de caixas de listagem</span><span class="sxs-lookup"><span data-stu-id="6fb46-116"><dt>**CTL3D\_LISTBOXES**</dt> <dt>0x0002</dt></span></span> </dl>           | <span data-ttu-id="6fb46-117">Caixas de listagem de subclasses.</span><span class="sxs-lookup"><span data-stu-id="6fb46-117">Subclass list boxes.</span></span><br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <span data-ttu-id="6fb46-118"><dt>**CTL3D \_ EDITA**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="6fb46-118"><dt>**CTL3D\_EDITS**</dt> <dt>0x0004</dt></span></span> </dl>                       | <span data-ttu-id="6fb46-119">Controles de edição de subclasse.</span><span class="sxs-lookup"><span data-stu-id="6fb46-119">Subclass edit controls.</span></span><br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <span data-ttu-id="6fb46-120"><dt>**CTL3D \_**</dt> <dt>0X0008</dt> de combinação</span><span class="sxs-lookup"><span data-stu-id="6fb46-120"><dt>**CTL3D\_COMBOS**</dt> <dt>0x0008</dt></span></span> </dl>                    | <span data-ttu-id="6fb46-121">Caixas de combinação de subclasse.</span><span class="sxs-lookup"><span data-stu-id="6fb46-121">Subclass combo boxes.</span></span><br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <span data-ttu-id="6fb46-122"><dt>**CTL3D \_ STATICTEXTS**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="6fb46-122"><dt>**CTL3D\_STATICTEXTS**</dt> <dt>0x0010</dt></span></span> </dl>     | <span data-ttu-id="6fb46-123">Controles de texto estáticos de subclasse.</span><span class="sxs-lookup"><span data-stu-id="6fb46-123">Subclass static text controls.</span></span><br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <span data-ttu-id="6fb46-124"><dt>**CTL3D \_ STATICFRAMES**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="6fb46-124"><dt>**CTL3D\_STATICFRAMES**</dt> <dt>0x0020</dt></span></span> </dl>  | <span data-ttu-id="6fb46-125">Quadros estáticos de subclasse.</span><span class="sxs-lookup"><span data-stu-id="6fb46-125">Subclass static frames.</span></span><br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <span data-ttu-id="6fb46-126"><dt>**CTL3D \_ Todos os**</dt> <dt>0xFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="6fb46-126"><dt>**CTL3D\_ALL**</dt> <dt>0xffff</dt></span></span> </dl>                             | <span data-ttu-id="6fb46-127">Subclasse todos os controles.</span><span class="sxs-lookup"><span data-stu-id="6fb46-127">Subclass all controls.</span></span><br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <span data-ttu-id="6fb46-128"><dt>**CTL3D \_ NODLGWINDOW**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="6fb46-128"><dt>**CTL3D\_NODLGWINDOW**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="6fb46-129">Não faça a subclasse da janela de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6fb46-129">Do not subclass the dialog window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fb46-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fb46-130">Return value</span></span>

<span data-ttu-id="6fb46-131">Retornará **true** se a função tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="6fb46-131">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fb46-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fb46-132">Remarks</span></span>

<span data-ttu-id="6fb46-133">Essa função é especialmente útil em aplicativos baseados em C++.</span><span class="sxs-lookup"><span data-stu-id="6fb46-133">This function is especially useful in applications based on C++.</span></span>

<span data-ttu-id="6fb46-134">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="6fb46-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fb46-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fb46-135">Requirements</span></span>



| <span data-ttu-id="6fb46-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fb46-136">Requirement</span></span> | <span data-ttu-id="6fb46-137">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb46-137">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb46-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6fb46-138">DLL</span></span><br/> | <dl> <span data-ttu-id="6fb46-139"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fb46-139"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
