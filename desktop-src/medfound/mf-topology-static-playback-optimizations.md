---
description: Habilita otimizações estáticas no pipeline de vídeo.
ms.assetid: 62fb3f0f-ab1f-4c61-8e7f-62908b947788
title: Atributo MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f9f7d884c49078ca02571f8ba141f9a1e13589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807913"
---
# <a name="mf_topology_static_playback_optimizations-attribute"></a><span data-ttu-id="f40d3-103">\_Atributo de \_ \_ otimizações de reprodução estática da topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="f40d3-103">MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS attribute</span></span>

<span data-ttu-id="f40d3-104">Habilita otimizações estáticas no pipeline de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f40d3-104">Enables static optimizations in the video pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="f40d3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f40d3-105">Data type</span></span>

<span data-ttu-id="f40d3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f40d3-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f40d3-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="f40d3-107">Get/set</span></span>

<span data-ttu-id="f40d3-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f40d3-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f40d3-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f40d3-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="f40d3-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="f40d3-110">Applies to</span></span>

[<span data-ttu-id="f40d3-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="f40d3-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="f40d3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f40d3-112">Remarks</span></span>

<span data-ttu-id="f40d3-113">Defina esse atributo antes de carregar uma topologia.</span><span class="sxs-lookup"><span data-stu-id="f40d3-113">Set this attribute before loading a topology.</span></span> <span data-ttu-id="f40d3-114">Se o atributo for **true**, o carregador de topologia tentará otimizar o pipeline antes do início da reprodução.</span><span class="sxs-lookup"><span data-stu-id="f40d3-114">If the attribute is **TRUE**, the topology loader attempts to optimize the pipeline before playback starts.</span></span>

<span data-ttu-id="f40d3-115">Se você definir esse atributo, também deverá definir os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="f40d3-115">If you set this attribute, you should also set the following attributes:</span></span>

-   [<span data-ttu-id="f40d3-116">\_taxa de \_ quadros de reprodução da topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="f40d3-116">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span>](mf-topology-playback-framerate.md)
-   [<span data-ttu-id="f40d3-117">\_ \_ esmaecimento máximo da reprodução da topologia MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="f40d3-117">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span>](mf-topology-playback-max-dims.md)

<span data-ttu-id="f40d3-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f40d3-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="f40d3-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f40d3-119">Examples</span></span>


```C++
HRESULT SetPlaybackOptimizations(IMFTopology *pTopology, HWND hwnd)
{
    HRESULT hr = pTopology->SetUINT32(
        MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS, TRUE);

    if (FAILED(hr))
    {
        return hr;
    }

    HMONITOR hCurrentMon = MonitorFromWindow(hwnd, MONITOR_DEFAULTTOPRIMARY);

    if (hCurrentMon)
    {
        MONITORINFO MonitorInfo = {0};
        MonitorInfo.cbSize = sizeof(MONITORINFO);

        BOOL fSucceeded = GetMonitorInfo(hCurrentMon, &MonitorInfo);

        if (fSucceeded )
        {
            const RECT& rcMonitor = MonitorInfo.rcMonitor;

            LONG width = rcMonitor.right - rcMonitor.left;
            LONG height = rcMonitor.bottom - rcMonitor.top;

            hr = MFSetAttributeSize(
                pTopology, 
                MF_TOPOLOGY_PLAYBACK_MAX_DIMS, 
                (UINT32)width, (UINT32)height
                );

            if (FAILED(hr))
            {
                goto done;
            }

            HDC hdc = GetDC(hwnd);

            hr = MFSetAttributeRatio(
                pTopology,
                MF_TOPOLOGY_PLAYBACK_FRAMERATE,
                GetDeviceCaps(hdc, VREFRESH), 1
                );

            ReleaseDC(hwnd, hdc);
        }
    }
done:
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="f40d3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f40d3-120">Requirements</span></span>



| <span data-ttu-id="f40d3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f40d3-121">Requirement</span></span> | <span data-ttu-id="f40d3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f40d3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f40d3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f40d3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f40d3-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f40d3-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f40d3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f40d3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f40d3-126">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f40d3-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f40d3-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f40d3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f40d3-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f40d3-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f40d3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f40d3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f40d3-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f40d3-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f40d3-131">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="f40d3-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="f40d3-132">Gerenciamento de qualidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="f40d3-132">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




