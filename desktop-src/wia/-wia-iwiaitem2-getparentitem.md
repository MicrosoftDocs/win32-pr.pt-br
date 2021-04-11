---
description: Obtém o item pai na árvore que representa um dispositivo de hardware de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'Método IWiaItem2:: GetParentItem (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 055625b98807103c3b79109216f6081d00564b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296382"
---
# <a name="iwiaitem2getparentitem-method"></a><span data-ttu-id="01b32-103">Método IWiaItem2:: GetParentItem</span><span class="sxs-lookup"><span data-stu-id="01b32-103">IWiaItem2::GetParentItem method</span></span>

<span data-ttu-id="01b32-104">Obtém o item pai na árvore que representa um dispositivo de hardware de aquisição de imagem do Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="01b32-104">Gets the parent item in the tree that represents a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b32-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01b32-105">Syntax</span></span>


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="01b32-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01b32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01b32-107">*ppIWiaItem2* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="01b32-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01b32-108">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="01b32-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="01b32-109">Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do pai do item na árvore de objetos item.</span><span class="sxs-lookup"><span data-stu-id="01b32-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the parent of the item in the tree of item objects.</span></span> <span data-ttu-id="01b32-110">Se esse método for chamado na raiz da árvore, o endereço retornado será **NULL**.</span><span class="sxs-lookup"><span data-stu-id="01b32-110">If this method is called on the root of the tree, then the returned address is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01b32-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01b32-111">Return value</span></span>

<span data-ttu-id="01b32-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="01b32-112">Type: **HRESULT**</span></span>

<span data-ttu-id="01b32-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="01b32-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01b32-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01b32-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="01b32-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="01b32-115">Remarks</span></span>

<span data-ttu-id="01b32-116">Dado qualquer objeto [**IWiaItem2**](-wia-iwiaitem2.md) na árvore de objetos de um dispositivo de hardware WIA 2,0, o aplicativo recupera um ponteiro para o item pai chamando essa função.</span><span class="sxs-lookup"><span data-stu-id="01b32-116">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the parent item by calling this function.</span></span>

<span data-ttu-id="01b32-117">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* se esses ponteiros não forem **nulos**.</span><span class="sxs-lookup"><span data-stu-id="01b32-117">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter if these pointers are not **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b32-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01b32-118">Requirements</span></span>



| <span data-ttu-id="01b32-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b32-119">Requirement</span></span> | <span data-ttu-id="01b32-120">Valor</span><span class="sxs-lookup"><span data-stu-id="01b32-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01b32-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01b32-121">Minimum supported client</span></span><br/> | <span data-ttu-id="01b32-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01b32-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="01b32-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01b32-123">Minimum supported server</span></span><br/> | <span data-ttu-id="01b32-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01b32-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="01b32-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01b32-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="01b32-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="01b32-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="01b32-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="01b32-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01b32-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01b32-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 
