---
description: Gerado pelo mecanismo de política quando a individualização está prestes a começar. A individualização é executada usando a implementação de aplicativos da interface IMFContentProtectionManager.
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: Evento MEIndividualizationStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb8d50bbc2081c4efa41d8b15cc3e41a14ab5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762853"
---
# <a name="meindividualizationstart-event"></a><span data-ttu-id="5bc2f-104">Evento MEIndividualizationStart</span><span class="sxs-lookup"><span data-stu-id="5bc2f-104">MEIndividualizationStart event</span></span>

<span data-ttu-id="5bc2f-105">Gerado pelo mecanismo de política quando a individualização está prestes a começar.</span><span class="sxs-lookup"><span data-stu-id="5bc2f-105">Raised by the policy engine when individualization is about to begin.</span></span> <span data-ttu-id="5bc2f-106">A individualização é executada usando a implementação do aplicativo da interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .</span><span class="sxs-lookup"><span data-stu-id="5bc2f-106">Individualization is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="5bc2f-107">Um aplicativo individual é aquele que recebeu uma atualização para seus componentes de DRM (gerenciamento de direitos digitais) que o diferencia de todas as outras cópias do mesmo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5bc2f-107">An individualized application is one that has received an upgrade to its digital rights management (DRM) components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="5bc2f-108">Os proprietários de conteúdo podem exigir que seus arquivos protegidos sejam reproduzidos somente em um aplicativo que tenha sido individualizado.</span><span class="sxs-lookup"><span data-stu-id="5bc2f-108">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

## <a name="event-values"></a><span data-ttu-id="5bc2f-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="5bc2f-109">Event values</span></span>

<span data-ttu-id="5bc2f-110">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="5bc2f-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5bc2f-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5bc2f-111">VARTYPE</span></span>              | <span data-ttu-id="5bc2f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bc2f-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5bc2f-113">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="5bc2f-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5bc2f-114">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="5bc2f-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5bc2f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bc2f-115">Remarks</span></span>

<span data-ttu-id="5bc2f-116">Quando a aquisição de licença é concluída, o mecanismo de política gera o evento [MEIndividualizationCompleted](meindividualizationcompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="5bc2f-116">When license acquisition is completed, the policy engine raises the [MEIndividualizationCompleted](meindividualizationcompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc2f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bc2f-117">Requirements</span></span>



| <span data-ttu-id="5bc2f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc2f-118">Requirement</span></span> | <span data-ttu-id="5bc2f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5bc2f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc2f-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bc2f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc2f-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bc2f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5bc2f-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bc2f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc2f-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5bc2f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5bc2f-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5bc2f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bc2f-125"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bc2f-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bc2f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bc2f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc2f-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5bc2f-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




