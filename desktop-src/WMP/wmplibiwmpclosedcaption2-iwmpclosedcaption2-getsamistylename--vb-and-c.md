---
title: Método IWMPClosedCaption2 getSAMIStyleName
description: O método getSAMIStyleName retorna o nome de um estilo suportado pelo arquivo SAMI atual.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- método getSAMIStyleName Windows Media Player
- método getSAMIStyleName Windows Media Player, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 Windows Media Player, método getSAMIStyleName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ceb3f598ae603d478af5cad9c78333952530a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782871"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a><span data-ttu-id="102d3-106">Método IWMPClosedCaption2:: getSAMIStyleName</span><span class="sxs-lookup"><span data-stu-id="102d3-106">IWMPClosedCaption2::getSAMIStyleName method</span></span>

<span data-ttu-id="102d3-107">O método **getSAMIStyleName** retorna o nome de um estilo suportado pelo arquivo Sami atual.</span><span class="sxs-lookup"><span data-stu-id="102d3-107">The **getSAMIStyleName** method returns the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="102d3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="102d3-108">Syntax</span></span>


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a><span data-ttu-id="102d3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="102d3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="102d3-110">*nIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="102d3-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="102d3-111">Um **System. Int32** que é o índice de base zero do nome do estilo a ser recuperado</span><span class="sxs-lookup"><span data-stu-id="102d3-111">A **System.Int32** that is the zero-based index of the style name to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="102d3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="102d3-112">Return value</span></span>

<span data-ttu-id="102d3-113">Um **System. String** que é o nome do estilo, conforme especificado no arquivo Sami.</span><span class="sxs-lookup"><span data-stu-id="102d3-113">A **System.String** that is the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="102d3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="102d3-114">Remarks</span></span>

<span data-ttu-id="102d3-115">Os estilos em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.</span><span class="sxs-lookup"><span data-stu-id="102d3-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="102d3-116">Esse método retorna uma cadeia de caracteres de comprimento zero (""), a menos que um arquivo de mídia digital esteja aberto (AxWindowsMediaPlayer. OpenState é igual a 13).</span><span class="sxs-lookup"><span data-stu-id="102d3-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="102d3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="102d3-117">Requirements</span></span>



| <span data-ttu-id="102d3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="102d3-118">Requirement</span></span> | <span data-ttu-id="102d3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="102d3-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="102d3-120">Versão</span><span class="sxs-lookup"><span data-stu-id="102d3-120">Version</span></span><br/>   | <span data-ttu-id="102d3-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="102d3-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="102d3-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="102d3-122">Namespace</span></span><br/> | <span data-ttu-id="102d3-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="102d3-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="102d3-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="102d3-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="102d3-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="102d3-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="102d3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="102d3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="102d3-127">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="102d3-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="102d3-128">**Interface IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="102d3-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="102d3-129">**IWMPClosedCaption. SAMIstyle (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="102d3-129">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="102d3-130">**Interface IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="102d3-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





