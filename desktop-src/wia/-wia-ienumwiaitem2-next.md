---
description: Preenche uma matriz de ponteiros para interfaces IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'Método IEnumWiaItem2:: Next (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164712"
---
# <a name="ienumwiaitem2next-method"></a><span data-ttu-id="a4c08-103">Método IEnumWiaItem2:: Next</span><span class="sxs-lookup"><span data-stu-id="a4c08-103">IEnumWiaItem2::Next method</span></span>

<span data-ttu-id="a4c08-104">Preenche uma matriz de ponteiros para interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c08-104">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c08-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4c08-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="a4c08-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4c08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4c08-107">*cElt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4c08-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c08-108">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="a4c08-108">Type: **ULONG**</span></span>

<span data-ttu-id="a4c08-109">Especifica o número de elementos de matriz na matriz indicado pelo parâmetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="a4c08-109">Specifies the number of array elements in the array indicated by the *ppIWiaItem2* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a4c08-110">*ppIWiaItem2* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a4c08-110">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c08-111">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a4c08-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="a4c08-112">Recebe o endereço de uma matriz de ponteiros de interface [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c08-112">Receives the address of an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers.</span></span> <span data-ttu-id="a4c08-113">**IEnumWiaItem2:: Next** preenche essa matriz com ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="a4c08-113">**IEnumWiaItem2::Next** fills this array with interface pointers.</span></span>

</dd> <dt>

<span data-ttu-id="a4c08-114">*pcEltFetched* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a4c08-114">*pcEltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c08-115">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="a4c08-115">Type: \**ULONG\** _</span></span>

<span data-ttu-id="a4c08-116">Na saída, esse parâmetro recebe o número de ponteiros de interface realmente armazenados na matriz indicada pelo parâmetro _ppIWiaItem2 \*.</span><span class="sxs-lookup"><span data-stu-id="a4c08-116">On output, this parameter receives the number of interface pointers actually stored in the array indicated by the _ppIWiaItem2\* parameter.</span></span> <span data-ttu-id="a4c08-117">Quando a enumeração for concluída, esse parâmetro conterá zero.</span><span class="sxs-lookup"><span data-stu-id="a4c08-117">When the enumeration is complete, this parameter contains zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4c08-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4c08-118">Return value</span></span>

<span data-ttu-id="a4c08-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a4c08-119">Type: **HRESULT**</span></span>

<span data-ttu-id="a4c08-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a4c08-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4c08-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4c08-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c08-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4c08-122">Remarks</span></span>

<span data-ttu-id="a4c08-123">O sistema de tempo de execução do WIA (Windows Image Acquisition) 2,0 representa os dispositivos de hardware WIA 2,0 como uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c08-123">The Windows Image Acquisition (WIA) 2.0 run-time system represents WIA 2.0 hardware devices as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="a4c08-124">Os aplicativos usam o método **IEnumWiaItem2:: Next** para obter um ponteiro de interface **IWiaItem2** para cada item na pasta atual da árvore de objetos **IWiaItem2** de um dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="a4c08-124">Applications use the **IEnumWiaItem2::Next** method to obtain an **IWiaItem2** interface pointer for each item in the current folder of a hardware device's **IWiaItem2** object tree.</span></span>

<span data-ttu-id="a4c08-125">Para obter a lista de ponteiros, o aplicativo passa uma matriz de ponteiros de interface [**IWiaItem2**](-wia-iwiaitem2.md) que ele aloca.</span><span class="sxs-lookup"><span data-stu-id="a4c08-125">To obtain the list of pointers, the application passes an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers that it allocates.</span></span> <span data-ttu-id="a4c08-126">Ele também passa o número de elementos de matriz no parâmetro *cElt*.</span><span class="sxs-lookup"><span data-stu-id="a4c08-126">It also passes the number of array elements in the parameter *cElt*.</span></span> <span data-ttu-id="a4c08-127">O método **IEnumWiaItem2:: Next** preenche a matriz com ponteiros para interfaces **IWiaItem2** .</span><span class="sxs-lookup"><span data-stu-id="a4c08-127">The **IEnumWiaItem2::Next** method fills the array with pointers to **IWiaItem2** interfaces.</span></span>

<span data-ttu-id="a4c08-128">Até que o processo de enumeração seja concluído, o método **IEnumWiaItem2:: Next** retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a4c08-128">Until the enumeration process completes, the **IEnumWiaItem2::Next** method returns S\_OK.</span></span> <span data-ttu-id="a4c08-129">A cada vez, ele define o valor apontado por *pcEltFetched* para o número de itens inseridos na matriz.</span><span class="sxs-lookup"><span data-stu-id="a4c08-129">Each time it does, it sets the value pointed to by *pcEltFetched* to the number of items it inserted into the array.</span></span> <span data-ttu-id="a4c08-130">Quando **IEnumWiaItem2:: Next** termina o processo de enumeração de objetos [**IWiaItem2**](-wia-iwiaitem2.md) , ele retorna S \_ false e define o local da memória apontado por *pcEltFetched* como zero.</span><span class="sxs-lookup"><span data-stu-id="a4c08-130">When **IEnumWiaItem2::Next** finishes the process of enumerating [**IWiaItem2**](-wia-iwiaitem2.md) objects, it returns S\_FALSE and sets the memory location pointed to by *pcEltFetched* to zero.</span></span>

<span data-ttu-id="a4c08-131">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="a4c08-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c08-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4c08-132">Requirements</span></span>



| <span data-ttu-id="a4c08-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4c08-133">Requirement</span></span> | <span data-ttu-id="a4c08-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a4c08-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c08-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4c08-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c08-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4c08-136">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a4c08-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4c08-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c08-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4c08-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a4c08-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4c08-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4c08-140"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4c08-140"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4c08-141">INSERI</span><span class="sxs-lookup"><span data-stu-id="a4c08-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a4c08-142"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a4c08-142"><dt>Wia.idl</dt></span></span> </dl> |



 

 
