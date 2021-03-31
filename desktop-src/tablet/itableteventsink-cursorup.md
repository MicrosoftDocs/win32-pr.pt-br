---
description: Ocorre quando o usuário dispara a caneta da superfície digitalizadora do Tablet.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'Método ITabletEventSink:: CursorUp'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171856"
---
# <a name="itableteventsinkcursorup-method"></a><span data-ttu-id="62fa4-103">Método ITabletEventSink:: CursorUp</span><span class="sxs-lookup"><span data-stu-id="62fa4-103">ITabletEventSink::CursorUp method</span></span>

<span data-ttu-id="62fa4-104">Ocorre quando o usuário dispara a caneta da superfície digitalizadora do Tablet.</span><span class="sxs-lookup"><span data-stu-id="62fa4-104">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="62fa4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62fa4-105">Syntax</span></span>


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="62fa4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62fa4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62fa4-107">*TCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62fa4-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fa4-108">O identificador do Tablet.</span><span class="sxs-lookup"><span data-stu-id="62fa4-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="62fa4-109">*CID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="62fa4-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fa4-110">O identificador da caneta.</span><span class="sxs-lookup"><span data-stu-id="62fa4-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="62fa4-111">*nSerialNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62fa4-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fa4-112">O número de série da caneta.</span><span class="sxs-lookup"><span data-stu-id="62fa4-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="62fa4-113">*cbPkt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62fa4-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fa4-114">O número de bytes em um pacote de dados da caneta.</span><span class="sxs-lookup"><span data-stu-id="62fa4-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="62fa4-115">*pbPkt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62fa4-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fa4-116">Os dados da caneta que indicam o local em que a caneta foi levantada do Tablet.</span><span class="sxs-lookup"><span data-stu-id="62fa4-116">The stylus data indicating the location where the stylus was lifted from the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62fa4-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62fa4-117">Return value</span></span>

<span data-ttu-id="62fa4-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="62fa4-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="62fa4-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62fa4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="62fa4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62fa4-120">Requirements</span></span>



| <span data-ttu-id="62fa4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="62fa4-121">Requirement</span></span> | <span data-ttu-id="62fa4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="62fa4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62fa4-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62fa4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="62fa4-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="62fa4-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="62fa4-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62fa4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="62fa4-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="62fa4-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="62fa4-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62fa4-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="62fa4-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62fa4-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62fa4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="62fa4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62fa4-130">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="62fa4-130">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




