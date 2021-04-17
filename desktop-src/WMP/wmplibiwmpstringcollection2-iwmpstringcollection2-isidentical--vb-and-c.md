---
title: Método isidêntico IWMPStringCollection2
description: O método isidêntico retorna um valor que indica se o objeto representado pela interface fornecida é o mesmo que o atual.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- método isidêntico do Windows Media Player
- método isidêntico Windows Media Player, interface IWMPStringCollection2
- Interface IWMPStringCollection2 do Windows Media Player, método isidêntico
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782731"
---
# <a name="iwmpstringcollection2isidentical-method"></a><span data-ttu-id="f1433-106">Método IWMPStringCollection2:: isidêntico</span><span class="sxs-lookup"><span data-stu-id="f1433-106">IWMPStringCollection2::isIdentical method</span></span>

<span data-ttu-id="f1433-107">O método **isidêntico** retorna um valor que indica se o objeto representado pela interface fornecida é o mesmo que o atual.</span><span class="sxs-lookup"><span data-stu-id="f1433-107">The **isIdentical** method returns a value indicating whether the object represented by the supplied interface is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1433-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1433-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="f1433-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1433-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1433-110">*pIWMPStringCollection2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f1433-110">*pIWMPStringCollection2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1433-111">A interface **WMPLib. IWMPStringCollection2** que representa o objeto a ser comparado com o atual.</span><span class="sxs-lookup"><span data-stu-id="f1433-111">The **WMPLib.IWMPStringCollection2** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1433-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1433-112">Return value</span></span>

<span data-ttu-id="f1433-113">O **System. Boolean** que é o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="f1433-113">The **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="f1433-114">Um valor **true** indica que os objetos da coleção de cadeia de caracteres são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="f1433-114">A value of **true** indicates that the string collection objects are the same.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1433-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1433-115">Remarks</span></span>

<span data-ttu-id="f1433-116">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f1433-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="f1433-117">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f1433-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1433-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1433-118">Requirements</span></span>



| <span data-ttu-id="f1433-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1433-119">Requirement</span></span> | <span data-ttu-id="f1433-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f1433-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1433-121">Versão</span><span class="sxs-lookup"><span data-stu-id="f1433-121">Version</span></span><br/>   | <span data-ttu-id="f1433-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f1433-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="f1433-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1433-123">Namespace</span></span><br/> | <span data-ttu-id="f1433-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f1433-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f1433-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="f1433-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f1433-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f1433-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1433-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1433-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1433-128">**Interface IWMPStringCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f1433-128">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





