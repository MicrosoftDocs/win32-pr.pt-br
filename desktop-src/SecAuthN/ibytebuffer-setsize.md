---
description: O método setSize altera o tamanho do objeto de fluxo.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'Método IByteBuffer:: SetSize (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922525"
---
# <a name="ibytebuffersetsize-method"></a><span data-ttu-id="e9fc3-103">Método IByteBuffer:: SetSize</span><span class="sxs-lookup"><span data-stu-id="e9fc3-103">IByteBuffer::SetSize method</span></span>

<span data-ttu-id="e9fc3-104">\[O método **SetSize** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-104">\[The **SetSize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e9fc3-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e9fc3-106">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="e9fc3-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="e9fc3-107">O método **SetSize** altera o tamanho do objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-107">The **SetSize** method changes the size of the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9fc3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9fc3-108">Syntax</span></span>


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a><span data-ttu-id="e9fc3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9fc3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9fc3-110">*libNewSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9fc3-110">*libNewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9fc3-111">Novo tamanho do fluxo como um número de bytes</span><span class="sxs-lookup"><span data-stu-id="e9fc3-111">New size of the stream as a number of bytes</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9fc3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9fc3-112">Return value</span></span>

<span data-ttu-id="e9fc3-113">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-113">The return value is an **HRESULT**.</span></span> <span data-ttu-id="e9fc3-114">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-114">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9fc3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9fc3-115">Remarks</span></span>

<span data-ttu-id="e9fc3-116">O método **IByteBuffer:: SetSize** altera o tamanho do objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-116">The **IByteBuffer::SetSize** method changes the size of the stream object.</span></span> <span data-ttu-id="e9fc3-117">Chame esse método para alocar espaço para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-117">Call this method to preallocate space for the stream.</span></span> <span data-ttu-id="e9fc3-118">Se o parâmetro *libNewSize* for maior que o tamanho atual do fluxo, o fluxo será estendido para o tamanho indicado preenchendo o espaço intermediário com bytes de valor indefinido.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-118">If the *libNewSize* parameter is larger than the current stream size, the stream is extended to the indicated size by filling the intervening space with bytes of undefined value.</span></span> <span data-ttu-id="e9fc3-119">Essa operação é semelhante ao método [**IByteBuffer:: Write**](ibytebuffer-write.md) se o ponteiro de busca estiver além do fim do fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-119">This operation is similar to the [**IByteBuffer::Write**](ibytebuffer-write.md) method if the seek pointer is past the current end-of-stream.</span></span>

<span data-ttu-id="e9fc3-120">Se o parâmetro *libNewSize* for menor do que o fluxo atual, o fluxo será truncado para o tamanho indicado.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-120">If the *libNewSize* parameter is smaller than the current stream, then the stream is truncated to the indicated size.</span></span>

<span data-ttu-id="e9fc3-121">O ponteiro de busca não é afetado pela alteração no tamanho do fluxo.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-121">The seek pointer is not affected by the change in stream size.</span></span>

<span data-ttu-id="e9fc3-122">Chamar **IByteBuffer:: SetSize** pode ser uma maneira eficaz de tentar obter uma grande parte do espaço contíguo.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-122">Calling **IByteBuffer::SetSize** can be an effective way of trying to obtain a large chunk of contiguous space.</span></span>

## <a name="examples"></a><span data-ttu-id="e9fc3-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e9fc3-123">Examples</span></span>

<span data-ttu-id="e9fc3-124">O exemplo a seguir mostra a configuração do tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="e9fc3-124">The following example shows setting the buffer size.</span></span>


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
```



## <a name="requirements"></a><span data-ttu-id="e9fc3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9fc3-125">Requirements</span></span>



| <span data-ttu-id="e9fc3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9fc3-126">Requirement</span></span> | <span data-ttu-id="e9fc3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e9fc3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9fc3-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9fc3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e9fc3-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e9fc3-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e9fc3-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9fc3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e9fc3-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9fc3-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9fc3-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e9fc3-132">End of client support</span></span><br/>    | <span data-ttu-id="e9fc3-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e9fc3-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e9fc3-134">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e9fc3-134">End of server support</span></span><br/>    | <span data-ttu-id="e9fc3-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9fc3-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e9fc3-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9fc3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9fc3-137"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9fc3-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9fc3-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e9fc3-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9fc3-139"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e9fc3-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e9fc3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e9fc3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9fc3-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9fc3-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e9fc3-142">IID</span><span class="sxs-lookup"><span data-stu-id="e9fc3-142">IID</span></span><br/>                      | <span data-ttu-id="e9fc3-143">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="e9fc3-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

