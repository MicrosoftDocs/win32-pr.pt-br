---
title: Método IAccessibilityDockingService GetAvailableSize
description: Obtém as dimensões disponíveis para o encaixe de uma janela de acessibilidade em um monitor.
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- Método COM de GetAvailableSize
- Método GetAvailableSize COM, interface IAccessibilityDockingService
- IAccessibilityDockingService interface COM, método GetAvailableSize
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006486"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a><span data-ttu-id="cd5d9-106">Método IAccessibilityDockingService:: GetAvailableSize</span><span class="sxs-lookup"><span data-stu-id="cd5d9-106">IAccessibilityDockingService::GetAvailableSize method</span></span>

<span data-ttu-id="cd5d9-107">Obtém as dimensões disponíveis para o encaixe de uma janela de acessibilidade em um monitor.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-107">Gets the dimensions available for docking an accessibility window on a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd5d9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd5d9-108">Syntax</span></span>


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a><span data-ttu-id="cd5d9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd5d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd5d9-110">*HMONITOR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd5d9-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd5d9-111">Especifica o monitor para o qual o tamanho de encaixe disponível será recuperado.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-111">Specifies the monitor for which the available docking size will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="cd5d9-112">*puMaxHeight* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cd5d9-112">*puMaxHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd5d9-113">Em caso de sucesso, defina para a altura máxima disponível para encaixe no *HMONITOR* especificado, em pixels.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-113">On success, set to the maximum height available for docking on the specified *hMonitor*, in pixels.</span></span>

<span data-ttu-id="cd5d9-114">Em caso de falha, defina como zero.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-114">On failure, set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd5d9-115">*puFixedWidth* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cd5d9-115">*puFixedWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd5d9-116">Em caso de sucesso, defina a largura fixa disponível para encaixe no *HMONITOR* especificado, em pixels.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-116">On success, set to the fixed width available for docking on the specified *hMonitor*, in pixels.</span></span> <span data-ttu-id="cd5d9-117">Qualquer janela encaixada neste *HMONITOR* será dimensionada para essa largura.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-117">Any window docked to this *hMonitor* will be sized to this width.</span></span>

<span data-ttu-id="cd5d9-118">Em caso de falha, defina como zero.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-118">On failure, set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd5d9-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd5d9-119">Return value</span></span>



| <span data-ttu-id="cd5d9-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cd5d9-120">Return code</span></span>                                                                                                                          | <span data-ttu-id="cd5d9-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd5d9-121">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd5d9-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cd5d9-122"><dt>**S\_OK**</dt></span></span> </dl>                                                 | <span data-ttu-id="cd5d9-123">Êxito.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-123">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="cd5d9-124"><dt>**HRESULT \_ do \_ Win32 (erro \_ \_ identificador de monitor inválido \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="cd5d9-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_MONITOR\_HANDLE)**</dt></span></span> </dl> | <span data-ttu-id="cd5d9-125">O monitor especificado pelo identificador de monitor não oferece suporte ao encaixe.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-125">The monitor specified by the monitor handle does not support docking.</span></span><br/> |



 

<span data-ttu-id="cd5d9-126">Se *puMaxHeight* ou *puFixedWidth* forem nulos, ocorrerá uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-126">If either *puMaxHeight* or *puFixedWidth* are null, an access violation will occur.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd5d9-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd5d9-127">Remarks</span></span>

<span data-ttu-id="cd5d9-128">As janelas de acessibilidade só podem ser encaixadas em um monitor que tenha pelo menos 768 pixels de tela vertical.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-128">Accessibility windows can only be docked to a monitor that has at least 768 vertical screen pixels.</span></span> <span data-ttu-id="cd5d9-129">Essa API não permitirá que essas janelas sejam encaixadas com uma altura que faria com que os aplicativos da Windows Store tenham menos de 768 pixels de tela vertical.</span><span class="sxs-lookup"><span data-stu-id="cd5d9-129">This API will not allow such windows to be docked with a height that would cause Windows Store apps to have less than 768 vertical screen pixels.</span></span>

## <a name="examples"></a><span data-ttu-id="cd5d9-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cd5d9-130">Examples</span></span>


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a><span data-ttu-id="cd5d9-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd5d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd5d9-132">**IAccessibilityDockingService**</span><span class="sxs-lookup"><span data-stu-id="cd5d9-132">**IAccessibilityDockingService**</span></span>](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





