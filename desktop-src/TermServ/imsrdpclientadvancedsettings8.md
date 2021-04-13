---
title: Interface IMsRdpClientAdvancedSettings8
description: Expõe métodos e propriedades que gerenciam as configurações avançadas do controle ActiveX Área de Trabalho Remota.
ms.assetid: 9e1de47d-f194-4d9e-8e47-7c13a0677aaa
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings8, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fce32baf792563e64d2f8b8e1ad2bd56a31c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369378"
---
# <a name="imsrdpclientadvancedsettings8-interface"></a><span data-ttu-id="02705-105">Interface IMsRdpClientAdvancedSettings8</span><span class="sxs-lookup"><span data-stu-id="02705-105">IMsRdpClientAdvancedSettings8 interface</span></span>

<span data-ttu-id="02705-106">Expõe métodos e propriedades que gerenciam as configurações avançadas do controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="02705-106">Exposes methods and properties that manage advanced settings of the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="02705-107">Para obter uma instância dessa interface, use a propriedade [**IMsRdpClient8:: AdvancedSettings9**](imsrdpclient8-advancedsettings9.md) .</span><span class="sxs-lookup"><span data-stu-id="02705-107">To obtain an instance of this interface, use the [**IMsRdpClient8::AdvancedSettings9**](imsrdpclient8-advancedsettings9.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="02705-108">Membros</span><span class="sxs-lookup"><span data-stu-id="02705-108">Members</span></span>

<span data-ttu-id="02705-109">A interface **IMsRdpClientAdvancedSettings8** herda de [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md).</span><span class="sxs-lookup"><span data-stu-id="02705-109">The **IMsRdpClientAdvancedSettings8** interface inherits from [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md).</span></span> <span data-ttu-id="02705-110">**IMsRdpClientAdvancedSettings8** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="02705-110">**IMsRdpClientAdvancedSettings8** also has these types of members:</span></span>

-   [<span data-ttu-id="02705-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="02705-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02705-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="02705-112">Properties</span></span>

<span data-ttu-id="02705-113">A interface **IMsRdpClientAdvancedSettings8** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="02705-113">The **IMsRdpClientAdvancedSettings8** interface has these properties.</span></span>



| <span data-ttu-id="02705-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="02705-114">Property</span></span>                                                                                  | <span data-ttu-id="02705-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="02705-115">Access type</span></span>           | <span data-ttu-id="02705-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="02705-116">Description</span></span>                                                           |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="02705-117">**BandwidthDetection**</span><span class="sxs-lookup"><span data-stu-id="02705-117">**BandwidthDetection**</span></span>](imsrdpclientadvancedsettings8-bandwidthdetection.md)<br/> | <span data-ttu-id="02705-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="02705-118">Read/write</span></span><br/> | <span data-ttu-id="02705-119">Especifica se as alterações de largura de banda são detectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="02705-119">Specifies if bandwidth changes are automatically detected.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="02705-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02705-120">Requirements</span></span>



| <span data-ttu-id="02705-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="02705-121">Requirement</span></span> | <span data-ttu-id="02705-122">Valor</span><span class="sxs-lookup"><span data-stu-id="02705-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02705-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02705-123">Minimum supported client</span></span><br/> | <span data-ttu-id="02705-124">Windows 8</span><span class="sxs-lookup"><span data-stu-id="02705-124">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="02705-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02705-125">Minimum supported server</span></span><br/> | <span data-ttu-id="02705-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="02705-126">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="02705-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="02705-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="02705-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02705-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="02705-129">DLL</span><span class="sxs-lookup"><span data-stu-id="02705-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02705-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02705-130"><dt>MsTscAx.dll</dt></span></span> </dl> |



 

 





