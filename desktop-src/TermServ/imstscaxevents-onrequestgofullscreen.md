---
title: Método IMsTscAxEvents OnRequestGoFullScreen
description: Chamado quando o cliente solicita para alternar para o modo de tela inteira e o método IMsTscAdvancedSettings Put \_ ContainerHandledFullScreen é chamado para definir a propriedade ContainerHandledFullScreen como um valor diferente de zero.
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnRequestGoFullScreen
- Método OnRequestGoFullScreen Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnRequestGoFullScreen
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestGoFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c865cd27b447743f781b8563956e7fb2d7f5d703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369725"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a><span data-ttu-id="05182-106">Método IMsTscAxEvents:: OnRequestGoFullScreen</span><span class="sxs-lookup"><span data-stu-id="05182-106">IMsTscAxEvents::OnRequestGoFullScreen method</span></span>

<span data-ttu-id="05182-107">Chamado quando o cliente solicita para alternar para o modo de tela inteira e o método [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) é chamado para definir a propriedade **ContainerHandledFullScreen** como um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="05182-107">Called when the client requests to switch to full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called to set the **ContainerHandledFullScreen** property to a nonzero value.</span></span>

## <a name="syntax"></a><span data-ttu-id="05182-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05182-108">Syntax</span></span>


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a><span data-ttu-id="05182-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05182-109">Parameters</span></span>

<span data-ttu-id="05182-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="05182-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05182-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05182-111">Return value</span></span>

<span data-ttu-id="05182-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="05182-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05182-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="05182-113">Remarks</span></span>

<span data-ttu-id="05182-114">No modo de tela inteira manipulado por contêiner, o contêiner deve inserir o modo de tela inteira padrão em resposta a esse evento.</span><span class="sxs-lookup"><span data-stu-id="05182-114">In container-handled full-screen mode, the container should enter standard full-screen mode in response to this event.</span></span>

<span data-ttu-id="05182-115">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="05182-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05182-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05182-116">Requirements</span></span>



| <span data-ttu-id="05182-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="05182-117">Requirement</span></span> | <span data-ttu-id="05182-118">Valor</span><span class="sxs-lookup"><span data-stu-id="05182-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05182-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05182-119">Minimum supported client</span></span><br/> | <span data-ttu-id="05182-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05182-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="05182-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05182-121">Minimum supported server</span></span><br/> | <span data-ttu-id="05182-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05182-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="05182-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="05182-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="05182-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05182-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="05182-125">DLL</span><span class="sxs-lookup"><span data-stu-id="05182-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05182-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05182-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="05182-127">IID</span><span class="sxs-lookup"><span data-stu-id="05182-127">IID</span></span><br/>                      | <span data-ttu-id="05182-128">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="05182-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="05182-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="05182-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05182-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="05182-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





