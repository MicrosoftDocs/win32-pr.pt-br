---
description: Retorna uma cadeia de caracteres que descreve o código de status.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'Método IWiaErrorHandler:: GetStatusDescription (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797504"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a><span data-ttu-id="96718-103">Método IWiaErrorHandler:: GetStatusDescription</span><span class="sxs-lookup"><span data-stu-id="96718-103">IWiaErrorHandler::GetStatusDescription method</span></span>

<span data-ttu-id="96718-104">Retorna uma cadeia de caracteres que descreve o código de status.</span><span class="sxs-lookup"><span data-stu-id="96718-104">Returns a string that describes the status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="96718-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96718-105">Syntax</span></span>


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a><span data-ttu-id="96718-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96718-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96718-107">*punkItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96718-107">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96718-108">Tipo: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="96718-108">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="96718-109">Ponteiro para o [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) do item que está sendo transferido.</span><span class="sxs-lookup"><span data-stu-id="96718-109">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) of the item being transferred.</span></span> <span data-ttu-id="96718-110">Esse objeto implementa minimamente [_ *IWiaItem2* \*](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="96718-110">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="96718-111">*hrStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96718-111">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96718-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="96718-112">Type: **HRESULT**</span></span>

<span data-ttu-id="96718-113">**HRESULT** que é o código de status recebido por [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="96718-113">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="96718-114">*cbResLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96718-114">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96718-115">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="96718-115">Type: **LONG**</span></span>

<span data-ttu-id="96718-116">**Longo** que é o tamanho dos dados referenciados por *pbData*.</span><span class="sxs-lookup"><span data-stu-id="96718-116">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="96718-117">*pbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96718-117">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96718-118">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="96718-118">Type: \**BYTE\** _</span></span>

<span data-ttu-id="96718-119">Ponteiro para o buffer de dados como recebido por [_ *BandedDataCallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="96718-119">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="96718-120">*pbstrDescription* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="96718-120">*pbstrDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96718-121">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="96718-121">Type: \**BSTR\** _</span></span>

<span data-ttu-id="96718-122">_ *BSTR*\* que recebe uma descrição do status ou do erro encontrado durante a transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="96718-122">_ *BSTR*\* that receives a description of the status or error encountered during the data transfer.</span></span> <span data-ttu-id="96718-123">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="96718-123">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="96718-124">O chamador deve liberar a cadeia de caracteres usando [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)e o implementador deve alocar a cadeia de caracteres usando [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span><span class="sxs-lookup"><span data-stu-id="96718-124">The caller must free the string using [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), and the implementor must allocate the string using [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96718-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96718-125">Return value</span></span>

<span data-ttu-id="96718-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="96718-126">Type: **HRESULT**</span></span>

<span data-ttu-id="96718-127">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="96718-127">Returns one of the following values.</span></span>



| <span data-ttu-id="96718-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="96718-128">Return code</span></span>                                                                             | <span data-ttu-id="96718-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="96718-129">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="96718-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="96718-130"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="96718-131">*pbstrDescription* contém um ponteiro **BSTR** válido.</span><span class="sxs-lookup"><span data-stu-id="96718-131">*pbstrDescription* contains a valid **BSTR** pointer.</span></span> <br/>  |
| <dl> <span data-ttu-id="96718-132"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="96718-132"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="96718-133">*hrStatus* é desconhecido e nenhuma descrição está disponível.</span><span class="sxs-lookup"><span data-stu-id="96718-133">*hrStatus* is unknown and no description is available.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="96718-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96718-134">Requirements</span></span>



| <span data-ttu-id="96718-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="96718-135">Requirement</span></span> | <span data-ttu-id="96718-136">Valor</span><span class="sxs-lookup"><span data-stu-id="96718-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96718-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96718-137">Minimum supported client</span></span><br/> | <span data-ttu-id="96718-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96718-138">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="96718-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96718-139">Minimum supported server</span></span><br/> | <span data-ttu-id="96718-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96718-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="96718-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96718-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="96718-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="96718-142"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="96718-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="96718-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96718-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96718-144"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="96718-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96718-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="96718-146"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96718-146"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
