---
description: Libera o contexto de dispositivo criado anteriormente (DC) para o objeto de superfície do Microsoft DirectDraw no modo kernel indicado.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: Função NtGdiDdReleaseDC (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a7319b423f12d7e4415d78d995bfb1d7cd0341a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826138"
---
# <a name="ntgdiddreleasedc-function"></a><span data-ttu-id="17d70-103">Função NtGdiDdReleaseDC</span><span class="sxs-lookup"><span data-stu-id="17d70-103">NtGdiDdReleaseDC function</span></span>

<span data-ttu-id="17d70-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="17d70-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="17d70-105">Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="17d70-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="17d70-106">Libera o contexto de dispositivo criado anteriormente (DC) para o objeto de superfície do Microsoft DirectDraw no modo kernel indicado.</span><span class="sxs-lookup"><span data-stu-id="17d70-106">Releases the previously created device context (DC) for the indicated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d70-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17d70-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="17d70-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17d70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17d70-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17d70-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17d70-110">Identificador para o objeto de superfície do DirectDraw do modo de kernel criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="17d70-110">Handle to the previously created kernel-mode DirectDraw surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17d70-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17d70-111">Return value</span></span>

<span data-ttu-id="17d70-112">Se for bem-sucedida, essa função retornará **true**; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="17d70-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="17d70-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="17d70-113">Remarks</span></span>

<span data-ttu-id="17d70-114">Os aplicativos que precisam obter um controlador de domínio para uma superfície do DirectDraw podem usar [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), que expõe essa funcionalidade de maneira independente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="17d70-114">Applications that need to obtain a DC for a DirectDraw surface may use [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), which exposes this functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="17d70-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17d70-115">Requirements</span></span>



| <span data-ttu-id="17d70-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="17d70-116">Requirement</span></span> | <span data-ttu-id="17d70-117">Valor</span><span class="sxs-lookup"><span data-stu-id="17d70-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17d70-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17d70-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17d70-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="17d70-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="17d70-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17d70-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17d70-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="17d70-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="17d70-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="17d70-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="17d70-123"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="17d70-123"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17d70-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="17d70-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d70-125">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="17d70-125">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="17d70-126">**DdReleaseDC**</span><span class="sxs-lookup"><span data-stu-id="17d70-126">**DdReleaseDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
