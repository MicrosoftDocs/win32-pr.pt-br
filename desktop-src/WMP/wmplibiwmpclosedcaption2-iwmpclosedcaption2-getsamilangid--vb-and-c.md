---
title: Método IWMPClosedCaption2 getSAMILangID
description: O método getSAMILangID retorna o LCID (identificador de localidade) de um idioma com suporte do arquivo SAMI atual.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- método getSAMILangID Windows Media Player
- método getSAMILangID Windows Media Player, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 Windows Media Player, método getSAMILangID
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9aaebecf8e86c056fa9c91141042facc6bcc18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759930"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a><span data-ttu-id="73fa5-106">Método IWMPClosedCaption2:: getSAMILangID</span><span class="sxs-lookup"><span data-stu-id="73fa5-106">IWMPClosedCaption2::getSAMILangID method</span></span>

<span data-ttu-id="73fa5-107">O método **getSAMILangID** retorna o LCID (identificador de localidade) de um idioma com suporte do arquivo Sami atual.</span><span class="sxs-lookup"><span data-stu-id="73fa5-107">The **getSAMILangID** method returns the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="73fa5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73fa5-108">Syntax</span></span>


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a><span data-ttu-id="73fa5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73fa5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fa5-110">*nIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73fa5-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73fa5-111">Um **System. Int32** que é o índice de base zero do LCID a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="73fa5-111">A **System.Int32** that is the zero-based index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73fa5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73fa5-112">Return value</span></span>

<span data-ttu-id="73fa5-113">Um **System. Int32** que é o LCID do idioma com o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="73fa5-113">A **System.Int32** that is the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="73fa5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="73fa5-114">Remarks</span></span>

<span data-ttu-id="73fa5-115">Os idiomas em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.</span><span class="sxs-lookup"><span data-stu-id="73fa5-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="73fa5-116">Esse método retorna 0, a menos que um arquivo de mídia digital esteja aberto (AxWindowsMediaPlayer. OpenState é igual a 13).</span><span class="sxs-lookup"><span data-stu-id="73fa5-116">This method returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="73fa5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73fa5-117">Requirements</span></span>



| <span data-ttu-id="73fa5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="73fa5-118">Requirement</span></span> | <span data-ttu-id="73fa5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="73fa5-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73fa5-120">Versão</span><span class="sxs-lookup"><span data-stu-id="73fa5-120">Version</span></span><br/>   | <span data-ttu-id="73fa5-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="73fa5-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="73fa5-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="73fa5-122">Namespace</span></span><br/> | <span data-ttu-id="73fa5-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="73fa5-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="73fa5-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="73fa5-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="73fa5-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="73fa5-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73fa5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="73fa5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73fa5-127">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="73fa5-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="73fa5-128">**Interface IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="73fa5-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="73fa5-129">**Interface IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="73fa5-129">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





