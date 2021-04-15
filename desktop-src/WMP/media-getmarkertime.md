---
title: Método Media. getmarcadortime
description: O método getmarcadortime recupera a hora do marcador no índice especificado.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- método getmarcadortime Windows Media Player
- método getmarcadortime Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método getmarcadortime
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761192"
---
# <a name="mediagetmarkertime-method"></a><span data-ttu-id="d0e12-106">Método Media. getmarcadortime</span><span class="sxs-lookup"><span data-stu-id="d0e12-106">Media.getMarkerTime method</span></span>

<span data-ttu-id="d0e12-107">O método **Getmarcadortime** recupera a hora do marcador no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="d0e12-107">The **getMarkerTime** method retrieves the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e12-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0e12-108">Syntax</span></span>


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="d0e12-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0e12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0e12-110">*markerNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0e12-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e12-111">**Número** (**longo**) que especifica o índice de marcador.</span><span class="sxs-lookup"><span data-stu-id="d0e12-111">**Number** (**long**) specifying the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0e12-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0e12-112">Return value</span></span>

<span data-ttu-id="d0e12-113">Esse método retorna um **número** (**duplo**) especificando o local do marcador em segundos a partir do início do clipe.</span><span class="sxs-lookup"><span data-stu-id="d0e12-113">This method returns a **Number** (**double**) specifying the location of the marker in seconds from the beginning of the clip.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0e12-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0e12-114">Remarks</span></span>

<span data-ttu-id="d0e12-115">Esse método retornará **NULL** se o marcador especificado não existir.</span><span class="sxs-lookup"><span data-stu-id="d0e12-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="d0e12-116">Alguns itens de mídia digital não contêm marcadores.</span><span class="sxs-lookup"><span data-stu-id="d0e12-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="d0e12-117">Use **markerCount** para descobrir quantos marcadores estão no clipe atual.</span><span class="sxs-lookup"><span data-stu-id="d0e12-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="d0e12-118">Os números de índice de marcador começam em 1.</span><span class="sxs-lookup"><span data-stu-id="d0e12-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="d0e12-119">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d0e12-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="d0e12-120">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d0e12-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d0e12-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d0e12-121">Examples</span></span>

<span data-ttu-id="d0e12-122">O exemplo de JScript a seguir usa *mídia*. **Getmarcadortime** para preencher um elemento de TextArea HTML chamado MTIMES com o local de cada marcador.</span><span class="sxs-lookup"><span data-stu-id="d0e12-122">The following JScript example uses *Media*.**getMarkerTime** to fill an HTML TEXTAREA element named MTIMES with the location of each marker.</span></span> <span data-ttu-id="d0e12-123">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d0e12-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="d0e12-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0e12-124">Requirements</span></span>



| <span data-ttu-id="d0e12-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0e12-125">Requirement</span></span> | <span data-ttu-id="d0e12-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d0e12-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e12-127">Versão</span><span class="sxs-lookup"><span data-stu-id="d0e12-127">Version</span></span><br/> | <span data-ttu-id="d0e12-128">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d0e12-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d0e12-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d0e12-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="d0e12-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0e12-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0e12-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0e12-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e12-132">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="d0e12-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="d0e12-133">**Media. getmarkname**</span><span class="sxs-lookup"><span data-stu-id="d0e12-133">**Media.getMarkerName**</span></span>](media-getmarkername.md)
</dt> <dt>

[<span data-ttu-id="d0e12-134">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="d0e12-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="d0e12-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d0e12-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="d0e12-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d0e12-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





