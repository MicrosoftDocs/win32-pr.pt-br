---
description: Ocorre quando a dica da caneta entra em contato com a superfície do Tablet de digitalização.
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: 'Método ITabletEventSink:: CursorDown'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662340"
---
# <a name="itableteventsinkcursordown-method"></a><span data-ttu-id="ccdd0-103">Método ITabletEventSink:: CursorDown</span><span class="sxs-lookup"><span data-stu-id="ccdd0-103">ITabletEventSink::CursorDown method</span></span>

<span data-ttu-id="ccdd0-104">Ocorre quando a dica da caneta entra em contato com a superfície do Tablet de digitalização.</span><span class="sxs-lookup"><span data-stu-id="ccdd0-104">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccdd0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccdd0-105">Syntax</span></span>


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="ccdd0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccdd0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccdd0-107">*TCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccdd0-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccdd0-108">O identificador do Tablet.</span><span class="sxs-lookup"><span data-stu-id="ccdd0-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="ccdd0-109">*CID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ccdd0-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccdd0-110">O identificador da caneta.</span><span class="sxs-lookup"><span data-stu-id="ccdd0-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="ccdd0-111">*nSerialNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccdd0-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccdd0-112">O número de série da caneta.</span><span class="sxs-lookup"><span data-stu-id="ccdd0-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="ccdd0-113">*cbPkt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccdd0-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccdd0-114">O número de bytes em um pacote de dados da caneta.</span><span class="sxs-lookup"><span data-stu-id="ccdd0-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="ccdd0-115">*pbPkt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccdd0-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccdd0-116">Os dados da caneta que indicam o local em que a caneta tocava o Tablet.</span><span class="sxs-lookup"><span data-stu-id="ccdd0-116">The stylus data indicating the location where the stylus touched the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccdd0-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccdd0-117">Return value</span></span>

<span data-ttu-id="ccdd0-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ccdd0-118">This method can return one of these values.</span></span>



| <span data-ttu-id="ccdd0-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ccdd0-119">Return code</span></span>                                                                            | <span data-ttu-id="ccdd0-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ccdd0-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ccdd0-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ccdd0-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="ccdd0-122">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ccdd0-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="ccdd0-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="ccdd0-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="ccdd0-124">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="ccdd0-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ccdd0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccdd0-125">Requirements</span></span>



| <span data-ttu-id="ccdd0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccdd0-126">Requirement</span></span> | <span data-ttu-id="ccdd0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ccdd0-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccdd0-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccdd0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ccdd0-129">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ccdd0-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ccdd0-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccdd0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ccdd0-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ccdd0-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ccdd0-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ccdd0-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ccdd0-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ccdd0-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccdd0-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccdd0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccdd0-135">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="ccdd0-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




