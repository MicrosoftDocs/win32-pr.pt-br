---
description: Atualiza os botões voltar, avançar e concluir no quadro do assistente do cliente.
title: Método WebWizardHost. SetWizardButtons (shldisp. h)
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
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968075"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="9d8a4-103">Método WebWizardHost. SetWizardButtons</span><span class="sxs-lookup"><span data-stu-id="9d8a4-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="9d8a4-104">Atualiza os botões **voltar**, **Avançar** e **concluir** no quadro do assistente do cliente.</span><span class="sxs-lookup"><span data-stu-id="9d8a4-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d8a4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d8a4-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="9d8a4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d8a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d8a4-107">*vbEnableBack* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d8a4-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d8a4-108">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9d8a4-108">Type: **Boolean**</span></span>

<span data-ttu-id="9d8a4-109">Habilita o botão **voltar** .</span><span class="sxs-lookup"><span data-stu-id="9d8a4-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="9d8a4-110">*vbEnableNext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d8a4-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d8a4-111">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9d8a4-111">Type: **Boolean**</span></span>

<span data-ttu-id="9d8a4-112">Habilita botão **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9d8a4-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="9d8a4-113">*vbLastPage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d8a4-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d8a4-114">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9d8a4-114">Type: **Boolean**</span></span>

<span data-ttu-id="9d8a4-115">Habilita o botão **concluir** .</span><span class="sxs-lookup"><span data-stu-id="9d8a4-115">Enables the **Finish** button.</span></span> <span data-ttu-id="9d8a4-116">Declara que esta é a última página do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="9d8a4-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d8a4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d8a4-117">Remarks</span></span>

<span data-ttu-id="9d8a4-118">Certifique-se de implementar funções de manipulador em cada página do lado do servidor para onback () e OnNext (), correspondente aos botões do assistente de **volta** e **próximo**.</span><span class="sxs-lookup"><span data-stu-id="9d8a4-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="9d8a4-119">As funções onback () e OnNext () respondem a **SetWizardButtons**.</span><span class="sxs-lookup"><span data-stu-id="9d8a4-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="9d8a4-120">No momento apropriado, a função OnNext () chama **SetWizardButtons** com *vbLastPage* = **true**, que pode habilitar um botão **concluir** .</span><span class="sxs-lookup"><span data-stu-id="9d8a4-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="9d8a4-121">OnNext () também chama [**FinalNext**](iwebwizardhost-finalnext.md) quando um usuário clica no botão **concluir** .</span><span class="sxs-lookup"><span data-stu-id="9d8a4-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d8a4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d8a4-122">Requirements</span></span>



| <span data-ttu-id="9d8a4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d8a4-123">Requirement</span></span> | <span data-ttu-id="9d8a4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9d8a4-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d8a4-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d8a4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9d8a4-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9d8a4-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9d8a4-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d8a4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9d8a4-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9d8a4-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9d8a4-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d8a4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d8a4-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d8a4-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d8a4-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="9d8a4-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9d8a4-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d8a4-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




