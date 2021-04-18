---
title: Método IWMPClosedCaption2 getSAMILangName
description: O método getSAMILangName retorna o nome de um idioma com suporte do arquivo SAMI atual.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- método getSAMILangName Windows Media Player
- método getSAMILangName Windows Media Player, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 Windows Media Player, método getSAMILangName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788018"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a><span data-ttu-id="596ff-106">Método IWMPClosedCaption2:: getSAMILangName</span><span class="sxs-lookup"><span data-stu-id="596ff-106">IWMPClosedCaption2::getSAMILangName method</span></span>

<span data-ttu-id="596ff-107">O método **getSAMILangName** retorna o nome de um idioma com suporte do arquivo Sami atual.</span><span class="sxs-lookup"><span data-stu-id="596ff-107">The **getSAMILangName** method returns the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="596ff-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="596ff-108">Syntax</span></span>


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a><span data-ttu-id="596ff-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="596ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="596ff-110">*nIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="596ff-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="596ff-111">**Um System. Int32** que é o índice de base zero do nome do idioma a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="596ff-111">**A System.Int32** that is the zero-based index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="596ff-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="596ff-112">Return value</span></span>

<span data-ttu-id="596ff-113">Um **System. String** que é o nome do idioma conforme especificado no arquivo Sami.</span><span class="sxs-lookup"><span data-stu-id="596ff-113">A **System.String** that is the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="596ff-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="596ff-114">Remarks</span></span>

<span data-ttu-id="596ff-115">Os idiomas em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.</span><span class="sxs-lookup"><span data-stu-id="596ff-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="596ff-116">Esse método retorna uma cadeia de caracteres de comprimento zero (""), a menos que um arquivo de mídia digital esteja aberto (AxWindowsMediaPlayer. OpenState é igual a 13).</span><span class="sxs-lookup"><span data-stu-id="596ff-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="596ff-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="596ff-117">Requirements</span></span>



| <span data-ttu-id="596ff-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="596ff-118">Requirement</span></span> | <span data-ttu-id="596ff-119">Valor</span><span class="sxs-lookup"><span data-stu-id="596ff-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="596ff-120">Versão</span><span class="sxs-lookup"><span data-stu-id="596ff-120">Version</span></span><br/>   | <span data-ttu-id="596ff-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="596ff-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="596ff-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="596ff-122">Namespace</span></span><br/> | <span data-ttu-id="596ff-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="596ff-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="596ff-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="596ff-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="596ff-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="596ff-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="596ff-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="596ff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="596ff-127">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="596ff-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="596ff-128">**Interface IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="596ff-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="596ff-129">**IWMPClosedCaption. SAMILang (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="596ff-129">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="596ff-130">**Interface IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="596ff-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





