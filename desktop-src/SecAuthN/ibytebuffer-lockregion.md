---
description: Restringe o acesso a um intervalo especificado de bytes no objeto de buffer.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'Método IByteBuffer:: LockRegion (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171264"
---
# <a name="ibytebufferlockregion-method"></a><span data-ttu-id="b151b-103">Método IByteBuffer:: LockRegion</span><span class="sxs-lookup"><span data-stu-id="b151b-103">IByteBuffer::LockRegion method</span></span>

<span data-ttu-id="b151b-104">\[O método **LockRegion** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b151b-104">\[The **LockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b151b-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b151b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b151b-106">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b151b-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="b151b-107">O método **LockRegion** restringe o acesso a um intervalo especificado de bytes no objeto buffer.</span><span class="sxs-lookup"><span data-stu-id="b151b-107">The **LockRegion** method restricts access to a specified range of bytes in the buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b151b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b151b-108">Syntax</span></span>


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="b151b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b151b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b151b-110">*libOffset* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b151b-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b151b-111">Inteiro que especifica o deslocamento de byte para o início do intervalo.</span><span class="sxs-lookup"><span data-stu-id="b151b-111">Integer that specifies the byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="b151b-112">*CB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b151b-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b151b-113">Inteiro que especifica o comprimento do intervalo, em bytes, a ser restringido.</span><span class="sxs-lookup"><span data-stu-id="b151b-113">Integer that specifies the length of the range, in bytes, to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="b151b-114">*dwLockType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b151b-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b151b-115">Especifica as restrições que estão sendo solicitadas ao acessar o intervalo.</span><span class="sxs-lookup"><span data-stu-id="b151b-115">Specifies the restrictions being requested on accessing the range.</span></span> <span data-ttu-id="b151b-116">Isso pode ser um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b151b-116">This can be one of the values in the following table.</span></span>



| <span data-ttu-id="b151b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b151b-117">Value</span></span>                                                                                                                                                            | <span data-ttu-id="b151b-118">Significado</span><span class="sxs-lookup"><span data-stu-id="b151b-118">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <span data-ttu-id="b151b-119"><dt>**BLOQUEAR \_ gravação**</dt></span><span class="sxs-lookup"><span data-stu-id="b151b-119"><dt>**LOCK\_WRITE**</dt></span></span> </dl>             | <span data-ttu-id="b151b-120">O intervalo especificado de bytes pode ser aberto e lido várias vezes, mas a gravação no intervalo bloqueado é proibida, exceto pelo proprietário que recebeu esse bloqueio.</span><span class="sxs-lookup"><span data-stu-id="b151b-120">The specified range of bytes can be opened and read any number of times, but writing to the locked range is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <span data-ttu-id="b151b-121"><dt>**BLOQUEIO \_ exclusivo**</dt></span><span class="sxs-lookup"><span data-stu-id="b151b-121"><dt>**LOCK\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="b151b-122">A gravação no intervalo de bytes especificado é proibida, exceto pelo proprietário que recebeu esse bloqueio.</span><span class="sxs-lookup"><span data-stu-id="b151b-122">Writing to the specified range of bytes is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <span data-ttu-id="b151b-123"><dt>**BLOQUEAR \_ ONLYONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="b151b-123"><dt>**LOCK\_ONLYONCE**</dt></span></span> </dl>    | <span data-ttu-id="b151b-124">Se esse bloqueio for concedido, nenhum outro \_ bloqueio de ONLYONCE de bloqueio poderá ser obtido no intervalo.</span><span class="sxs-lookup"><span data-stu-id="b151b-124">If this lock is granted, no other LOCK\_ONLYONCE lock can be obtained on the range.</span></span> <span data-ttu-id="b151b-125">Geralmente, esse tipo de bloqueio é um alias para algum outro tipo de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="b151b-125">Usually this lock type is an alias for some other lock type.</span></span> <span data-ttu-id="b151b-126">Portanto, implementações específicas podem ter um comportamento adicional associado a esse tipo de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="b151b-126">Thus, specific implementations can have additional behavior associated with this lock type.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b151b-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b151b-127">Return value</span></span>

<span data-ttu-id="b151b-128">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b151b-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="b151b-129">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b151b-129">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b151b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="b151b-130">Remarks</span></span>

<span data-ttu-id="b151b-131">O intervalo de bytes pode ultrapassar a extremidade atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="b151b-131">The byte range can extend past the current end of the stream.</span></span> <span data-ttu-id="b151b-132">O bloqueio além do fim de um fluxo é útil como um método de comunicação entre diferentes instâncias do fluxo sem alterar os dados que realmente fazem parte do fluxo.</span><span class="sxs-lookup"><span data-stu-id="b151b-132">Locking beyond the end of a stream is useful as a method of communication between different instances of the stream without changing data that is actually part of the stream.</span></span>

<span data-ttu-id="b151b-133">Há suporte para três tipos de bloqueio: bloqueio para excluir outros gravadores, bloqueio para excluir outros leitores ou gravadores e bloqueio que permite que apenas um solicitante obtenha um bloqueio no intervalo determinado, que geralmente é um alias para um dos outros dois tipos de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="b151b-133">Three types of locking can be supported: locking to exclude other writers, locking to exclude other readers or writers, and locking that allows only one requester to obtain a lock on the given range, which is usually an alias for one of the other two lock types.</span></span> <span data-ttu-id="b151b-134">Uma determinada instância de fluxo pode dar suporte a qualquer um dos dois primeiros tipos, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="b151b-134">A given stream instance might support either of the first two types, or both.</span></span> <span data-ttu-id="b151b-135">O tipo de bloqueio é especificado por *dwLockType*, usando um valor da enumeração [**LockType**](/windows/win32/api/objidl/ne-objidl-locktype) .</span><span class="sxs-lookup"><span data-stu-id="b151b-135">The lock type is specified by *dwLockType*, using a value from the [**LOCKTYPE**](/windows/win32/api/objidl/ne-objidl-locktype) enumeration.</span></span>

<span data-ttu-id="b151b-136">Qualquer região bloqueada com **LockRegion** deve ser desbloqueada mais tarde chamando [**IByteBuffer:: UnlockRegion**](ibytebuffer-unlockregion.md) com exatamente os mesmos valores para os parâmetros *libOffset*, *CB* e *dwLockType* .</span><span class="sxs-lookup"><span data-stu-id="b151b-136">Any region locked with **LockRegion** must later be explicitly unlocked by calling [**IByteBuffer::UnlockRegion**](ibytebuffer-unlockregion.md) with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="b151b-137">A região deve ser desbloqueada antes de o fluxo ser liberado.</span><span class="sxs-lookup"><span data-stu-id="b151b-137">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="b151b-138">Duas regiões adjacentes não podem ser bloqueadas separadamente e desbloqueadas com uma única chamada de desbloqueio.</span><span class="sxs-lookup"><span data-stu-id="b151b-138">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="b151b-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b151b-139">Examples</span></span>

<span data-ttu-id="b151b-140">O exemplo a seguir mostra a restrição de acesso a um intervalo de bytes.</span><span class="sxs-lookup"><span data-stu-id="b151b-140">The following example shows restricting access to a range of bytes.</span></span>


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="b151b-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b151b-141">Requirements</span></span>



| <span data-ttu-id="b151b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="b151b-142">Requirement</span></span> | <span data-ttu-id="b151b-143">Valor</span><span class="sxs-lookup"><span data-stu-id="b151b-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b151b-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b151b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b151b-145">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b151b-145">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b151b-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b151b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b151b-147">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b151b-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b151b-148">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b151b-148">End of client support</span></span><br/>    | <span data-ttu-id="b151b-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b151b-149">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b151b-150">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b151b-150">End of server support</span></span><br/>    | <span data-ttu-id="b151b-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b151b-151">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b151b-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b151b-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="b151b-153"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b151b-153"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b151b-154">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b151b-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="b151b-155"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b151b-155"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b151b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="b151b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b151b-157"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b151b-157"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b151b-158">IID</span><span class="sxs-lookup"><span data-stu-id="b151b-158">IID</span></span><br/>                      | <span data-ttu-id="b151b-159">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="b151b-159">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

