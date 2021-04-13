---
title: Método IMsTscAxEvents OnRequestContainerMinimize
description: Chamado quando o usuário pressiona o botão minimizar na barra de conexão no modo de tela inteira. O acionamento desse evento é uma solicitação que o aplicativo de contêiner minimiza em si mesmo.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnRequestContainerMinimize
- Método OnRequestContainerMinimize Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnRequestContainerMinimize
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85387e3b156eed29dc7068eac84280be521a934e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369726"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a><span data-ttu-id="5166d-107">Método IMsTscAxEvents:: OnRequestContainerMinimize</span><span class="sxs-lookup"><span data-stu-id="5166d-107">IMsTscAxEvents::OnRequestContainerMinimize method</span></span>

<span data-ttu-id="5166d-108">Chamado quando o usuário pressiona o botão **minimizar** na barra de conexão no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="5166d-108">Called when the user presses the **Minimize** button on the connection bar in full-screen mode.</span></span> <span data-ttu-id="5166d-109">O acionamento desse evento é uma solicitação que o aplicativo de contêiner minimiza em si mesmo.</span><span class="sxs-lookup"><span data-stu-id="5166d-109">The firing of this event is a request that the container application minimize itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="5166d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5166d-110">Syntax</span></span>


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a><span data-ttu-id="5166d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5166d-111">Parameters</span></span>

<span data-ttu-id="5166d-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5166d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5166d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5166d-113">Return value</span></span>

<span data-ttu-id="5166d-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5166d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5166d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5166d-115">Remarks</span></span>

<span data-ttu-id="5166d-116">Esse método só será chamado se o modo de tela inteira manipulado por contêiner estiver habilitado-consulte [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="5166d-116">This method will only be called if the container-handled full-screen mode is enabled - see [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5166d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5166d-117">Requirements</span></span>



| <span data-ttu-id="5166d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5166d-118">Requirement</span></span> | <span data-ttu-id="5166d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5166d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5166d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5166d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5166d-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5166d-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5166d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5166d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5166d-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5166d-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5166d-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5166d-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="5166d-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5166d-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5166d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5166d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5166d-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5166d-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5166d-128">IID</span><span class="sxs-lookup"><span data-stu-id="5166d-128">IID</span></span><br/>                      | <span data-ttu-id="5166d-129">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="5166d-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="5166d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5166d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5166d-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="5166d-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





