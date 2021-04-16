---
description: Cria um objeto de enumerador e retorna um ponteiro para sua interface IEnumWiaItem2 para pastas com itens na árvore IWiaItem2 de um dispositivo WIA (Windows Image Acquisition) 2,0.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'Método IWiaItem2:: EnumChildItems (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461146"
---
# <a name="iwiaitem2enumchilditems-method"></a><span data-ttu-id="0f909-103">Método IWiaItem2:: EnumChildItems</span><span class="sxs-lookup"><span data-stu-id="0f909-103">IWiaItem2::EnumChildItems method</span></span>

<span data-ttu-id="0f909-104">Cria um objeto de enumerador e retorna um ponteiro para sua interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) para pastas com itens na árvore [**IWiaItem2**](-wia-iwiaitem2.md) de um dispositivo WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="0f909-104">Creates an enumerator object and passes back a pointer to its [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface for folders with items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree of a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f909-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f909-105">Syntax</span></span>


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="0f909-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f909-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f909-107">*pCategoryGUID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f909-107">*pCategoryGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f909-108">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="0f909-108">Type: \**const GUID\** _</span></span>

<span data-ttu-id="0f909-109">Especifica um ponteiro para uma categoria para a qual nós filhos são enumerados.</span><span class="sxs-lookup"><span data-stu-id="0f909-109">Specifies a pointer to a category for which child nodes are enumerated.</span></span> <span data-ttu-id="0f909-110">Se _ \* NULL \* \*, todos os nós filho serão enumerados.</span><span class="sxs-lookup"><span data-stu-id="0f909-110">If _\*NULL\*\*, then all child nodes are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="0f909-111">*ppIEnumWiaItem2* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f909-111">*ppIEnumWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f909-112">Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="0f909-112">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="0f909-113">Recebe o endereço de um ponteiro para a interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que esse método cria.</span><span class="sxs-lookup"><span data-stu-id="0f909-113">Receives the address of a pointer to the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface that this method creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f909-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f909-114">Return value</span></span>

<span data-ttu-id="0f909-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0f909-115">Type: **HRESULT**</span></span>

<span data-ttu-id="0f909-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0f909-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f909-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f909-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f909-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f909-118">Remarks</span></span>

<span data-ttu-id="0f909-119">O sistema de tempo de execução WIA 2,0 representa cada dispositivo de hardware WIA 2,0 como uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="0f909-119">The WIA 2.0 run-time system represents each WIA 2.0 hardware device as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="0f909-120">O método **IWiaItem2:: EnumChildItems** permite que os aplicativos enumerem itens filho no item atual.</span><span class="sxs-lookup"><span data-stu-id="0f909-120">The **IWiaItem2::EnumChildItems** method enables applications to enumerate child items in the current item.</span></span> <span data-ttu-id="0f909-121">No entanto, ele só pode ser aplicado a itens que são pastas.</span><span class="sxs-lookup"><span data-stu-id="0f909-121">However, it can only be applied to items that are folders.</span></span>

<span data-ttu-id="0f909-122">Se a pasta não estiver vazia, ela conterá uma subárvore de objetos [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="0f909-122">If the folder is not empty, it contains a subtree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="0f909-123">O método **IWiaItem2:: EnumChildItems** enumera todos os itens contidos na pasta.</span><span class="sxs-lookup"><span data-stu-id="0f909-123">The **IWiaItem2::EnumChildItems** method enumerates all of the items contained in the folder.</span></span> <span data-ttu-id="0f909-124">Ele armazena um ponteiro para um enumerador no parâmetro *ppIEnumWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="0f909-124">It stores a pointer to an enumerator in the *ppIEnumWiaItem2* parameter.</span></span> <span data-ttu-id="0f909-125">Os aplicativos usam o ponteiro do enumerador para executar a enumeração dos itens filho de um objeto.</span><span class="sxs-lookup"><span data-stu-id="0f909-125">Applications use the enumerator pointer to perform the enumeration of an object's child items.</span></span>

<span data-ttu-id="0f909-126">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIEnumWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="0f909-126">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f909-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f909-127">Requirements</span></span>



| <span data-ttu-id="0f909-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f909-128">Requirement</span></span> | <span data-ttu-id="0f909-129">Valor</span><span class="sxs-lookup"><span data-stu-id="0f909-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f909-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f909-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0f909-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f909-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0f909-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f909-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0f909-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0f909-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0f909-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f909-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f909-135"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f909-135"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f909-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="0f909-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f909-137"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f909-137"><dt>Wia.idl</dt></span></span> </dl> |



 

 
