---
description: Define o título e o subtítulo que aparecem no título do assistente. Em geral, o cliente exibirá o título acima do HTML e abaixo da barra de título.
title: Método WebWizardHost.SetHeaderText (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: d524f9ae6d1031d518e237d393bbb1dc0d35b2bd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841827"
---
# <a name="webwizardhostsetheadertext-method"></a><span data-ttu-id="142d0-104">Método WebWizardHost.SetHeaderText</span><span class="sxs-lookup"><span data-stu-id="142d0-104">WebWizardHost.SetHeaderText method</span></span>

<span data-ttu-id="142d0-105">Define o título e o subtítulo que aparecem no título do assistente.</span><span class="sxs-lookup"><span data-stu-id="142d0-105">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="142d0-106">Em geral, o cliente exibirá o título acima do HTML e abaixo da barra de título.</span><span class="sxs-lookup"><span data-stu-id="142d0-106">In general, the client will display the header above the HTML and below the title bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="142d0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="142d0-107">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a><span data-ttu-id="142d0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="142d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="142d0-109">*bstrHeaderTitle* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="142d0-109">*bstrHeaderTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="142d0-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="142d0-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="142d0-111">Cadeia de caracteres que contém o título.</span><span class="sxs-lookup"><span data-stu-id="142d0-111">String containing the title.</span></span>

</dd> <dt>

<span data-ttu-id="142d0-112">*bstrHeaderSubtitle* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="142d0-112">*bstrHeaderSubtitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="142d0-113">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="142d0-113">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="142d0-114">Cadeia de caracteres que contém o subtítulo.</span><span class="sxs-lookup"><span data-stu-id="142d0-114">String containing the subtitle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="142d0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="142d0-115">Requirements</span></span>



| <span data-ttu-id="142d0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="142d0-116">Requirement</span></span> | <span data-ttu-id="142d0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="142d0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="142d0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="142d0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="142d0-119">Somente \[ aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="142d0-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="142d0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="142d0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="142d0-121">Somente aplicativos da área de trabalho do Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="142d0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="142d0-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="142d0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="142d0-123"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="142d0-123"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="142d0-124">Idl</span><span class="sxs-lookup"><span data-stu-id="142d0-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="142d0-125"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="142d0-125"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 
