---
description: 'Verifica se uma extensão especificada está disponível no computador e pode ser usada pelo método IWiaItem2:: GetExtension.'
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'Método IWiaItem2:: CheckExtension (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761635"
---
# <a name="iwiaitem2checkextension-method"></a><span data-ttu-id="eb835-103">Método IWiaItem2:: CheckExtension</span><span class="sxs-lookup"><span data-stu-id="eb835-103">IWiaItem2::CheckExtension method</span></span>

<span data-ttu-id="eb835-104">Verifica se uma extensão especificada está disponível no computador e pode ser usada pelo método [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) .</span><span class="sxs-lookup"><span data-stu-id="eb835-104">Checks whether a specified extension is available on the machine and can be used by the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb835-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb835-105">Syntax</span></span>


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
);
```



## <a name="parameters"></a><span data-ttu-id="eb835-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb835-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb835-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb835-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb835-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="eb835-108">Type: **LONG**</span></span>

<span data-ttu-id="eb835-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="eb835-109">Currently unused.</span></span> <span data-ttu-id="eb835-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="eb835-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="eb835-111">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb835-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb835-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="eb835-112">Type: **BSTR**</span></span>

<span data-ttu-id="eb835-113">Especifica o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="eb835-113">Specifies the name of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="eb835-114">*riidExtensionInterface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb835-114">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb835-115">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="eb835-115">Type: **REFIID**</span></span>

<span data-ttu-id="eb835-116">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="eb835-116">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="eb835-117">*pbExtensionExists* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="eb835-117">*pbExtensionExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb835-118">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="eb835-118">Type: \**BOOL\** _</span></span>

<span data-ttu-id="eb835-119">Recebe um ponteiro para um _ \* BOOL \* \*.</span><span class="sxs-lookup"><span data-stu-id="eb835-119">Receives a pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="eb835-120"><span id="FALSE"></span><span id="false"></span>**FOR**</span><span class="sxs-lookup"><span data-stu-id="eb835-120"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="eb835-121">A extensão especificada não está disponível.</span><span class="sxs-lookup"><span data-stu-id="eb835-121">The specified extension is not available.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="eb835-122"><span id="TRUE"></span><span id="true"></span>**TRUE**</span><span class="sxs-lookup"><span data-stu-id="eb835-122"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="eb835-123">A extensão especificada está disponível.</span><span class="sxs-lookup"><span data-stu-id="eb835-123">The specified extension is available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb835-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb835-124">Return value</span></span>

<span data-ttu-id="eb835-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="eb835-125">Type: **HRESULT**</span></span>

<span data-ttu-id="eb835-126">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eb835-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb835-127">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb835-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb835-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb835-128">Remarks</span></span>

<span data-ttu-id="eb835-129">Usando esse método, os aplicativos podem verificar se uma extensão está disponível antes de chamar o método [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) .</span><span class="sxs-lookup"><span data-stu-id="eb835-129">Using this method, applications can check whether an extension is available before calling the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span> <span data-ttu-id="eb835-130">Além disso, o aplicativo pode verificar quais extensões estão disponíveis sem a criação de cada uma delas e, em seguida, decidir qual delas usar.</span><span class="sxs-lookup"><span data-stu-id="eb835-130">Also, the application can check which extensions are available without co-creating each of them, and then decide which one to use.</span></span>

## <a name="examples"></a><span data-ttu-id="eb835-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eb835-131">Examples</span></span>

<span data-ttu-id="eb835-132">CheckImgFilter verifica se o driver tem um filtro de processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="eb835-132">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="eb835-133">Antes de chamar o componente de visualização, um aplicativo deve garantir que o driver tenha um filtro de processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="eb835-133">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



## <a name="requirements"></a><span data-ttu-id="eb835-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb835-134">Requirements</span></span>



| <span data-ttu-id="eb835-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb835-135">Requirement</span></span> | <span data-ttu-id="eb835-136">Valor</span><span class="sxs-lookup"><span data-stu-id="eb835-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eb835-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb835-137">Minimum supported client</span></span><br/> | <span data-ttu-id="eb835-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb835-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eb835-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb835-139">Minimum supported server</span></span><br/> | <span data-ttu-id="eb835-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eb835-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eb835-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb835-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb835-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb835-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb835-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="eb835-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb835-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb835-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 




