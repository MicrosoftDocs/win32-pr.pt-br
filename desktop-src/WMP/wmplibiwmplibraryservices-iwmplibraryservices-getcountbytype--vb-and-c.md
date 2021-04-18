---
title: Método IWMPLibraryServices getCountByType
description: O método getCountByType retorna a contagem de bibliotecas disponíveis de um tipo especificado.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- método getCountByType Windows Media Player
- método getCountByType Windows Media Player, interface IWMPLibraryServices
- Interface IWMPLibraryServices Windows Media Player, método getCountByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754585"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a><span data-ttu-id="0a01a-106">Método IWMPLibraryServices:: getCountByType</span><span class="sxs-lookup"><span data-stu-id="0a01a-106">IWMPLibraryServices::getCountByType method</span></span>

<span data-ttu-id="0a01a-107">O método **getCountByType** retorna a contagem de bibliotecas disponíveis de um tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="0a01a-107">The **getCountByType** method returns the count of available libraries of a specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a01a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a01a-108">Syntax</span></span>


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a><span data-ttu-id="0a01a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a01a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a01a-110">*wmplt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a01a-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a01a-111">Um valor da enumeração **WMPLib. WMPLibraryType** que especifica o tipo de biblioteca a ser contabilizada.</span><span class="sxs-lookup"><span data-stu-id="0a01a-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a01a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a01a-112">Return value</span></span>

<span data-ttu-id="0a01a-113">Um **System. Int32** que é a contagem de bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="0a01a-113">A **System.Int32** that is the library count.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a01a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a01a-114">Requirements</span></span>



| <span data-ttu-id="0a01a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a01a-115">Requirement</span></span> | <span data-ttu-id="0a01a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0a01a-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a01a-117">Versão</span><span class="sxs-lookup"><span data-stu-id="0a01a-117">Version</span></span><br/>   | <span data-ttu-id="0a01a-118">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="0a01a-118">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="0a01a-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a01a-119">Namespace</span></span><br/> | <span data-ttu-id="0a01a-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0a01a-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0a01a-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="0a01a-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0a01a-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0a01a-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a01a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a01a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a01a-124">**Interface IWMPLibraryServices (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0a01a-124">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0a01a-125">**WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="0a01a-125">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





