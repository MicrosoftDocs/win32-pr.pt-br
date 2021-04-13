---
title: Propriedade IMsRdpClientNonScriptable5 DisableConnectionBar
description: Especifica se o controle ActiveX Área de Trabalho Remota deve desabilitar a barra de conexão.
ms.assetid: 82c57b93-f976-43e6-97f9-3602bf97e466
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DisableConnectionBar
- Propriedade DisableConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade DisableConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableConnectionBar
- IMsRdpClientNonScriptable5.put_DisableConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a129d4781db69a564eecbca3a715c3c5ccf1a9cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499845"
---
# <a name="imsrdpclientnonscriptable5disableconnectionbar-property"></a><span data-ttu-id="1cfbe-106">IMsRdpClientNonScriptable5: Propriedade isableConnectionBar de:D</span><span class="sxs-lookup"><span data-stu-id="1cfbe-106">IMsRdpClientNonScriptable5::DisableConnectionBar property</span></span>

<span data-ttu-id="1cfbe-107">Especifica se o controle ActiveX Área de Trabalho Remota deve desabilitar a barra de conexão.</span><span class="sxs-lookup"><span data-stu-id="1cfbe-107">Specifies whether the Remote Desktop ActiveX control should disable the connection bar.</span></span> <span data-ttu-id="1cfbe-108">Se essa propriedade contiver a **variante \_ true**, a barra de conexão deverá ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="1cfbe-108">If this property contains **VARIANT\_TRUE**, the connection bar should be disabled.</span></span> <span data-ttu-id="1cfbe-109">Se essa propriedade contiver a **variante \_ false**, a barra de conexão deverá ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="1cfbe-109">If this property contains **VARIANT\_FALSE**, the connection bar should be enabled.</span></span>

<span data-ttu-id="1cfbe-110">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="1cfbe-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cfbe-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cfbe-111">Syntax</span></span>


```C++
HRESULT put_DisableConnectionBar(
  [in] VARIANT_BOOL fDisableConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="1cfbe-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1cfbe-112">Property value</span></span>

<span data-ttu-id="1cfbe-113">Especifica o novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="1cfbe-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cfbe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cfbe-114">Requirements</span></span>



| <span data-ttu-id="1cfbe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cfbe-115">Requirement</span></span> | <span data-ttu-id="1cfbe-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1cfbe-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfbe-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cfbe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1cfbe-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1cfbe-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1cfbe-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cfbe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1cfbe-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1cfbe-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="1cfbe-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1cfbe-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="1cfbe-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cfbe-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="1cfbe-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1cfbe-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cfbe-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cfbe-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="1cfbe-125">IID</span><span class="sxs-lookup"><span data-stu-id="1cfbe-125">IID</span></span><br/>                      | <span data-ttu-id="1cfbe-126">IID \_ IMsRdpClientNonScriptable5 é definido como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="1cfbe-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1cfbe-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cfbe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cfbe-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="1cfbe-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





