---
title: Evento Player. DomainChange
description: O evento DomainChange ocorre quando o domínio do DVD é alterado. | Evento Player. DomainChange
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Evento DomainChange do Windows Media Player
- Evento DomainChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento DomainChange
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814070"
---
# <a name="playerdomainchange-event"></a><span data-ttu-id="bc394-107">Evento Player. DomainChange</span><span class="sxs-lookup"><span data-stu-id="bc394-107">Player.DomainChange event</span></span>

<span data-ttu-id="bc394-108">O evento **DomainChange** ocorre quando o domínio do DVD é alterado.</span><span class="sxs-lookup"><span data-stu-id="bc394-108">The **DomainChange** event occurs when the DVD domain changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc394-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc394-109">Syntax</span></span>


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a><span data-ttu-id="bc394-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc394-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc394-111">*strDomain*</span><span class="sxs-lookup"><span data-stu-id="bc394-111">*strDomain*</span></span> 
</dt> <dd>

<span data-ttu-id="bc394-112">**Cadeia de caracteres** que indica o novo domínio.</span><span class="sxs-lookup"><span data-stu-id="bc394-112">**String** indicating the new domain.</span></span> <span data-ttu-id="bc394-113">Contém um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="bc394-113">Contains one of the following values.</span></span>



| <span data-ttu-id="bc394-114">String</span><span class="sxs-lookup"><span data-stu-id="bc394-114">String</span></span>            | <span data-ttu-id="bc394-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc394-115">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="bc394-116">firstplay</span><span class="sxs-lookup"><span data-stu-id="bc394-116">firstplay</span></span>         | <span data-ttu-id="bc394-117">Executando a inicialização padrão de um disco de DVD.</span><span class="sxs-lookup"><span data-stu-id="bc394-117">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="bc394-118">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="bc394-118">videoManagerMenu</span></span>  | <span data-ttu-id="bc394-119">Exibindo menus para o disco inteiro. Também conhecido como menu raiz ou topMenu.</span><span class="sxs-lookup"><span data-stu-id="bc394-119">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="bc394-120">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="bc394-120">videoTitleSetMenu</span></span> | <span data-ttu-id="bc394-121">Exibindo menus para o conjunto de títulos atual.</span><span class="sxs-lookup"><span data-stu-id="bc394-121">Displaying menus for current title set.</span></span> <span data-ttu-id="bc394-122">Também conhecido como titleMenu.</span><span class="sxs-lookup"><span data-stu-id="bc394-122">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="bc394-123">título</span><span class="sxs-lookup"><span data-stu-id="bc394-123">title</span></span>             | <span data-ttu-id="bc394-124">Exibindo o título atual.</span><span class="sxs-lookup"><span data-stu-id="bc394-124">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="bc394-125">parar</span><span class="sxs-lookup"><span data-stu-id="bc394-125">stop</span></span>              | <span data-ttu-id="bc394-126">O navegador de DVD está no domínio de parada de DVD.</span><span class="sxs-lookup"><span data-stu-id="bc394-126">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc394-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc394-127">Return value</span></span>

<span data-ttu-id="bc394-128">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bc394-128">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc394-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc394-129">Remarks</span></span>

<span data-ttu-id="bc394-130">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="bc394-130">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="bc394-131">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="bc394-131">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="bc394-132">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="bc394-132">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc394-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc394-133">Requirements</span></span>



| <span data-ttu-id="bc394-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc394-134">Requirement</span></span> | <span data-ttu-id="bc394-135">Valor</span><span class="sxs-lookup"><span data-stu-id="bc394-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bc394-136">Versão</span><span class="sxs-lookup"><span data-stu-id="bc394-136">Version</span></span><br/> | <span data-ttu-id="bc394-137">Windows Media Player para Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="bc394-137">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="bc394-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bc394-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="bc394-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc394-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc394-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc394-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc394-141">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="bc394-141">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="bc394-142">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="bc394-142">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





