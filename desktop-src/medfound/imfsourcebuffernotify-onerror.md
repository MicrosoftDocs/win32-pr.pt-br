---
description: Usado para indicar que ocorreu um erro com o buffer de origem.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: 'Método IMFSourceBufferNotify:: OnError'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782548"
---
# <a name="imfsourcebuffernotifyonerror-method"></a><span data-ttu-id="4ebf6-103">Método IMFSourceBufferNotify:: OnError</span><span class="sxs-lookup"><span data-stu-id="4ebf6-103">IMFSourceBufferNotify::OnError method</span></span>

<span data-ttu-id="4ebf6-104">Usado para indicar que ocorreu um erro com o buffer de origem.</span><span class="sxs-lookup"><span data-stu-id="4ebf6-104">Used to indicate that an error has occurred with the source buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebf6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ebf6-105">Syntax</span></span>


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="4ebf6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ebf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ebf6-107">*HR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebf6-107">*hr* \[in\]</span></span>
<span data-ttu-id="4ebf6-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4ebf6-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="4ebf6-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ebf6-109">Return value</span></span>

<span data-ttu-id="4ebf6-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4ebf6-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ebf6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ebf6-111">Requirements</span></span>



| <span data-ttu-id="4ebf6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ebf6-112">Requirement</span></span> | <span data-ttu-id="4ebf6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4ebf6-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ebf6-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ebf6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4ebf6-115">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4ebf6-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4ebf6-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ebf6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4ebf6-117">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="4ebf6-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4ebf6-118">INSERI</span><span class="sxs-lookup"><span data-stu-id="4ebf6-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ebf6-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ebf6-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ebf6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ebf6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ebf6-121">**IMFSourceBufferNotify**</span><span class="sxs-lookup"><span data-stu-id="4ebf6-121">**IMFSourceBufferNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




