---
description: Ocorre quando a caneta está sendo movida no digitalizador.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: 'ITabletEventSink: método ackets de:P'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fb671b0556cf121e28ae81c5dcfa804208e00006
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922158"
---
# <a name="itableteventsinkpackets-method"></a><span data-ttu-id="83bca-103">ITabletEventSink: método ackets de:P</span><span class="sxs-lookup"><span data-stu-id="83bca-103">ITabletEventSink::Packets method</span></span>

<span data-ttu-id="83bca-104">Ocorre quando a caneta está sendo movida no digitalizador.</span><span class="sxs-lookup"><span data-stu-id="83bca-104">Occurs when the stylus is moving on the digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="83bca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83bca-105">Syntax</span></span>


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="83bca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83bca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83bca-107">*TCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83bca-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bca-108">O identificador do Tablet.</span><span class="sxs-lookup"><span data-stu-id="83bca-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="83bca-109">*cPkts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83bca-109">*cPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bca-110">O número de pacotes.</span><span class="sxs-lookup"><span data-stu-id="83bca-110">The number of packets.</span></span>

</dd> <dt>

<span data-ttu-id="83bca-111">*cbPkts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83bca-111">*cbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bca-112">O tamanho do buffer de pacote</span><span class="sxs-lookup"><span data-stu-id="83bca-112">The size of packet buffer</span></span>

</dd> <dt>

<span data-ttu-id="83bca-113">*pbPkts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83bca-113">*pbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bca-114">O buffer de pacotes.</span><span class="sxs-lookup"><span data-stu-id="83bca-114">The packet buffer.</span></span>

</dd> <dt>

<span data-ttu-id="83bca-115">*pnSerialNumbers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83bca-115">*pnSerialNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bca-116">A matriz de número de série.</span><span class="sxs-lookup"><span data-stu-id="83bca-116">The serial number array.</span></span>

</dd> <dt>

<span data-ttu-id="83bca-117">*CID*</span><span class="sxs-lookup"><span data-stu-id="83bca-117">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="83bca-118">O identificador da caneta.</span><span class="sxs-lookup"><span data-stu-id="83bca-118">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83bca-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83bca-119">Return value</span></span>

<span data-ttu-id="83bca-120">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="83bca-120">This method can return one of these values.</span></span>



| <span data-ttu-id="83bca-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="83bca-121">Return code</span></span>                                                                            | <span data-ttu-id="83bca-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="83bca-122">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="83bca-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="83bca-123"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="83bca-124">Êxito.</span><span class="sxs-lookup"><span data-stu-id="83bca-124">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="83bca-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="83bca-125"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="83bca-126">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="83bca-126">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="83bca-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83bca-127">Requirements</span></span>



| <span data-ttu-id="83bca-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="83bca-128">Requirement</span></span> | <span data-ttu-id="83bca-129">Valor</span><span class="sxs-lookup"><span data-stu-id="83bca-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83bca-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83bca-130">Minimum supported client</span></span><br/> | <span data-ttu-id="83bca-131">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="83bca-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="83bca-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83bca-132">Minimum supported server</span></span><br/> | <span data-ttu-id="83bca-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="83bca-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="83bca-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83bca-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="83bca-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83bca-135"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83bca-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="83bca-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83bca-137">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="83bca-137">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




