---
title: Códigos de erro (UIAutomationCoreApi. h)
description: Este tópico descreve os códigos de erro expostos pela automação da interface do usuário da Microsoft.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008792"
---
# <a name="error-codes-uiautomationcoreapih"></a><span data-ttu-id="169bb-103">Códigos de erro (UIAutomationCoreApi. h)</span><span class="sxs-lookup"><span data-stu-id="169bb-103">Error Codes (UIAutomationCoreApi.h)</span></span>

<span data-ttu-id="169bb-104">Este tópico descreve os códigos de erro expostos pela automação da interface do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="169bb-104">This topic describes the error codes exposed by Microsoft UI Automation.</span></span> <span data-ttu-id="169bb-105">A lista é classificada alfabeticamente por nome.</span><span class="sxs-lookup"><span data-stu-id="169bb-105">The list is sorted alphabetically by name.</span></span>



| <span data-ttu-id="169bb-106">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="169bb-106">Constant/value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="169bb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="169bb-107">Description</span></span>                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <span data-ttu-id="169bb-108"><dt>**UIA \_ E \_ ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="169bb-108"><dt>**UIA\_E\_ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span></span> </dl>          | <span data-ttu-id="169bb-109">Indica que um método foi chamado em um elemento virtualizado ou em um elemento que não existe mais, geralmente porque foi destruído.</span><span class="sxs-lookup"><span data-stu-id="169bb-109">Indicates that a method was called on a virtualized element, or on an element that no longer exists, usually because it has been destroyed.</span></span> <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <span data-ttu-id="169bb-110"><dt>**UIA \_ E \_ ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span><span class="sxs-lookup"><span data-stu-id="169bb-110"><dt>**UIA\_E\_ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span></span> </dl>                | <span data-ttu-id="169bb-111">Indica que um método que requer um elemento habilitado, como [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) ou [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), foi chamado em um elemento que foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="169bb-111">Indicates that a method that requires an enabled element, such as [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) or [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), was called on an element that was disabled.</span></span> <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <span data-ttu-id="169bb-112"><dt>**UIA \_ E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt></span><span class="sxs-lookup"><span data-stu-id="169bb-112"><dt>**UIA\_E\_INVALIDOPERATION**</dt> <dt>0x80131509</dt></span></span> </dl>                   | <span data-ttu-id="169bb-113">Indica que o método tentou uma operação que não era válida.</span><span class="sxs-lookup"><span data-stu-id="169bb-113">Indicates that the method attempted an operation that was not valid.</span></span><br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <span data-ttu-id="169bb-114"><dt>**UIA \_ E \_ NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="169bb-114"><dt>**UIA\_E\_NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span></span> </dl>                   | <span data-ttu-id="169bb-115">Indica que o método [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) foi chamado em um elemento que não tem um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="169bb-115">Indicates that the [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) method was called on an element that has no clickable point.</span></span><br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <span data-ttu-id="169bb-116"><dt>**UIA \_ E \_ sem suporte**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="169bb-116"><dt>**UIA\_E\_NOTSUPPORTED**</dt> <dt>0x80040204</dt></span></span> </dl>                               | <span data-ttu-id="169bb-117">Indica que o provedor não dá suporte explicitamente à propriedade ou ao padrão de controle especificado.</span><span class="sxs-lookup"><span data-stu-id="169bb-117">Indicates that the provider explicitly does not support the specified property or control pattern.</span></span> <span data-ttu-id="169bb-118">A automação da interface do usuário retornará esse código de erro para o chamador sem tentar fornecer um valor padrão ou fazer fallback para outro provedor.</span><span class="sxs-lookup"><span data-stu-id="169bb-118">UI Automation will return this error code to the caller without attempting to provide a default value or falling back to another provider.</span></span><br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <span data-ttu-id="169bb-119"><dt>**UIA \_ E \_ PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="169bb-119"><dt>**UIA\_E\_PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span></span> </dl> | <span data-ttu-id="169bb-120">Indica que ocorreu um problema ao carregar um assembly que contém um provedor do lado do cliente (proxy).</span><span class="sxs-lookup"><span data-stu-id="169bb-120">Indicates that a problem occurred when loading an assembly that contains a client-side (proxy) provider.</span></span><br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <span data-ttu-id="169bb-121"><dt>**UIA \_ E & 0x80131505 de \_ tempo limite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="169bb-121"><dt>**UIA\_E\_TIMEOUT**</dt> <dt>0x80131505</dt></span></span> </dl>                                                      | <span data-ttu-id="169bb-122">Indica que o tempo alocado para um processo ou uma operação expirou.</span><span class="sxs-lookup"><span data-stu-id="169bb-122">Indicates that the time allotted for a process or operation has expired.</span></span><br/>                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="169bb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="169bb-123">Requirements</span></span>



| <span data-ttu-id="169bb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="169bb-124">Requirement</span></span> | <span data-ttu-id="169bb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="169bb-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="169bb-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="169bb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="169bb-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="169bb-127">Windows XP \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="169bb-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="169bb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="169bb-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="169bb-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="169bb-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="169bb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="169bb-131"><dt>UIAutomationCoreApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="169bb-131"><dt>UIAutomationCoreApi.h</dt></span></span> </dl> |



 

 





