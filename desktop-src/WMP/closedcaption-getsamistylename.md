---
title: Método ClosedCaption. getSAMIStyleName
description: O método getSAMIStyleName recupera o nome de um estilo com suporte no arquivo SAMI atual.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- método getSAMIStyleName Windows Media Player
- método getSAMIStyleName Windows Media Player, classe ClosedCaption
- Classe ClosedCaption Windows Media Player, método getSAMIStyleName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813372"
---
# <a name="closedcaptiongetsamistylename-method"></a><span data-ttu-id="5ab5a-106">Método ClosedCaption. getSAMIStyleName</span><span class="sxs-lookup"><span data-stu-id="5ab5a-106">ClosedCaption.getSAMIStyleName method</span></span>

<span data-ttu-id="5ab5a-107">O método **getSAMIStyleName** recupera o nome de um estilo com suporte no arquivo Sami atual.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-107">The **getSAMIStyleName** method retrieves the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab5a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ab5a-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="5ab5a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ab5a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ab5a-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5ab5a-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab5a-111">**Número** (**longo**) especificando o índice do nome do estilo a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-111">**Number** (**long**) specifying the index of the style name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ab5a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ab5a-112">Return value</span></span>

<span data-ttu-id="5ab5a-113">Esse método retorna uma **cadeia de caracteres** que contém o nome do estilo, conforme especificado no arquivo Sami.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-113">This method returns a **String** containing the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ab5a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ab5a-114">Remarks</span></span>

<span data-ttu-id="5ab5a-115">Os estilos em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="5ab5a-116">Esse método não pode ser usado até que um arquivo de mídia digital esteja aberto (*Player*.**OpenState** é igual a 13).</span><span class="sxs-lookup"><span data-stu-id="5ab5a-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="5ab5a-117">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ab5a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ab5a-118">Requirements</span></span>



| <span data-ttu-id="5ab5a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ab5a-119">Requirement</span></span> | <span data-ttu-id="5ab5a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5ab5a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab5a-121">Versão</span><span class="sxs-lookup"><span data-stu-id="5ab5a-121">Version</span></span><br/> | <span data-ttu-id="5ab5a-122">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5ab5a-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="5ab5a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5ab5a-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ab5a-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ab5a-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ab5a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ab5a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab5a-126">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="5ab5a-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="5ab5a-127">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="5ab5a-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="5ab5a-128">**ClosedCaption. SAMIstyle**</span><span class="sxs-lookup"><span data-stu-id="5ab5a-128">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





