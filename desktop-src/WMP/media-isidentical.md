---
title: Método Media. isidêntico
description: O método isidêntico recupera um valor que indica se o objeto fornecido é o mesmo que o atual. | Método Media. isidêntico
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- método isidêntico do Windows Media Player
- método isidêntico Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método isidêntico
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810682"
---
# <a name="mediaisidentical-method"></a><span data-ttu-id="5ad5d-107">Método Media. isidêntico</span><span class="sxs-lookup"><span data-stu-id="5ad5d-107">Media.isIdentical method</span></span>

<span data-ttu-id="5ad5d-108">O método **isidêntico** recupera um valor que indica se o objeto fornecido é o mesmo que o atual.</span><span class="sxs-lookup"><span data-stu-id="5ad5d-108">The **isIdentical** method retrieves a value indicating whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad5d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ad5d-109">Syntax</span></span>


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a><span data-ttu-id="5ad5d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ad5d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ad5d-111">*mídia* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ad5d-111">*media* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad5d-112">Objeto de **mídia** a ser comparado com o objeto de **mídia** atual.</span><span class="sxs-lookup"><span data-stu-id="5ad5d-112">**Media** object to compare with the current **Media** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ad5d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ad5d-113">Return value</span></span>

<span data-ttu-id="5ad5d-114">Esse método retorna um **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="5ad5d-114">This method returns a **Boolean**.</span></span>

## <a name="examples"></a><span data-ttu-id="5ad5d-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5ad5d-115">Examples</span></span>

<span data-ttu-id="5ad5d-116">O exemplo de JScript a seguir usa *mídia*. **isidêntico** para verificar se um item de mídia chamado newMedia é o mesmo que o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="5ad5d-116">The following JScript example uses *Media*.**isIdentical** to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="5ad5d-117">Se eles não forem iguais, o novo item de mídia será reproduzido.</span><span class="sxs-lookup"><span data-stu-id="5ad5d-117">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="5ad5d-118">Caso contrário, a mídia atual continuará a ser executada sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="5ad5d-118">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="5ad5d-119">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5ad5d-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a><span data-ttu-id="5ad5d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ad5d-120">Requirements</span></span>



| <span data-ttu-id="5ad5d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ad5d-121">Requirement</span></span> | <span data-ttu-id="5ad5d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5ad5d-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad5d-123">Versão</span><span class="sxs-lookup"><span data-stu-id="5ad5d-123">Version</span></span><br/> | <span data-ttu-id="5ad5d-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5ad5d-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5ad5d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5ad5d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ad5d-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ad5d-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ad5d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ad5d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad5d-128">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="5ad5d-128">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





