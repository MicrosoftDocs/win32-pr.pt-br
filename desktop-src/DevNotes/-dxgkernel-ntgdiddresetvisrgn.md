---
description: Usado para habilitar o modo de usuário para obter uma compreensão válida da região de recorte para Windows na área de trabalho. Esse recorte pode ser alterado de forma assíncrona do ponto de vista de threads do modo de usuário.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Função NtGdiDdResetVisrgn (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826136"
---
# <a name="ntgdiddresetvisrgn-function"></a><span data-ttu-id="1d610-104">Função NtGdiDdResetVisrgn</span><span class="sxs-lookup"><span data-stu-id="1d610-104">NtGdiDdResetVisrgn function</span></span>

<span data-ttu-id="1d610-105">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1d610-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="1d610-106">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="1d610-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="1d610-107">Usado para habilitar o modo de usuário para obter uma compreensão válida da região de recorte para Windows na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1d610-107">Used to enable the user mode to gain a valid understanding of the clipping region for windows on the desktop.</span></span> <span data-ttu-id="1d610-108">Esse recorte pode ser alterado de forma assíncrona do ponto de vista de threads do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="1d610-108">This clipping can change asynchronously from the point of view of user-mode threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d610-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d610-109">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="1d610-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d610-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d610-111">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d610-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d610-112">Ponteiro para o objeto de modo de usuário de qualquer superfície que pertence ao dispositivo do DirectDraw para o qual o recorte deve ser redefinido.</span><span class="sxs-lookup"><span data-stu-id="1d610-112">Pointer to the user-mode object of any surface belonging to the DirectDraw device for which clipping is to be reset.</span></span> <span data-ttu-id="1d610-113">Para obter detalhes, consulte a documentação do DDK.</span><span class="sxs-lookup"><span data-stu-id="1d610-113">For details, see the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="1d610-114">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d610-114">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d610-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1d610-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d610-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d610-116">Return value</span></span>

<span data-ttu-id="1d610-117">Se for bem-sucedida, essa função retornará **true**; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="1d610-117">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d610-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d610-118">Remarks</span></span>

<span data-ttu-id="1d610-119">O recorte pode ser alterado de forma assíncrona do ponto de vista de threads do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="1d610-119">Clipping can change asynchronously from the point of view of user-mode threads.</span></span> <span data-ttu-id="1d610-120">As partes do modo kernel do DirectDraw e do Windows Graphics Device Interface (GDI) mantêm um contador que é incrementado sempre que a lista de recorte de toda a área de trabalho é alterada.</span><span class="sxs-lookup"><span data-stu-id="1d610-120">The kernel-mode parts of DirectDraw and Windows Graphics Device Interface (GDI) maintain a counter that is incremented whenever the clipping list for the entire desktop changes.</span></span> <span data-ttu-id="1d610-121">Uma chamada para essa função registra esse contador com cada superfície primária do DirectDraw existente no sistema.</span><span class="sxs-lookup"><span data-stu-id="1d610-121">A call to this function records this counter with every existing DirectDraw primary surface on the system.</span></span>

<span data-ttu-id="1d610-122">Posteriormente, quando uma dessas superfícies primárias for modificada por uma operação [IDirectDrawSurface7:: Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) ou [IDirectDrawSurface7:: Lock](/previous-versions/ms858221(v=msdn.10)) (consulte a documentação do DDK), o contador registrado com a superfície será comparado com o contador global.</span><span class="sxs-lookup"><span data-stu-id="1d610-122">At any later time when one of these primary surfaces is modified by a [IDirectDrawSurface7::Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) or [IDirectDrawSurface7::Lock](/previous-versions/ms858221(v=msdn.10)) operation (see DDK documentation), then the counter recorded with the surface is compared with the global counter.</span></span> <span data-ttu-id="1d610-123">Se esses valores forem diferentes, um código de erro DDERR \_ VISRGNCHANGED será retornado para o código do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="1d610-123">If these values are different, an error code DDERR\_VISRGNCHANGED is returned to the user-mode code.</span></span> <span data-ttu-id="1d610-124">O código de modo de usuário então consultará novamente o recorte atual para a área de trabalho, chamará **NtGdiDdResetVisrgn** e tentará novamente o IDirectDrawSurface7:: Blt aplicado à superfície primária, respeitando o novo recorte.</span><span class="sxs-lookup"><span data-stu-id="1d610-124">The user-mode code will then re-query the current clipping for the desktop, call **NtGdiDdResetVisrgn**, and re-try the IDirectDrawSurface7::Blt applied to the primary surface, respecting the new clipping.</span></span> <span data-ttu-id="1d610-125">Eventualmente, o recorte que foi amostrado pelo código do modo de usuário será o mesmo que o recorte atual de Propriedade do modo kernel, e o IDirectDrawSurface7:: Blt terá permissão para continuar.</span><span class="sxs-lookup"><span data-stu-id="1d610-125">Eventually, the clipping that was sampled by the user-mode code will be the same as the current clipping owned by kernel mode, and the IDirectDrawSurface7::Blt will be allowed to continue.</span></span>

<span data-ttu-id="1d610-126">Os aplicativos são aconselhados a usar a interface [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) ou o método [IDirect3DDevice8::P reenviado](/previous-versions/ms889707(v=msdn.10)) para lidar com alterações de recorte assíncrono.</span><span class="sxs-lookup"><span data-stu-id="1d610-126">Applications are advised to use the [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) interface or [IDirect3DDevice8::Present](/previous-versions/ms889707(v=msdn.10)) method to handle asynchronous clipping changes.</span></span> <span data-ttu-id="1d610-127">Essas construções implementam recorte assíncrono em uma maneira automatizada e independente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1d610-127">These constructs implement asynchronous clipping in an automated and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d610-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d610-128">Requirements</span></span>



| <span data-ttu-id="1d610-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d610-129">Requirement</span></span> | <span data-ttu-id="1d610-130">Valor</span><span class="sxs-lookup"><span data-stu-id="1d610-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d610-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d610-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1d610-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1d610-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1d610-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d610-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1d610-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1d610-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1d610-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1d610-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d610-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d610-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d610-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d610-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d610-138">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="1d610-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="1d610-139">**DdResetVisrgn**</span><span class="sxs-lookup"><span data-stu-id="1d610-139">**DdResetVisrgn**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
