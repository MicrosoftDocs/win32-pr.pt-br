---
description: Define o título e o subtítulo que aparecem no cabeçalho do assistente. Em geral, o cliente exibirá o cabeçalho acima do HTML e abaixo da barra de título.
title: Método WebWizardHost. setheadertext (shldisp. h)
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
ms.openlocfilehash: 92e23fab94cfedd8bbc62e31086759af48238a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968076"
---
# <a name="webwizardhostsetheadertext-method"></a><span data-ttu-id="f4952-104">Método WebWizardHost. setheadertext</span><span class="sxs-lookup"><span data-stu-id="f4952-104">WebWizardHost.SetHeaderText method</span></span>

<span data-ttu-id="f4952-105">Define o título e o subtítulo que aparecem no cabeçalho do assistente.</span><span class="sxs-lookup"><span data-stu-id="f4952-105">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="f4952-106">Em geral, o cliente exibirá o cabeçalho acima do HTML e abaixo da barra de título.</span><span class="sxs-lookup"><span data-stu-id="f4952-106">In general, the client will display the header above the HTML and below the title bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4952-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4952-107">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a><span data-ttu-id="f4952-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4952-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4952-109">*bstrHeaderTitle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4952-109">*bstrHeaderTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4952-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f4952-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f4952-111">Cadeia de caracteres que contém o título.</span><span class="sxs-lookup"><span data-stu-id="f4952-111">String containing the title.</span></span>

</dd> <dt>

<span data-ttu-id="f4952-112">*bstrHeaderSubtitle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4952-112">*bstrHeaderSubtitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4952-113">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f4952-113">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f4952-114">Cadeia de caracteres que contém o subtítulo.</span><span class="sxs-lookup"><span data-stu-id="f4952-114">String containing the subtitle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4952-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4952-115">Requirements</span></span>



| <span data-ttu-id="f4952-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4952-116">Requirement</span></span> | <span data-ttu-id="f4952-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f4952-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4952-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4952-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f4952-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f4952-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f4952-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4952-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f4952-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f4952-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f4952-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4952-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4952-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4952-123"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f4952-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="f4952-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f4952-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4952-125"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 
