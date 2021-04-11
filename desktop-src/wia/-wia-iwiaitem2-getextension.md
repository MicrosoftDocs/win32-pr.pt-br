---
description: Obtém as interfaces de extensão que podem vir com um driver de dispositivo de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'Método IWiaItem2:: GetExtension (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010519"
---
# <a name="iwiaitem2getextension-method"></a><span data-ttu-id="1541a-103">Método IWiaItem2:: GetExtension</span><span class="sxs-lookup"><span data-stu-id="1541a-103">IWiaItem2::GetExtension method</span></span>

<span data-ttu-id="1541a-104">Obtém as interfaces de extensão que podem vir com um driver de dispositivo de aquisição de imagem do Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="1541a-104">Gets the extension interfaces that might come with a Windows Image Acquisition (WIA) 2.0 device driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="1541a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1541a-105">Syntax</span></span>


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a><span data-ttu-id="1541a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1541a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1541a-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1541a-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1541a-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="1541a-108">Type: **LONG**</span></span>

<span data-ttu-id="1541a-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="1541a-109">Currently unused.</span></span> <span data-ttu-id="1541a-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="1541a-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="1541a-111">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1541a-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1541a-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1541a-112">Type: **BSTR**</span></span>

<span data-ttu-id="1541a-113">Especifica o nome da extensão à qual o aplicativo de chamada requer um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="1541a-113">Specifies the name of the extension that the calling application requires a pointer to.</span></span>

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span data-ttu-id="1541a-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span><span class="sxs-lookup"><span data-stu-id="1541a-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span></span>


</dt> <dd>

<span data-ttu-id="1541a-115">A extensão do filtro de segmentação.</span><span class="sxs-lookup"><span data-stu-id="1541a-115">The segmentation filter extension.</span></span> <span data-ttu-id="1541a-116">Atualmente, esse é o único valor válido para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1541a-116">This is currently the only valid value for this parameter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1541a-117">*riidExtensionInterface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1541a-117">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1541a-118">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="1541a-118">Type: **REFIID**</span></span>

<span data-ttu-id="1541a-119">Especifica o identificador da interface de extensão.</span><span class="sxs-lookup"><span data-stu-id="1541a-119">Specifies the identifier of the extension interface.</span></span>

</dd> <dt>

<span data-ttu-id="1541a-120">*ppOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1541a-120">*ppOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1541a-121">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="1541a-121">Type: **VOID\*\***</span></span>

<span data-ttu-id="1541a-122">Recebe o endereço de um ponteiro para a interface de extensão.</span><span class="sxs-lookup"><span data-stu-id="1541a-122">Receives the address of a pointer to the extension interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1541a-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1541a-123">Return value</span></span>

<span data-ttu-id="1541a-124">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1541a-124">Type: **HRESULT**</span></span>

<span data-ttu-id="1541a-125">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1541a-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1541a-126">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1541a-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1541a-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="1541a-127">Remarks</span></span>

<span data-ttu-id="1541a-128">Um aplicativo invoca esse método para criar um objeto de extensão que implementa uma das interfaces de extensão de driver WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="1541a-128">An application invokes this method to create an extension object implementing one of the WIA 2.0 driver extension interfaces.</span></span> <span data-ttu-id="1541a-129">**IWiaItem2:: GetExtension** armazena o endereço da interface de extensão do objeto de extensão no parâmetro *riidExtensionInterface* .</span><span class="sxs-lookup"><span data-stu-id="1541a-129">**IWiaItem2::GetExtension** stores the address of the extension object's extension interface in the *riidExtensionInterface* parameter.</span></span> <span data-ttu-id="1541a-130">Em seguida, o aplicativo usa o ponteiro de interface para chamar seus métodos.</span><span class="sxs-lookup"><span data-stu-id="1541a-130">The application then uses the interface pointer to call its methods.</span></span>

<span data-ttu-id="1541a-131">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *riidExtensionInterface* .</span><span class="sxs-lookup"><span data-stu-id="1541a-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *riidExtensionInterface* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="1541a-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1541a-132">Examples</span></span>

<span data-ttu-id="1541a-133">CreateSegmentationFilter cria uma instância do [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)(filtro de segmentação do driver) chamando **IWiaItem2:: GetExtension** na interface de [**IWiaItem2**](-wia-iwiaitem2.md) passada.</span><span class="sxs-lookup"><span data-stu-id="1541a-133">CreateSegmentationFilter creates an instance of the driver's segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) by calling **IWiaItem2::GetExtension** on the passed-in [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span>


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
   }
   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="1541a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1541a-134">Requirements</span></span>



| <span data-ttu-id="1541a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1541a-135">Requirement</span></span> | <span data-ttu-id="1541a-136">Valor</span><span class="sxs-lookup"><span data-stu-id="1541a-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1541a-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1541a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1541a-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1541a-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1541a-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1541a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1541a-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1541a-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1541a-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1541a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1541a-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="1541a-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="1541a-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="1541a-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1541a-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1541a-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 
