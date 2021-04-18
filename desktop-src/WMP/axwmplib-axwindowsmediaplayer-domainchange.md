---
title: Evento DomainChange do objeto AxWindowsMediaPlayer
description: O evento DomainChange ocorre quando o domínio do DVD é alterado. | Evento DomainChange do objeto AxWindowsMediaPlayer
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Evento DomainChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784918"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="53a61-105">Evento DomainChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="53a61-105">DomainChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="53a61-106">O evento DomainChange ocorre quando o domínio do DVD é alterado.</span><span class="sxs-lookup"><span data-stu-id="53a61-106">The DomainChange event occurs when the DVD domain changes.</span></span>

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a><span data-ttu-id="53a61-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="53a61-107">Event Data</span></span>

<span data-ttu-id="53a61-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="53a61-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEventHandler**.</span></span> <span data-ttu-id="53a61-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="53a61-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="53a61-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="53a61-110">Property</span></span>  | <span data-ttu-id="53a61-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="53a61-111">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53a61-112">strDomain</span><span class="sxs-lookup"><span data-stu-id="53a61-112">strDomain</span></span> | <span data-ttu-id="53a61-113">System. StringIndicates o novo domínio.</span><span class="sxs-lookup"><span data-stu-id="53a61-113">System.StringIndicates the new domain.</span></span> <span data-ttu-id="53a61-114">Para obter os valores possíveis, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="53a61-114">For possible values, see the Remarks section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="53a61-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="53a61-115">Remarks</span></span>

<span data-ttu-id="53a61-116">A tabela a seguir mostra os valores possíveis para a propriedade strDomain.</span><span class="sxs-lookup"><span data-stu-id="53a61-116">The following table shows the possible values for the strDomain property.</span></span>



| <span data-ttu-id="53a61-117">String</span><span class="sxs-lookup"><span data-stu-id="53a61-117">String</span></span>            | <span data-ttu-id="53a61-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="53a61-118">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="53a61-119">firstPlay</span><span class="sxs-lookup"><span data-stu-id="53a61-119">firstPlay</span></span>         | <span data-ttu-id="53a61-120">Executando a inicialização padrão de um disco de DVD.</span><span class="sxs-lookup"><span data-stu-id="53a61-120">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="53a61-121">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="53a61-121">videoManagerMenu</span></span>  | <span data-ttu-id="53a61-122">Exibindo menus para o disco inteiro. Também conhecido como menu raiz ou topMenu.</span><span class="sxs-lookup"><span data-stu-id="53a61-122">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="53a61-123">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="53a61-123">videoTitleSetMenu</span></span> | <span data-ttu-id="53a61-124">Exibindo menus para o conjunto de títulos atual.</span><span class="sxs-lookup"><span data-stu-id="53a61-124">Displaying menus for current title set.</span></span> <span data-ttu-id="53a61-125">Também conhecido como titleMenu.</span><span class="sxs-lookup"><span data-stu-id="53a61-125">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="53a61-126">título</span><span class="sxs-lookup"><span data-stu-id="53a61-126">title</span></span>             | <span data-ttu-id="53a61-127">Exibindo o título atual.</span><span class="sxs-lookup"><span data-stu-id="53a61-127">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="53a61-128">parar</span><span class="sxs-lookup"><span data-stu-id="53a61-128">stop</span></span>              | <span data-ttu-id="53a61-129">O navegador de DVD está no domínio de parada de DVD.</span><span class="sxs-lookup"><span data-stu-id="53a61-129">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

## <a name="requirements"></a><span data-ttu-id="53a61-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53a61-130">Requirements</span></span>



| <span data-ttu-id="53a61-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="53a61-131">Requirement</span></span> | <span data-ttu-id="53a61-132">Valor</span><span class="sxs-lookup"><span data-stu-id="53a61-132">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53a61-133">Versão</span><span class="sxs-lookup"><span data-stu-id="53a61-133">Version</span></span><br/>   | <span data-ttu-id="53a61-134">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="53a61-134">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="53a61-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="53a61-135">Namespace</span></span><br/> | <span data-ttu-id="53a61-136">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="53a61-136">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="53a61-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="53a61-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="53a61-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="53a61-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53a61-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="53a61-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a61-140">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="53a61-140">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="53a61-141">**Interface IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="53a61-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





