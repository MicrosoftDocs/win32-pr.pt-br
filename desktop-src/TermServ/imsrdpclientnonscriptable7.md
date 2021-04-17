---
title: Interface do IMsRdpClientNonScriptable7
description: Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota. Deriva da interface IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable7
- Serviços de Área de Trabalho Remota da interface IMsRdpClientNonScriptable7, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8becf3bbf66ea18b2df87069ba38bab44c56db70
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "105791106"
---
# <a name="imsrdpclientnonscriptable7-interface"></a><span data-ttu-id="73382-106">Interface do IMsRdpClientNonScriptable7</span><span class="sxs-lookup"><span data-stu-id="73382-106">IMsRdpClientNonScriptable7 interface</span></span>

<span data-ttu-id="73382-107">Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="73382-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="73382-108">Deriva da interface [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) .</span><span class="sxs-lookup"><span data-stu-id="73382-108">Derives from the [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) interface.</span></span> <span data-ttu-id="73382-109">Os métodos desta interface só podem ser acessados por meio de vtable; Eles não estão disponíveis para uso em clientes programáveis.</span><span class="sxs-lookup"><span data-stu-id="73382-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="73382-110">Uma instância dessa interface é obtida chamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto [**IMsTscAx**](imstscax-interface.md) , passando **\_ IMsRdpClientNonScriptable7 de IID**.</span><span class="sxs-lookup"><span data-stu-id="73382-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable7**.</span></span>

## <a name="members"></a><span data-ttu-id="73382-111">Membros</span><span class="sxs-lookup"><span data-stu-id="73382-111">Members</span></span>

<span data-ttu-id="73382-112">A interface **IMsRdpClientNonScriptable7** herda de [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="73382-112">The **IMsRdpClientNonScriptable7** interface inherits from [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="73382-113">**IMsRdpClientNonScriptable7** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="73382-113">**IMsRdpClientNonScriptable7** also has these types of members:</span></span>

- [<span data-ttu-id="73382-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="73382-114">Methods</span></span>](#methods)
- [<span data-ttu-id="73382-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73382-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="73382-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="73382-116">Methods</span></span>

<span data-ttu-id="73382-117">A interface **IMsRdpClientNonScriptable7** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="73382-117">The **IMsRdpClientNonScriptable7** interface has these methods.</span></span>


| <span data-ttu-id="73382-118">Método</span><span class="sxs-lookup"><span data-stu-id="73382-118">Method</span></span>            | <span data-ttu-id="73382-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="73382-119">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="73382-120">**DisableDpiCursorScalingForProcess**</span><span class="sxs-lookup"><span data-stu-id="73382-120">**DisableDpiCursorScalingForProcess**</span></span>](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  <span data-ttu-id="73382-121">Desabilita o dimensionamento local do cursor do mouse recebido do servidor, garantindo que a forma do cursor seja renderizada corretamente sem modificação.</span><span class="sxs-lookup"><span data-stu-id="73382-121">Disables local scaling of the mouse cursor received from the server, ensuring that the cursor shape is rendered correctly without modification.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="73382-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73382-122">Properties</span></span>

<span data-ttu-id="73382-123">A interface **IMsRdpClientNonScriptable7** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="73382-123">The **IMsRdpClientNonScriptable7** interface has these properties.</span></span>

| <span data-ttu-id="73382-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="73382-124">Property</span></span>         | <span data-ttu-id="73382-125">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="73382-125">Access type</span></span>           | <span data-ttu-id="73382-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="73382-126">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="73382-127">**CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="73382-127">**CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | <span data-ttu-id="73382-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73382-128">Read-only</span></span> |  <span data-ttu-id="73382-129">Obtém a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="73382-129">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>   |
| [<span data-ttu-id="73382-130">**Área de Transferência**</span><span class="sxs-lookup"><span data-stu-id="73382-130">**Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)                       | <span data-ttu-id="73382-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73382-131">Read-only</span></span> |    <span data-ttu-id="73382-132">Obtém o controlador da área de transferência usado para sincronizar as áreas de transferência local e remota se a sincronização da área de transferência manual estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="73382-132">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="73382-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73382-133">Requirements</span></span>

| <span data-ttu-id="73382-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="73382-134">Requirement</span></span> | <span data-ttu-id="73382-135">Valor</span><span class="sxs-lookup"><span data-stu-id="73382-135">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="73382-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73382-136">Minimum supported client</span></span>| <span data-ttu-id="73382-137">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="73382-137">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="73382-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="73382-138">Type library</span></span>            | <span data-ttu-id="73382-139">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="73382-139">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="73382-140">DLL</span><span class="sxs-lookup"><span data-stu-id="73382-140">DLL</span></span>                  | <span data-ttu-id="73382-141">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="73382-141">MsTscAx.dll</span></span>     |
| <span data-ttu-id="73382-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="73382-142">CLSID</span></span>                    | <span data-ttu-id="73382-143">CLSID \_ MsRdpClient12 é definido como 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="73382-143">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="73382-144">CLSID \_ MsRdpClient12NotSafeForScripting é definido como 3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="73382-144">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="73382-145">CLSID \_ MsRdpClient11 é definido como 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="73382-145">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="73382-146">CLSID \_ MsRdpClient11NotSafeForScripting é definido como 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="73382-146">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="73382-147">IID</span><span class="sxs-lookup"><span data-stu-id="73382-147">IID</span></span>                      | <span data-ttu-id="73382-148">IID \_ IMsRdpClientNonScriptable7 é definido como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="73382-148">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>            |

## <a name="see-also"></a><span data-ttu-id="73382-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="73382-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73382-150">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="73382-150">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
