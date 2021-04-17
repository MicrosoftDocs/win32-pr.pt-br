---
description: Obtém um IMemoryBuffer como uma matriz de bytes.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'Método IMemoryBufferByteAccess:: GetBuffer'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782783"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a><span data-ttu-id="936ab-103">Método IMemoryBufferByteAccess:: GetBuffer</span><span class="sxs-lookup"><span data-stu-id="936ab-103">IMemoryBufferByteAccess::GetBuffer method</span></span>

<span data-ttu-id="936ab-104">Obtém um [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) como uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="936ab-104">Gets an [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) as an array of bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="936ab-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="936ab-105">Syntax</span></span>


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a><span data-ttu-id="936ab-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="936ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936ab-107">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="936ab-107">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="936ab-108">Um ponteiro para uma matriz de bytes que contém os dados do buffer.</span><span class="sxs-lookup"><span data-stu-id="936ab-108">A pointer to a byte array containing the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="936ab-109">*capacidade* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="936ab-109">*capacity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="936ab-110">O número de bytes na matriz retornada</span><span class="sxs-lookup"><span data-stu-id="936ab-110">The number of bytes in the returned array</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="936ab-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="936ab-111">Return value</span></span>

<span data-ttu-id="936ab-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="936ab-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="936ab-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="936ab-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="936ab-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="936ab-114">Remarks</span></span>

<span data-ttu-id="936ab-115">Quando [**memorybuffer já:: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) é chamado, o código que usa esse buffer deve definir o ponteiro de *valor* como NULL.</span><span class="sxs-lookup"><span data-stu-id="936ab-115">When [**MemoryBuffer::Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) is called, the code using this buffer should set the *value* pointer to null.</span></span>

## <a name="see-also"></a><span data-ttu-id="936ab-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="936ab-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="936ab-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="936ab-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span></span>
</dt> </dl>

 

 
