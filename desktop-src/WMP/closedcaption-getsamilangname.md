---
title: Método ClosedCaption. getSAMILangName
description: O método getSAMILangName recupera o nome de um idioma com suporte no arquivo SAMI atual.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- método getSAMILangName Windows Media Player
- método getSAMILangName Windows Media Player, classe ClosedCaption
- Classe ClosedCaption Windows Media Player, método getSAMILangName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd4b481de808ac8814e596cfc038aec38c7f19b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811342"
---
# <a name="closedcaptiongetsamilangname-method"></a><span data-ttu-id="f6511-106">Método ClosedCaption. getSAMILangName</span><span class="sxs-lookup"><span data-stu-id="f6511-106">ClosedCaption.getSAMILangName method</span></span>

<span data-ttu-id="f6511-107">O método **getSAMILangName** recupera o nome de um idioma com suporte no arquivo Sami atual.</span><span class="sxs-lookup"><span data-stu-id="f6511-107">The **getSAMILangName** method retrieves the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6511-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6511-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="f6511-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6511-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6511-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f6511-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6511-111">**Número** (**longo**) especificando o índice do nome do idioma a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="f6511-111">**Number** (**long**) specifying the index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6511-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6511-112">Return value</span></span>

<span data-ttu-id="f6511-113">Esse método retorna uma **cadeia de caracteres** que contém o nome do idioma, conforme especificado no arquivo Sami.</span><span class="sxs-lookup"><span data-stu-id="f6511-113">This method returns a **String** containing the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6511-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6511-114">Remarks</span></span>

<span data-ttu-id="f6511-115">Os idiomas em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.</span><span class="sxs-lookup"><span data-stu-id="f6511-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="f6511-116">Esse método não pode ser usado até que um arquivo de mídia digital esteja aberto (*Player*.**OpenState** é igual a 13).</span><span class="sxs-lookup"><span data-stu-id="f6511-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="f6511-117">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="f6511-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6511-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6511-118">Requirements</span></span>



| <span data-ttu-id="f6511-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6511-119">Requirement</span></span> | <span data-ttu-id="f6511-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f6511-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6511-121">Versão</span><span class="sxs-lookup"><span data-stu-id="f6511-121">Version</span></span><br/> | <span data-ttu-id="f6511-122">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f6511-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f6511-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f6511-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="f6511-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6511-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6511-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6511-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6511-126">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="f6511-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="f6511-127">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="f6511-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="f6511-128">**ClosedCaption.SAMILang**</span><span class="sxs-lookup"><span data-stu-id="f6511-128">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





