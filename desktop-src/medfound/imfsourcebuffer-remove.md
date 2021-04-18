---
description: Remove os segmentos de mídia definidos pelo intervalo de tempo especificado do IMFSourceBuffer.
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: 'Método IMFSourceBuffer:: Remove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: d82660d08efe651b321672b6ccd0cb475875beee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771390"
---
# <a name="imfsourcebufferremove-method"></a><span data-ttu-id="a4e34-103">Método IMFSourceBuffer:: Remove</span><span class="sxs-lookup"><span data-stu-id="a4e34-103">IMFSourceBuffer::Remove method</span></span>

<span data-ttu-id="a4e34-104">Remove os segmentos de mídia definidos pelo intervalo de tempo especificado do [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="a4e34-104">Removes the media segments defined by the specified time range from the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e34-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4e34-105">Syntax</span></span>


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a><span data-ttu-id="a4e34-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4e34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4e34-107">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4e34-107">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4e34-108">O início do intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="a4e34-108">The start of the time range.</span></span>

</dd> <dt>

<span data-ttu-id="a4e34-109">*fim* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4e34-109">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4e34-110">O fim do intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="a4e34-110">The end of the time range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4e34-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4e34-111">Return value</span></span>

<span data-ttu-id="a4e34-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a4e34-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4e34-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4e34-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e34-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4e34-114">Requirements</span></span>



| <span data-ttu-id="a4e34-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4e34-115">Requirement</span></span> | <span data-ttu-id="a4e34-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a4e34-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e34-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4e34-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a4e34-118">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a4e34-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a4e34-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4e34-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a4e34-120">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="a4e34-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a4e34-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="a4e34-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a4e34-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a4e34-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4e34-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4e34-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e34-124">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="a4e34-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




