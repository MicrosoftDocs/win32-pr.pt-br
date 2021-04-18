---
title: Método ClosedCaption. getSAMILangID
description: O método getSAMILangID recupera o identificador de localidade (LCID) de um idioma com suporte do arquivo SAMI atual.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- método getSAMILangID Windows Media Player
- método getSAMILangID Windows Media Player, classe ClosedCaption
- Classe ClosedCaption Windows Media Player, método getSAMILangID
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd543c9cb9d884022d78a875a2f8de078c479b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760458"
---
# <a name="closedcaptiongetsamilangid-method"></a><span data-ttu-id="74563-106">Método ClosedCaption. getSAMILangID</span><span class="sxs-lookup"><span data-stu-id="74563-106">ClosedCaption.getSAMILangID method</span></span>

<span data-ttu-id="74563-107">O método **getSAMILangID** recupera o identificador de localidade (LCID) de um idioma com suporte do arquivo Sami atual.</span><span class="sxs-lookup"><span data-stu-id="74563-107">The **getSAMILangID** method retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="74563-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74563-108">Syntax</span></span>


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="74563-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74563-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74563-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="74563-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74563-111">**Número** (**longo**) ESPECIFICANDO o índice do LCID a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="74563-111">**Number** (**long**) specifying the index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74563-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74563-112">Return value</span></span>

<span data-ttu-id="74563-113">Esse método retorna um **número** (**Long**) que contém o LCID do idioma com o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="74563-113">This method returns a **Number** (**long**) containing the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="74563-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="74563-114">Remarks</span></span>

<span data-ttu-id="74563-115">Os idiomas em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.</span><span class="sxs-lookup"><span data-stu-id="74563-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="74563-116">Esse método não pode ser usado até que um arquivo de mídia digital esteja aberto (*Player*.**OpenState** é igual a 13).</span><span class="sxs-lookup"><span data-stu-id="74563-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="74563-117">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="74563-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="74563-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74563-118">Requirements</span></span>



| <span data-ttu-id="74563-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="74563-119">Requirement</span></span> | <span data-ttu-id="74563-120">Valor</span><span class="sxs-lookup"><span data-stu-id="74563-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="74563-121">Versão</span><span class="sxs-lookup"><span data-stu-id="74563-121">Version</span></span><br/> | <span data-ttu-id="74563-122">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="74563-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="74563-123">DLL</span><span class="sxs-lookup"><span data-stu-id="74563-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="74563-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74563-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74563-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="74563-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74563-126">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="74563-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="74563-127">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="74563-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





