---
description: Consulta uma representação em modo kernel criada anteriormente de um objeto Microsoft DirectDraw para seus recursos.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Função NtGdiDdQueryDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 557854f70f4f1a55022b16d1bfe045efbc017a13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826567"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a><span data-ttu-id="2b2b7-103">Função NtGdiDdQueryDirectDrawObject</span><span class="sxs-lookup"><span data-stu-id="2b2b7-103">NtGdiDdQueryDirectDrawObject function</span></span>

<span data-ttu-id="2b2b7-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="2b2b7-105">Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="2b2b7-106">Consulta uma representação em modo kernel criada anteriormente de um objeto Microsoft DirectDraw para seus recursos.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-106">Queries a previously created kernel-mode representation of a Microsoft DirectDraw object for its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b2b7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b2b7-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a><span data-ttu-id="2b2b7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b2b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b2b7-109">*hDirectDrawLocal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2b7-110">Identificador para o dispositivo DirectDraw do modo kernel criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-110">Handle to the previously-created kernel-mode DirectDraw device.</span></span>

</dd> <dt>

<span data-ttu-id="2b2b7-111">*pHalInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-111">*pHalInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2b7-112">Ponteiro para uma [**estrutura \_ HALINFO do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) que será preenchida com os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-112">Pointer to a [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) structure that will be filled with the device's capabilities.</span></span> <span data-ttu-id="2b2b7-113">Consulte a documentação do DDK para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-113">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="2b2b7-114">*pCallBackFlags*</span><span class="sxs-lookup"><span data-stu-id="2b2b7-114">*pCallBackFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="2b2b7-115">Ponteiro para um buffer fornecido pelo chamador que armazena sinalizadores de retorno de chamada relatados por driver.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-115">Pointer to a caller-provided buffer that stores driver-reported callback flags.</span></span> <span data-ttu-id="2b2b7-116">O buffer deve ter tamanho 3 \* sizeof (DWORD) e armazena sinalizadores de retorno de chamada na seguinte ordem: pCallBackFlags \[ 0 \] para sinalizadores em [**\_ retornos de chamada DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), pCallBackFlags \[ 1 \] para sinalizadores em [**DD \_ SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)e pCallBackFlags \[ 2 \] para sinalizadores em [**DD \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span><span class="sxs-lookup"><span data-stu-id="2b2b7-116">The buffer should be of size 3\*sizeof(DWORD) and stores callback flags in the following order: pCallBackFlags\[0\] for flags in [**DD\_CALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), pCallBackFlags\[1\] for flags in [**DD\_SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks), and pCallBackFlags\[2\] for flags in [**DD\_PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span></span> <span data-ttu-id="2b2b7-117">Consulte a documentação do DDK para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-117">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="2b2b7-118">*puD3dCallbacks* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-118">*puD3dCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2b7-119">Ponteiro para uma tabela de ponteiros de retorno de chamada Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-119">Pointer to a table of Direct3D callback pointers.</span></span> <span data-ttu-id="2b2b7-120">A tabela é preenchida com ponteiros para funções dentro Gdi32.dll que imitam um driver de vídeo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-120">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="2b2b7-121">Essa tabela de retorno de chamada é idêntica à \_ estrutura D3DHAL D3DCALLBACKS discutida na documentação do DDK.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-121">This callback table is identical to the D3DHAL\_D3DCALLBACKS structure discussed in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="2b2b7-122">*puD3dDriverData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-122">*puD3dDriverData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2b7-123">Ponteiro para [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) data, conforme descrito na documentação do DDK.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-123">Pointer to [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) data, as described in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="2b2b7-124">*puD3dBufferCallbacks* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-124">*puD3dBufferCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2b7-125">Ponteiro para uma tabela de ponteiros de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-125">Pointer to a table of callback pointers.</span></span> <span data-ttu-id="2b2b7-126">A tabela é preenchida com ponteiros para funções dentro Gdi32.dll que imitam um driver de vídeo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-126">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="2b2b7-127">Essa tabela de retorno de chamada é idêntica à \_ estrutura DDHAL DDEXEBUFCALLBACKS, que é mapeada para a estrutura [**DD \_ D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) discutida na documentação do DDK, exceto que os membros XxxD3DBuffer no **DD \_ D3DBUFCALLBACKS** são substituídos por XxxExecuteBuffer no DDHAL \_ DDEXEBUFCALLBACKS.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-127">This callback table is identical to the DDHAL\_DDEXEBUFCALLBACKS structure, which maps to the [**DD\_D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) structure discussed in the DDK documentation, except that members XxxD3DBuffer in **DD\_D3DBUFCALLBACKS** are replaced with XxxExecuteBuffer in DDHAL\_DDEXEBUFCALLBACKS.</span></span>

</dd> <dt>

<span data-ttu-id="2b2b7-128">*puD3dTextureFormats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-128">*puD3dTextureFormats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2b7-129">Ponteiro para uma matriz de estruturas [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que definem o conjunto de formatos de textura permitidos.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-129">Pointer to an array of [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structures that define the set of permissible texture formats.</span></span>

</dd> <dt>

<span data-ttu-id="2b2b7-130">*puNumHeaps* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-130">*puNumHeaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2b7-131">Ponteiro para o membro **dwNumHeaps** de [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-131">Pointer to the **dwNumHeaps** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**.</span></span> <span data-ttu-id="2b2b7-132">O membro **dwNumHeaps** especifica o número de heaps de memória em *puvmList*.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-132">The **dwNumHeaps** member specifies the number of memory heaps in *puvmList*.</span></span> <span data-ttu-id="2b2b7-133">Consulte a documentação do DDK para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-133">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="2b2b7-134">*puvmList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-134">*puvmList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2b7-135">Ponteiro para uma lista de descritores de heap de memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-135">Pointer to a list of video memory heap descriptors.</span></span> <span data-ttu-id="2b2b7-136">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-136">Can be **NULL**.</span></span> <span data-ttu-id="2b2b7-137">Esse parâmetro não é usado porque o gerenciamento de memória de vídeo é totalmente manipulado no modo kernel.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-137">This parameter is not used because video memory management is handled entirely within kernel mode.</span></span>

</dd> <dt>

<span data-ttu-id="2b2b7-138">*puNumFourCC* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-138">*puNumFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2b7-139">Ponteiro para o membro **puNumFourCCCodes** de [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-139">Pointer to the **puNumFourCCCodes** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.</span></span> <span data-ttu-id="2b2b7-140">O membro **puNumFourCCCodes** especifica o número de códigos de [quatro caracteres (FourCC)](../directshow/fourcc-codes.md) aos quais o driver dá suporte.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-140">The **puNumFourCCCodes** member specifies the number of [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) codes that the driver supports.</span></span> <span data-ttu-id="2b2b7-141">Consulte a documentação do DDK para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-141">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="2b2b7-142">*puFourCC* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-142">*puFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2b7-143">Ponteiro para uma lista de formatos de superfície [FOURCC (códigos de quatro caracteres)](../directshow/fourcc-codes.md) com suporte.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-143">Pointer to a list of supported [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) surface formats.</span></span> <span data-ttu-id="2b2b7-144">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-144">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b2b7-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b2b7-145">Return value</span></span>

<span data-ttu-id="2b2b7-146">Se for bem-sucedida, essa função retornará **true**; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-146">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b2b7-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b2b7-147">Remarks</span></span>

<span data-ttu-id="2b2b7-148">Uma chamada para essa função foi projetada para ser feita em um processo de duas etapas.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-148">A call to this function is designed to be made in a two-step process.</span></span> <span data-ttu-id="2b2b7-149">Na primeira etapa, *puFourCC*, *puvmList* e *PuD3dTextureFormats* devem ser **NULL** e [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) preencherá o [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. **dwNumFourCCCodes**, **DD \_ HALINFO**.**vmiData**. **dwNumHeaps** e [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** com o número de entradas que devem ser retornadas.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-149">In the first step, *puFourCC*, *puvmList* and *puD3dTextureFormats* should be **NULL**, and [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) will fill in [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.**dwNumFourCCCodes**, **DD\_HALINFO**.**vmiData**.**dwNumHeaps**, and [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** with the number of entries that are to be returned.</span></span> <span data-ttu-id="2b2b7-150">Na segunda chamada, o chamador deve alocar matrizes do tamanho indicado e passar esses ponteiros em vez de valores **nulos** nos parâmetros *puFourCC*, *puvmList* e *puD3dTextureFormats* .</span><span class="sxs-lookup"><span data-stu-id="2b2b7-150">In the second call, the caller should allocate arrays of the indicated size and pass those pointers instead of **NULL** values in the *puFourCC*, *puvmList* and *puD3dTextureFormats* parameters.</span></span> <span data-ttu-id="2b2b7-151">As matrizes serão então preenchidas com os dados apropriados.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-151">The arrays will then be populated with appropriate data.</span></span>

<span data-ttu-id="2b2b7-152">Os aplicativos são aconselhados a usar as APIs do DirectDraw e do [Direct3D](../direct3d10/d3d10-graphics-reference.md) para criar e gerenciar objetos de dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-152">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="2b2b7-153">Essas construções abstraem o processo de criação de dispositivos de maneira simplificada e independente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2b2b7-153">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b2b7-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b2b7-154">Requirements</span></span>



| <span data-ttu-id="2b2b7-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b2b7-155">Requirement</span></span> | <span data-ttu-id="2b2b7-156">Valor</span><span class="sxs-lookup"><span data-stu-id="2b2b7-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2b7-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b2b7-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2b2b7-158">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2b2b7-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b2b7-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2b2b7-160">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2b2b7-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2b2b7-161">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2b2b7-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b2b7-162"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b2b7-162"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b2b7-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b2b7-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b2b7-164">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="2b2b7-164">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="2b2b7-165">**DdQueryDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="2b2b7-165">**DdQueryDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[<span data-ttu-id="2b2b7-166">**NtGdiDdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="2b2b7-166">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
