---
title: Método IWMPLibraryServices getLibraryByType
description: O método getLibraryByType retorna uma interface IWMPLibrary que representa a biblioteca que tem o tipo e o índice especificados.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- método getLibraryByType Windows Media Player
- método getLibraryByType Windows Media Player, interface IWMPLibraryServices
- Interface IWMPLibraryServices Windows Media Player, método getLibraryByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811781"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a><span data-ttu-id="e0a65-106">Método IWMPLibraryServices:: getLibraryByType</span><span class="sxs-lookup"><span data-stu-id="e0a65-106">IWMPLibraryServices::getLibraryByType method</span></span>

<span data-ttu-id="e0a65-107">O método **getLibraryByType** retorna uma interface **IWMPLibrary** que representa a biblioteca que tem o tipo e o índice especificados.</span><span class="sxs-lookup"><span data-stu-id="e0a65-107">The **getLibraryByType** method returns an **IWMPLibrary** interface that represents the library that has the specified type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0a65-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0a65-108">Syntax</span></span>


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a><span data-ttu-id="e0a65-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0a65-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0a65-110">*wmplt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0a65-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0a65-111">Um valor da enumeração **WMPLib. WMPLibraryType** que especifica o tipo de biblioteca a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="e0a65-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e0a65-112">*Lindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0a65-112">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0a65-113">Um **System. Int32** que é o índice da biblioteca a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="e0a65-113">A **System.Int32** that is the index of the library to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0a65-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0a65-114">Return value</span></span>

<span data-ttu-id="e0a65-115">Uma interface **WMPLib. IWMPLibrary** para a biblioteca que é retornada.</span><span class="sxs-lookup"><span data-stu-id="e0a65-115">A **WMPLib.IWMPLibrary** interface for the library that is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0a65-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0a65-116">Remarks</span></span>

<span data-ttu-id="e0a65-117">Há apenas uma biblioteca local, e as bibliotecas de discos estão disponíveis somente em CDs de dados e DVDs que contêm conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e0a65-117">There is only one local library, and disc libraries are available only on data CDs and DVDs that contain media content.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0a65-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0a65-118">Requirements</span></span>



| <span data-ttu-id="e0a65-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0a65-119">Requirement</span></span> | <span data-ttu-id="e0a65-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e0a65-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0a65-121">Versão</span><span class="sxs-lookup"><span data-stu-id="e0a65-121">Version</span></span><br/>   | <span data-ttu-id="e0a65-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="e0a65-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="e0a65-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0a65-123">Namespace</span></span><br/> | <span data-ttu-id="e0a65-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e0a65-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e0a65-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="e0a65-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e0a65-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e0a65-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0a65-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0a65-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a65-128">**Interface IWMPLibrary (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a65-128">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0a65-129">**Interface IWMPLibraryServices (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a65-129">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0a65-130">**WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="e0a65-130">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





