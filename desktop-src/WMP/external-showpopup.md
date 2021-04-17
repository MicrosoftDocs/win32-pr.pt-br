---
title: Método external. ShowPopup
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Método external. ShowPopup
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- método de pop-up Windows Media Player
- método de pop-up Windows Media Player, classe externa
- Classe externa Windows Media Player, método ShowPopup
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783602"
---
# <a name="externalshowpopup-method"></a><span data-ttu-id="6680c-107">Método external. ShowPopup</span><span class="sxs-lookup"><span data-stu-id="6680c-107">External.showPopup method</span></span>

> [!Note]  
> <span data-ttu-id="6680c-108">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="6680c-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6680c-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="6680c-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6680c-110">O método **ShowPopup** instrui o Windows Media Player a exibir uma página da Web pop-up; ou seja, uma página da Web que aparece em uma janela separada.</span><span class="sxs-lookup"><span data-stu-id="6680c-110">The **showPopup** method instructs Windows Media Player to display a pop-up webpage; that is, a webpage that appears in a separate window.</span></span>

## <a name="syntax"></a><span data-ttu-id="6680c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6680c-111">Syntax</span></span>


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a><span data-ttu-id="6680c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6680c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6680c-113">*PopupIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6680c-113">*PopupIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6680c-114">**Número** (**longo**) que especifica o índice da página da Web pop-up.</span><span class="sxs-lookup"><span data-stu-id="6680c-114">**Number** (**long**) that specifies the index of the pop-up webpage.</span></span>

</dd> <dt>

<span data-ttu-id="6680c-115">*Parâmetros* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="6680c-115">*Parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6680c-116">**Cadeia de caracteres** que o Windows Media Player acrescenta à URL da página da Web.</span><span class="sxs-lookup"><span data-stu-id="6680c-116">**String** that Windows Media Player appends to the URL of the webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6680c-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6680c-117">Return value</span></span>

<span data-ttu-id="6680c-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6680c-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6680c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6680c-119">Remarks</span></span>

<span data-ttu-id="6680c-120">O índice pop-up não é interpretado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6680c-120">The pop-up index is not interpreted by Windows Media Player.</span></span> <span data-ttu-id="6680c-121">Os índices que identificam páginas da Web pop-up são criados pela loja online e têm significado apenas para a loja online.</span><span class="sxs-lookup"><span data-stu-id="6680c-121">Indexes that identify pop-up webpages are created by the online store, and have meaning only to the online store.</span></span>

<span data-ttu-id="6680c-122">As etapas a seguir mostram como o Windows Media Player usa os parâmetros do método **ShowPopup** para criar uma URL para a janela pop-up.</span><span class="sxs-lookup"><span data-stu-id="6680c-122">The following steps show how Windows Media Player uses the parameters of the **showPopup** method to create a URL for the popup window.</span></span>

1.  <span data-ttu-id="6680c-123">O script em uma página de descoberta chama **Popup**, passando um inteiro em *PopupIndex* e uma cadeia de caracteres em *parâmetros*.</span><span class="sxs-lookup"><span data-stu-id="6680c-123">Script on a discovery page calls **showPopup**, passing an integer in *PopupIndex* and a string in *Parameters*.</span></span>

2.  <span data-ttu-id="6680c-124">O Windows Media Player passa o índice para [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) para recuperar a URL da página da Web a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="6680c-124">Windows Media Player passes the index to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to retrieve the URL of the webpage to be displayed.</span></span>

3.  <span data-ttu-id="6680c-125">O Windows Media Player acrescenta *parâmetros* à URL como uma cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="6680c-125">Windows Media Player appends *Parameters* to the URL as a query string.</span></span> <span data-ttu-id="6680c-126">Por exemplo, se **GetItemInfo** retornar " https://www.Proseware.com/Pages/Popup1.htm " e os *parâmetros* forem iguais a "DlgX = 800&DlgY = 400&greeting = Hi", o Windows Media Player criará a seguinte URL:</span><span class="sxs-lookup"><span data-stu-id="6680c-126">For example, if **GetItemInfo** returns "https://www.Proseware.com/Pages/Popup1.htm" and *Parameters* is equal to "DlgX=800&DlgY=400&Greeting=Hi", Windows Media Player creates the following URL:</span></span>

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

<span data-ttu-id="6680c-127">Você pode usar *parâmetros* para especificar o tamanho da janela pop-up.</span><span class="sxs-lookup"><span data-stu-id="6680c-127">You can use *Parameters* to specify the size of the pop-up window.</span></span> <span data-ttu-id="6680c-128">Por exemplo, se você definir *parâmetros* como "DlgX = 800&DlgY = 400", a janela pop-up terá um tamanho de 800 pixels por 400 pixels.</span><span class="sxs-lookup"><span data-stu-id="6680c-128">For example, if you set *Parameters* to "DlgX=800&DlgY=400", the pop-up window will have a size of 800 pixels by 400 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="6680c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6680c-129">Requirements</span></span>



| <span data-ttu-id="6680c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6680c-130">Requirement</span></span> | <span data-ttu-id="6680c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="6680c-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6680c-132">Versão</span><span class="sxs-lookup"><span data-stu-id="6680c-132">Version</span></span><br/> | <span data-ttu-id="6680c-133">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="6680c-133">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="6680c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6680c-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="6680c-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6680c-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6680c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="6680c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6680c-137">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="6680c-137">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





