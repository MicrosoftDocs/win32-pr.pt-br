---
description: 'Remove a restrição de acesso em um intervalo de bytes anteriormente restritos usando IByteBuffer:: LockRegion.'
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'Método IByteBuffer:: UnlockRegion (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92e49ba000177326ad14d3b83002613a15e96e18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922524"
---
# <a name="ibytebufferunlockregion-method"></a><span data-ttu-id="4f79f-103">Método IByteBuffer:: UnlockRegion</span><span class="sxs-lookup"><span data-stu-id="4f79f-103">IByteBuffer::UnlockRegion method</span></span>

<span data-ttu-id="4f79f-104">\[O método **UnlockRegion** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4f79f-104">\[The **UnlockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4f79f-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4f79f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4f79f-106">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4f79f-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="4f79f-107">O método **UnlockRegion** remove a restrição de acesso em um intervalo de bytes anteriormente restringido usando [**IByteBuffer:: LockRegion**](ibytebuffer-lockregion.md).</span><span class="sxs-lookup"><span data-stu-id="4f79f-107">The **UnlockRegion** method removes the access restriction on a range of bytes previously restricted by using [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f79f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f79f-108">Syntax</span></span>


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="4f79f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f79f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f79f-110">*libOffset* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f79f-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f79f-111">Deslocamento de byte para o início do intervalo.</span><span class="sxs-lookup"><span data-stu-id="4f79f-111">Byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="4f79f-112">*CB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f79f-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f79f-113">Comprimento, em bytes, do intervalo a ser restringido.</span><span class="sxs-lookup"><span data-stu-id="4f79f-113">Length, in bytes, of the range to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="4f79f-114">*dwLockType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f79f-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f79f-115">Restrições de acesso previamente colocadas no intervalo.</span><span class="sxs-lookup"><span data-stu-id="4f79f-115">Access restrictions previously placed on the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f79f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f79f-116">Return value</span></span>

<span data-ttu-id="4f79f-117">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4f79f-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="4f79f-118">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4f79f-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f79f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f79f-119">Remarks</span></span>

<span data-ttu-id="4f79f-120">O método **IByteBuffer:: UnlockRegion** desbloqueia uma região bloqueada anteriormente usando o método [**IByteBuffer:: LockRegion**](ibytebuffer-lockregion.md) .</span><span class="sxs-lookup"><span data-stu-id="4f79f-120">The **IByteBuffer::UnlockRegion** method unlocks a region previously locked by using the [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md) method.</span></span> <span data-ttu-id="4f79f-121">As regiões bloqueadas devem ser desbloqueadas mais tarde chamando **IByteBuffer:: UnlockRegion** com exatamente os mesmos valores para os parâmetros *libOffset*, *CB* e *dwLockType* .</span><span class="sxs-lookup"><span data-stu-id="4f79f-121">Locked regions must later be explicitly unlocked by calling **IByteBuffer::UnlockRegion** with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="4f79f-122">A região deve ser desbloqueada antes de o fluxo ser liberado.</span><span class="sxs-lookup"><span data-stu-id="4f79f-122">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="4f79f-123">Duas regiões adjacentes não podem ser bloqueadas separadamente e desbloqueadas com uma única chamada de desbloqueio.</span><span class="sxs-lookup"><span data-stu-id="4f79f-123">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="4f79f-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f79f-124">Examples</span></span>

<span data-ttu-id="4f79f-125">O exemplo a seguir mostra o desbloqueio de um intervalo de bytes.</span><span class="sxs-lookup"><span data-stu-id="4f79f-125">The following example shows unlocking a range of bytes.</span></span>


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="4f79f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f79f-126">Requirements</span></span>



| <span data-ttu-id="4f79f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f79f-127">Requirement</span></span> | <span data-ttu-id="4f79f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4f79f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f79f-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f79f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4f79f-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4f79f-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4f79f-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f79f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4f79f-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4f79f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f79f-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4f79f-133">End of client support</span></span><br/>    | <span data-ttu-id="4f79f-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4f79f-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4f79f-135">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4f79f-135">End of server support</span></span><br/>    | <span data-ttu-id="4f79f-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4f79f-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4f79f-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f79f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f79f-138"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f79f-138"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f79f-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4f79f-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f79f-140"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4f79f-140"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4f79f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4f79f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f79f-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f79f-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f79f-143">IID</span><span class="sxs-lookup"><span data-stu-id="4f79f-143">IID</span></span><br/>                      | <span data-ttu-id="4f79f-144">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="4f79f-144">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

