---
description: Pesquisa a árvore de subitens de um item usando o nome como a chave de pesquisa.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'Método IWiaItem2:: FindItemByName (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 821be7e4abd8d1396befa886093aa197bcdea7f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772552"
---
# <a name="iwiaitem2finditembyname-method"></a><span data-ttu-id="120c6-103">Método IWiaItem2:: FindItemByName</span><span class="sxs-lookup"><span data-stu-id="120c6-103">IWiaItem2::FindItemByName method</span></span>

<span data-ttu-id="120c6-104">Pesquisa a árvore de subitens de um item usando o nome como a chave de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="120c6-104">Searches an item's tree of subitems using the name as the search key.</span></span>

## <a name="syntax"></a><span data-ttu-id="120c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="120c6-105">Syntax</span></span>


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="120c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="120c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="120c6-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="120c6-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="120c6-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="120c6-108">Type: **LONG**</span></span>

<span data-ttu-id="120c6-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="120c6-109">Currently unused.</span></span> <span data-ttu-id="120c6-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="120c6-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="120c6-111">*bstrFullItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="120c6-111">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="120c6-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="120c6-112">Type: **BSTR**</span></span>

<span data-ttu-id="120c6-113">Especifica o nome do item a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="120c6-113">Specifies the name fo the item to search for.</span></span>

</dd> <dt>

<span data-ttu-id="120c6-114">*ppIWiaItem2* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="120c6-114">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="120c6-115">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="120c6-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="120c6-116">Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item encontrado.</span><span class="sxs-lookup"><span data-stu-id="120c6-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item found.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="120c6-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="120c6-117">Return value</span></span>

<span data-ttu-id="120c6-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="120c6-118">Type: **HRESULT**</span></span>

<span data-ttu-id="120c6-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="120c6-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="120c6-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="120c6-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="120c6-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="120c6-121">Remarks</span></span>

<span data-ttu-id="120c6-122">Esse método pesquisa a árvore do item atual de subitens usando o nome como a chave de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="120c6-122">This method searches the current item's tree of sub-items using the name as the search key.</span></span> <span data-ttu-id="120c6-123">Se **IWiaItem2:: FindItemByName** encontrar o item especificado por *bstrFullItemName*, ele armazenará o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item no parâmetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="120c6-123">If **IWiaItem2::FindItemByName** finds the item specified by *bstrFullItemName*, it stores the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="120c6-124">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="120c6-124">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="120c6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="120c6-125">Requirements</span></span>



| <span data-ttu-id="120c6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="120c6-126">Requirement</span></span> | <span data-ttu-id="120c6-127">Valor</span><span class="sxs-lookup"><span data-stu-id="120c6-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="120c6-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="120c6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="120c6-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="120c6-129">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="120c6-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="120c6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="120c6-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="120c6-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="120c6-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="120c6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="120c6-133"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="120c6-133"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="120c6-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="120c6-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="120c6-135"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="120c6-135"><dt>Wia.idl</dt></span></span> </dl> |



 

 
