---
title: Método external. download
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método de download inicia o download de um conjunto de itens de mídia.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- método de download do Windows Media Player
- método de download do Windows Media Player, classe externa
- Classe externa Windows Media Player, método de download
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789544"
---
# <a name="externaldownload-method"></a><span data-ttu-id="1e148-108">Método external. download</span><span class="sxs-lookup"><span data-stu-id="1e148-108">External.download method</span></span>

> [!Note]  
> <span data-ttu-id="1e148-109">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="1e148-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1e148-110">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="1e148-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1e148-111">O método de **Download** inicia o download de um conjunto de itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="1e148-111">The **download** method initiates the download of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e148-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e148-112">Syntax</span></span>


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a><span data-ttu-id="1e148-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e148-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e148-114">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="1e148-114">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e148-115">Uma [constante de local de biblioteca](library-location-constants.md) que especifica o tipo de item a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="1e148-115">A [library location constant](library-location-constants.md) that specifies the type of item to be downloaded.</span></span> <span data-ttu-id="1e148-116">Por exemplo, CPTrackID especifica que uma ou mais faixas devem ser baixadas.</span><span class="sxs-lookup"><span data-stu-id="1e148-116">For example, CPTrackID specifies that one or more tracks are to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="1e148-117">*IDs* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1e148-117">*IDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e148-118">**Cadeia de caracteres** que contém as IDs, delimitada por ponto e vírgula, dos itens de mídia a serem baixados.</span><span class="sxs-lookup"><span data-stu-id="1e148-118">**String** containing the IDs, delimited by semicolons, of the media items to be downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e148-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e148-119">Return value</span></span>

<span data-ttu-id="1e148-120">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1e148-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e148-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e148-121">Requirements</span></span>



| <span data-ttu-id="1e148-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e148-122">Requirement</span></span> | <span data-ttu-id="1e148-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1e148-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e148-124">Versão</span><span class="sxs-lookup"><span data-stu-id="1e148-124">Version</span></span><br/> | <span data-ttu-id="1e148-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="1e148-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="1e148-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1e148-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="1e148-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e148-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e148-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e148-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e148-129">**Baixando conteúdo de mídia**</span><span class="sxs-lookup"><span data-stu-id="1e148-129">**Downloading Media Content**</span></span>](downloading-media-content.md)
</dt> <dt>

[<span data-ttu-id="1e148-130">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="1e148-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="1e148-131">**Externo. comprar**</span><span class="sxs-lookup"><span data-stu-id="1e148-131">**External.buy**</span></span>](external-buy.md)
</dt> <dt>

[<span data-ttu-id="1e148-132">**IWMPContentPartner::D aixar**</span><span class="sxs-lookup"><span data-stu-id="1e148-132">**IWMPContentPartner::Download**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





