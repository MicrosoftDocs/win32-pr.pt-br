---
description: Atualiza os botões Voltar, Próximo e Concluir no quadro do assistente do cliente.
title: Método WebWizardHost.SetWizardButtons (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: a1b2a79c7ea323c36371e08d3519e71e4c537935
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842617"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="17b2f-103">Método WebWizardHost.SetWizardButtons</span><span class="sxs-lookup"><span data-stu-id="17b2f-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="17b2f-104">Atualiza os **botões Voltar,** **Próximo** **e** Concluir no quadro do assistente do cliente.</span><span class="sxs-lookup"><span data-stu-id="17b2f-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b2f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17b2f-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="17b2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17b2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b2f-107">*vbEnableBack* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="17b2f-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b2f-108">Tipo: **booliana**</span><span class="sxs-lookup"><span data-stu-id="17b2f-108">Type: **Boolean**</span></span>

<span data-ttu-id="17b2f-109">Habilita o **botão** Voltar.</span><span class="sxs-lookup"><span data-stu-id="17b2f-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="17b2f-110">*vbEnableNext* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="17b2f-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b2f-111">Tipo: **booliana**</span><span class="sxs-lookup"><span data-stu-id="17b2f-111">Type: **Boolean**</span></span>

<span data-ttu-id="17b2f-112">Habilita botão **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="17b2f-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="17b2f-113">*vbLastPage* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="17b2f-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b2f-114">Tipo: **booliana**</span><span class="sxs-lookup"><span data-stu-id="17b2f-114">Type: **Boolean**</span></span>

<span data-ttu-id="17b2f-115">Habilita o **botão** Concluir.</span><span class="sxs-lookup"><span data-stu-id="17b2f-115">Enables the **Finish** button.</span></span> <span data-ttu-id="17b2f-116">Declara que esta é a última página do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="17b2f-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17b2f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="17b2f-117">Remarks</span></span>

<span data-ttu-id="17b2f-118">Certifique-se de implementar funções de manipulador em cada página do lado do servidor para OnBack() e OnNext(), correspondentes aos botões do assistente **Voltar** e **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="17b2f-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="17b2f-119">As funções OnBack() e OnNext() respondem a **SetWizardButtons.**</span><span class="sxs-lookup"><span data-stu-id="17b2f-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="17b2f-120">No momento apropriado, a função OnNext() chama **SetWizardButtons** com *vbLastPage* = **true,** que pode habilitar um **botão** Concluir.</span><span class="sxs-lookup"><span data-stu-id="17b2f-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="17b2f-121">OnNext() também chama [**FinalNext**](iwebwizardhost-finalnext.md) quando um usuário clica no **botão** Concluir.</span><span class="sxs-lookup"><span data-stu-id="17b2f-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b2f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17b2f-122">Requirements</span></span>



| <span data-ttu-id="17b2f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b2f-123">Requirement</span></span> | <span data-ttu-id="17b2f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="17b2f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17b2f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17b2f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="17b2f-126">Somente \[ aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="17b2f-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="17b2f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17b2f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="17b2f-128">Somente aplicativos da área de trabalho do Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="17b2f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="17b2f-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17b2f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="17b2f-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="17b2f-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="17b2f-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="17b2f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17b2f-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17b2f-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




