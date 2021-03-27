---
description: Expõe métodos que habilitam páginas HTML que são hospedadas em uma extensão de assistente para se comunicar com o assistente.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Objeto WebWizardHost (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 1fbaf53db11fda577e9e9c5384af5f7c62fe1944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921659"
---
# <a name="webwizardhost-object"></a><span data-ttu-id="062c4-103">Objeto WebWizardHost</span><span class="sxs-lookup"><span data-stu-id="062c4-103">WebWizardHost object</span></span>

<span data-ttu-id="062c4-104">Expõe métodos que habilitam páginas HTML que são hospedadas em uma extensão de assistente para se comunicar com o assistente.</span><span class="sxs-lookup"><span data-stu-id="062c4-104">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span>

## <a name="members"></a><span data-ttu-id="062c4-105">Membros</span><span class="sxs-lookup"><span data-stu-id="062c4-105">Members</span></span>

<span data-ttu-id="062c4-106">O objeto **WebWizardHost** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="062c4-106">The **WebWizardHost** object has these types of members:</span></span>

-   [<span data-ttu-id="062c4-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="062c4-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="062c4-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="062c4-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="062c4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="062c4-109">Methods</span></span>

<span data-ttu-id="062c4-110">O objeto **WebWizardHost** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="062c4-110">The **WebWizardHost** object has these methods.</span></span>



| <span data-ttu-id="062c4-111">Método</span><span class="sxs-lookup"><span data-stu-id="062c4-111">Method</span></span>                                                      | <span data-ttu-id="062c4-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="062c4-112">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="062c4-113">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="062c4-113">**Cancel**</span></span>](iwebwizardhost-cancel.md)                     | <span data-ttu-id="062c4-114">Simula um clique no botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="062c4-114">Simulates a **Cancel** button click.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="062c4-115">**FinalBack**</span><span class="sxs-lookup"><span data-stu-id="062c4-115">**FinalBack**</span></span>](iwebwizardhost-finalback.md)               | <span data-ttu-id="062c4-116">Navega até a página do lado do cliente imediatamente antes da página que hospeda as páginas HTML do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="062c4-116">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span><br/>                                                                    |
| [<span data-ttu-id="062c4-117">**FinalNext**</span><span class="sxs-lookup"><span data-stu-id="062c4-117">**FinalNext**</span></span>](iwebwizardhost-finalnext.md)               | <span data-ttu-id="062c4-118">Navega até a página do assistente do lado do cliente que segue a página que hospeda as páginas HTML do lado do servidor ou conclui o assistente se não houver outras páginas do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="062c4-118">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span><br/> |
| [<span data-ttu-id="062c4-119">**Setheadertext**</span><span class="sxs-lookup"><span data-stu-id="062c4-119">**SetHeaderText**</span></span>](iwebwizardhost-setheadertext.md)       | <span data-ttu-id="062c4-120">Define o título e o subtítulo que aparecem no cabeçalho do assistente.</span><span class="sxs-lookup"><span data-stu-id="062c4-120">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="062c4-121">Em geral, o cliente exibirá o cabeçalho acima do HTML e abaixo da barra de título.</span><span class="sxs-lookup"><span data-stu-id="062c4-121">In general, the client will display the header above the HTML and below the title bar.</span></span><br/>                    |
| [<span data-ttu-id="062c4-122">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="062c4-122">**SetWizardButtons**</span></span>](iwebwizardhost-setwizardbuttons.md) | <span data-ttu-id="062c4-123">Atualiza os botões **voltar**, **Avançar** e **concluir** no quadro do assistente do cliente.</span><span class="sxs-lookup"><span data-stu-id="062c4-123">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="062c4-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="062c4-124">Properties</span></span>

<span data-ttu-id="062c4-125">O objeto **WebWizardHost** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="062c4-125">The **WebWizardHost** object has these properties.</span></span>



| <span data-ttu-id="062c4-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="062c4-126">Property</span></span>                                               | <span data-ttu-id="062c4-127">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="062c4-127">Access type</span></span>           | <span data-ttu-id="062c4-128">Description</span><span class="sxs-lookup"><span data-stu-id="062c4-128">Description</span></span>                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="062c4-129">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="062c4-129">**Caption**</span></span>](iwebwizardhost-caption.md)<br/>   | <span data-ttu-id="062c4-130">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="062c4-130">Read/write</span></span><br/> | <span data-ttu-id="062c4-131">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="062c4-131">Not implemented.</span></span><br/>                              |
| [<span data-ttu-id="062c4-132">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="062c4-132">**Property**</span></span>](iwebwizardhost-property.md)<br/> | <span data-ttu-id="062c4-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="062c4-133">Read/write</span></span><br/> | <span data-ttu-id="062c4-134">Define ou recupera o valor atual de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="062c4-134">Sets or retrieves a property's current value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="062c4-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="062c4-135">Requirements</span></span>



| <span data-ttu-id="062c4-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="062c4-136">Requirement</span></span> | <span data-ttu-id="062c4-137">Valor</span><span class="sxs-lookup"><span data-stu-id="062c4-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="062c4-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="062c4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="062c4-139">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="062c4-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="062c4-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="062c4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="062c4-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="062c4-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="062c4-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="062c4-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="062c4-143"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="062c4-143"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="062c4-144">INSERI</span><span class="sxs-lookup"><span data-stu-id="062c4-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="062c4-145"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="062c4-145"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="062c4-146">IID</span><span class="sxs-lookup"><span data-stu-id="062c4-146">IID</span></span><br/>                      | <span data-ttu-id="062c4-147">\_WEBWIZARDHOST CLSID</span><span class="sxs-lookup"><span data-stu-id="062c4-147">CLSID\_WebWizardHost</span></span><br/>                                                        |



 

 




