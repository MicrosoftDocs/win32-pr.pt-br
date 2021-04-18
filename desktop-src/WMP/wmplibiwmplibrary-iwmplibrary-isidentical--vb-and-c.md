---
title: Método isidêntico IWMPLibrary
description: O método isidêntico retorna um valor que indica se o objeto fornecido é o mesmo que o atual.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- método isidêntico do Windows Media Player
- método isidêntico Windows Media Player, interface IWMPLibrary
- Interface IWMPLibrary do Windows Media Player, método isidêntico
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764522"
---
# <a name="iwmplibraryisidentical-method"></a><span data-ttu-id="8fd8a-106">Método IWMPLibrary:: isidêntico</span><span class="sxs-lookup"><span data-stu-id="8fd8a-106">IWMPLibrary::isIdentical method</span></span>

<span data-ttu-id="8fd8a-107">O método **isidêntico** retorna um valor que indica se o objeto fornecido é o mesmo que o atual.</span><span class="sxs-lookup"><span data-stu-id="8fd8a-107">The **isIdentical** method returns a value that indicates whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd8a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fd8a-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="8fd8a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fd8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fd8a-110">*pIWMPLibrary* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8fd8a-110">*pIWMPLibrary* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fd8a-111">Uma interface **WMPLib. IWMPLibrary** que representa o objeto a ser comparado com o atual.</span><span class="sxs-lookup"><span data-stu-id="8fd8a-111">A **WMPLib.IWMPLibrary** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fd8a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8fd8a-112">Return value</span></span>

<span data-ttu-id="8fd8a-113">Um **System. Boolean** que é o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="8fd8a-113">A **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="8fd8a-114">O valor **true** indica que os objetos são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="8fd8a-114">The value **true** indicates that the objects are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fd8a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fd8a-115">Requirements</span></span>



| <span data-ttu-id="8fd8a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fd8a-116">Requirement</span></span> | <span data-ttu-id="8fd8a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8fd8a-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd8a-118">Versão</span><span class="sxs-lookup"><span data-stu-id="8fd8a-118">Version</span></span><br/>   | <span data-ttu-id="8fd8a-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="8fd8a-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="8fd8a-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="8fd8a-120">Namespace</span></span><br/> | <span data-ttu-id="8fd8a-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8fd8a-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8fd8a-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="8fd8a-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8fd8a-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8fd8a-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fd8a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fd8a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd8a-125">**Interface IWMPLibrary (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8fd8a-125">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





