---
title: Interface do IMsRdpClientNonScriptable6
description: Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota. Deriva da interface IMsRdpClientNonScriptable5.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable6
- Serviços de Área de Trabalho Remota da interface IMsRdpClientNonScriptable6, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 0d6793452ebf59f1974831aef0fa10f2469d8e92
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104370030"
---
# <a name="imsrdpclientnonscriptable6-interface"></a><span data-ttu-id="d5a86-106">Interface do IMsRdpClientNonScriptable6</span><span class="sxs-lookup"><span data-stu-id="d5a86-106">IMsRdpClientNonScriptable6 interface</span></span>

<span data-ttu-id="d5a86-107">Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="d5a86-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="d5a86-108">Deriva da interface [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) .</span><span class="sxs-lookup"><span data-stu-id="d5a86-108">Derives from the [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) interface.</span></span> <span data-ttu-id="d5a86-109">Os métodos desta interface só podem ser acessados por meio de vtable; Eles não estão disponíveis para uso em clientes programáveis.</span><span class="sxs-lookup"><span data-stu-id="d5a86-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="d5a86-110">Uma instância dessa interface é obtida chamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto [**IMsTscAx**](imstscax-interface.md) , passando **\_ IMsRdpClientNonScriptable6 de IID**.</span><span class="sxs-lookup"><span data-stu-id="d5a86-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable6**.</span></span>

## <a name="members"></a><span data-ttu-id="d5a86-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d5a86-111">Members</span></span>

<span data-ttu-id="d5a86-112">A interface **IMsRdpClientNonScriptable6** herda de [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="d5a86-112">The **IMsRdpClientNonScriptable6** interface inherits from [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="d5a86-113">**IMsRdpClientNonScriptable6** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d5a86-113">**IMsRdpClientNonScriptable6** also has these types of members:</span></span>

- [<span data-ttu-id="d5a86-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d5a86-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d5a86-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="d5a86-115">Methods</span></span>

<span data-ttu-id="d5a86-116">A interface **IMsRdpClientNonScriptable6** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d5a86-116">The **IMsRdpClientNonScriptable6** interface has these methods.</span></span>


| <span data-ttu-id="d5a86-117">Método</span><span class="sxs-lookup"><span data-stu-id="d5a86-117">Method</span></span>            | <span data-ttu-id="d5a86-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5a86-118">Description</span></span>                   |
|:-----------------------------|:-----------------|
| [<span data-ttu-id="d5a86-119">**SendLocation2D**</span><span class="sxs-lookup"><span data-stu-id="d5a86-119">**SendLocation2D**</span></span>](imsrdpclientnonscriptable6-sendlocation2d.md)     |  <span data-ttu-id="d5a86-120">Envia um valor de latitude e longitude para o servidor para que a localização geográfica do cliente possa ser refletida na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="d5a86-120">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                   |
| [<span data-ttu-id="d5a86-121">**SendLocation3D**</span><span class="sxs-lookup"><span data-stu-id="d5a86-121">**SendLocation3D**</span></span>](imsrdpclientnonscriptable6-sendlocation3d.md)     | <span data-ttu-id="d5a86-122">Envia um valor de latitude, longitude e altitude para o servidor para que o local geográfico do cliente possa ser refletido na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="d5a86-122">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                 |

## <a name="requirements"></a><span data-ttu-id="d5a86-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5a86-123">Requirements</span></span>

| <span data-ttu-id="d5a86-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5a86-124">Requirement</span></span> | <span data-ttu-id="d5a86-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d5a86-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="d5a86-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5a86-126">Minimum supported client</span></span>| <span data-ttu-id="d5a86-127">Windows 10, versão 1709 (build 16299)</span><span class="sxs-lookup"><span data-stu-id="d5a86-127">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="d5a86-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d5a86-128">Type library</span></span>            | <span data-ttu-id="d5a86-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d5a86-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="d5a86-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d5a86-130">DLL</span></span>                  | <span data-ttu-id="d5a86-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d5a86-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="d5a86-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="d5a86-132">CLSID</span></span>                    | <span data-ttu-id="d5a86-133">CLSID \_ MsRdpClient12 é definido como 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="d5a86-133">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="d5a86-134">CLSID \_ MsRdpClient12NotSafeForScripting é definido como 3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="d5a86-134">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="d5a86-135">CLSID \_ MsRdpClient11 é definido como 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="d5a86-135">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="d5a86-136">CLSID \_ MsRdpClient11NotSafeForScripting é definido como 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="d5a86-136">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="d5a86-137">IID</span><span class="sxs-lookup"><span data-stu-id="d5a86-137">IID</span></span>                      | <span data-ttu-id="d5a86-138">IID \_ IMsRdpClientNonScriptable6 é definido como 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="d5a86-138">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="d5a86-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5a86-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5a86-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="d5a86-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>
