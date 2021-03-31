---
description: Obtém o item raiz de uma árvore de objetos de item usados para representar um dispositivo de hardware de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: bc31ad4a-0851-4510-a038-83646ffd5c98
title: 'Método IWiaItem2:: GetRootItem (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetRootItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c8d4f004cc9c7cabaf4898f5e8c838a0399dc106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647219"
---
# <a name="iwiaitem2getrootitem-method"></a><span data-ttu-id="5d042-103">Método IWiaItem2:: GetRootItem</span><span class="sxs-lookup"><span data-stu-id="5d042-103">IWiaItem2::GetRootItem method</span></span>

<span data-ttu-id="5d042-104">Obtém o item raiz de uma árvore de objetos de item usados para representar um dispositivo de hardware de aquisição de imagem do Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="5d042-104">Gets the root item of a tree of item objects used to represent a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d042-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d042-105">Syntax</span></span>


```C++
HRESULT GetRootItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="5d042-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d042-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d042-107">*ppIWiaItem2* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5d042-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d042-108">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5d042-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="5d042-109">Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item raiz.</span><span class="sxs-lookup"><span data-stu-id="5d042-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d042-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d042-110">Return value</span></span>

<span data-ttu-id="5d042-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5d042-111">Type: **HRESULT**</span></span>

<span data-ttu-id="5d042-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5d042-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d042-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d042-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d042-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d042-114">Remarks</span></span>

<span data-ttu-id="5d042-115">Dado qualquer objeto [**IWiaItem2**](-wia-iwiaitem2.md) na árvore de objetos de um dispositivo de hardware WIA 2,0, o aplicativo recupera um ponteiro para o item raiz chamando essa função.</span><span class="sxs-lookup"><span data-stu-id="5d042-115">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the root item by calling this function.</span></span>

<span data-ttu-id="5d042-116">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="5d042-116">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d042-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d042-117">Requirements</span></span>



| <span data-ttu-id="5d042-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d042-118">Requirement</span></span> | <span data-ttu-id="5d042-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5d042-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d042-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d042-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d042-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d042-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5d042-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d042-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d042-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d042-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5d042-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d042-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d042-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d042-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d042-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="5d042-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d042-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d042-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 
