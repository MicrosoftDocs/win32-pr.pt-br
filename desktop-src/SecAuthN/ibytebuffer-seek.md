---
description: O método Seek altera o ponteiro de busca para um novo local relativo ao início do buffer, para o final do buffer ou para o ponteiro de busca atual.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'Método IByteBuffer:: Seek (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eacfedc3ed23a7a4cf1f60e6c6ac21936c3c94f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829765"
---
# <a name="ibytebufferseek-method"></a><span data-ttu-id="9ae25-103">Método IByteBuffer:: Seek</span><span class="sxs-lookup"><span data-stu-id="9ae25-103">IByteBuffer::Seek method</span></span>

<span data-ttu-id="9ae25-104">\[O método **Seek** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="9ae25-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9ae25-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9ae25-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9ae25-106">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="9ae25-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="9ae25-107">O método **Seek** altera o ponteiro de busca para um novo local relativo ao início do buffer, para o final do buffer ou para o ponteiro de busca atual.</span><span class="sxs-lookup"><span data-stu-id="9ae25-107">The **Seek** method changes the seek pointer to a new location relative to the beginning of the buffer, to the end of the buffer, or to the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae25-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ae25-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a><span data-ttu-id="9ae25-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ae25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ae25-110">*dlibMove* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ae25-110">*dlibMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ae25-111">O deslocamento a ser adicionado ao local indicado por *dwOrigin*.</span><span class="sxs-lookup"><span data-stu-id="9ae25-111">Displacement to be added to the location indicated by *dwOrigin*.</span></span> <span data-ttu-id="9ae25-112">Se *dwOrigin* for \_ conjunto de busca de fluxo \_ , isso será interpretado como um valor não assinado em vez de assinada.</span><span class="sxs-lookup"><span data-stu-id="9ae25-112">If *dwOrigin* is STREAM\_SEEK\_SET, this is interpreted as an unsigned value rather than signed.</span></span>

</dd> <dt>

<span data-ttu-id="9ae25-113">*dwOrigin* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ae25-113">*dwOrigin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ae25-114">Especifica a origem para o deslocamento especificado em *dlibMove*.</span><span class="sxs-lookup"><span data-stu-id="9ae25-114">Specifies the origin for the displacement specified in *dlibMove*.</span></span> <span data-ttu-id="9ae25-115">A origem pode ser um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9ae25-115">The origin can be one of the values in the following table.</span></span>



| <span data-ttu-id="9ae25-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9ae25-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="9ae25-117">Significado</span><span class="sxs-lookup"><span data-stu-id="9ae25-117">Meaning</span></span>                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <span data-ttu-id="9ae25-118"><dt>**\_conjunto de busca de fluxo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9ae25-118"><dt>**STREAM\_SEEK\_SET**</dt></span></span> </dl> | <span data-ttu-id="9ae25-119">O novo ponteiro de busca é um deslocamento relativo ao início do fluxo.</span><span class="sxs-lookup"><span data-stu-id="9ae25-119">The new seek pointer is an offset relative to the beginning of the stream.</span></span> <span data-ttu-id="9ae25-120">Nesse caso, o parâmetro *dlibMove* é a nova posição de busca relativa ao início do fluxo.</span><span class="sxs-lookup"><span data-stu-id="9ae25-120">In this case, the *dlibMove* parameter is the new seek position relative to the beginning of the stream.</span></span><br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <span data-ttu-id="9ae25-121"><dt>**\_pesquisa de busca de fluxo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9ae25-121"><dt>**STREAM\_SEEK\_CUR**</dt></span></span> </dl> | <span data-ttu-id="9ae25-122">O novo ponteiro de busca é um deslocamento relativo ao local do ponteiro de busca atual.</span><span class="sxs-lookup"><span data-stu-id="9ae25-122">The new seek pointer is an offset relative to the current seek pointer location.</span></span> <span data-ttu-id="9ae25-123">Nesse caso, o parâmetro *dlibMove* é o deslocamento assinado da posição de busca atual.</span><span class="sxs-lookup"><span data-stu-id="9ae25-123">In this case, the *dlibMove* parameter is the signed displacement from the current seek position.</span></span><br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <span data-ttu-id="9ae25-124"><dt>**fim do fluxo de \_ busca \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9ae25-124"><dt>**STREAM\_SEEK\_END**</dt></span></span> </dl> | <span data-ttu-id="9ae25-125">O novo ponteiro de busca é um deslocamento relativo ao final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="9ae25-125">The new seek pointer is an offset relative to the end of the stream.</span></span> <span data-ttu-id="9ae25-126">Nesse caso, o parâmetro *dlibMove* é a nova posição de busca relativa ao final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="9ae25-126">In this case, the *dlibMove* parameter is the new seek position relative to the end of the stream.</span></span><br/>             |



 

</dd> <dt>

<span data-ttu-id="9ae25-127">*plibNewPosition* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9ae25-127">*plibNewPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ae25-128">Ponteiro para o local em que esse método grava o valor do novo ponteiro de busca do início do fluxo.</span><span class="sxs-lookup"><span data-stu-id="9ae25-128">Pointer to the location where this method writes the value of the new seek pointer from the beginning of the stream.</span></span> <span data-ttu-id="9ae25-129">Você pode definir esse ponteiro como **nulo** para indicar que você não está interessado nesse valor.</span><span class="sxs-lookup"><span data-stu-id="9ae25-129">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="9ae25-130">Nesse caso, esse método não fornece o novo ponteiro de busca.</span><span class="sxs-lookup"><span data-stu-id="9ae25-130">In this case, this method does not provide the new seek pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ae25-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ae25-131">Return value</span></span>

<span data-ttu-id="9ae25-132">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9ae25-132">The return value is an **HRESULT**.</span></span> <span data-ttu-id="9ae25-133">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9ae25-133">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ae25-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ae25-134">Remarks</span></span>

<span data-ttu-id="9ae25-135">O método **Seek** altera o ponteiro de busca para que as operações de leitura e gravação subsequentes possam ocorrer em um local diferente no objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="9ae25-135">The **Seek** method changes the seek pointer so subsequent read and write operations can take place at a different location in the stream object.</span></span> <span data-ttu-id="9ae25-136">É um erro a ser buscado antes do início do fluxo.</span><span class="sxs-lookup"><span data-stu-id="9ae25-136">It is an error to seek before the beginning of the stream.</span></span> <span data-ttu-id="9ae25-137">No entanto, não há um erro a ser buscado após o final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="9ae25-137">It is not, however, an error to seek past the end of the stream.</span></span> <span data-ttu-id="9ae25-138">A busca após o final do fluxo é útil para operações de gravação subsequentes, pois o fluxo nesse momento será estendido para a posição de busca imediatamente antes que a operação de gravação seja feita.</span><span class="sxs-lookup"><span data-stu-id="9ae25-138">Seeking past the end of the stream is useful for subsequent write operations, as the stream will at that time be extended to the seek position immediately before the write operation is done.</span></span>

<span data-ttu-id="9ae25-139">Você também pode usar esse método para obter o valor atual do ponteiro de busca chamando esse método com o parâmetro *dwOrigin* definido como Stream \_ Seek \_ cur e o parâmetro *dlibMove* definido como zero para que o ponteiro de busca não seja alterado.</span><span class="sxs-lookup"><span data-stu-id="9ae25-139">You can also use this method to obtain the current value of the seek pointer by calling this method with the *dwOrigin* parameter set to STREAM\_SEEK\_CUR and the *dlibMove* parameter set to zero so the seek pointer is not changed.</span></span> <span data-ttu-id="9ae25-140">O ponteiro de busca atual é retornado no parâmetro *plibNewPosition* .</span><span class="sxs-lookup"><span data-stu-id="9ae25-140">The current seek pointer is returned in the *plibNewPosition* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="9ae25-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ae25-141">Examples</span></span>

<span data-ttu-id="9ae25-142">O exemplo a seguir mostra o posicionamento do ponteiro de busca em um novo local.</span><span class="sxs-lookup"><span data-stu-id="9ae25-142">The following example shows positioning the seek pointer to a new location.</span></span>


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
```



## <a name="requirements"></a><span data-ttu-id="9ae25-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ae25-143">Requirements</span></span>



| <span data-ttu-id="9ae25-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ae25-144">Requirement</span></span> | <span data-ttu-id="9ae25-145">Valor</span><span class="sxs-lookup"><span data-stu-id="9ae25-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae25-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ae25-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae25-147">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9ae25-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9ae25-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ae25-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae25-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ae25-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ae25-150">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="9ae25-150">End of client support</span></span><br/>    | <span data-ttu-id="9ae25-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9ae25-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9ae25-152">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="9ae25-152">End of server support</span></span><br/>    | <span data-ttu-id="9ae25-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ae25-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9ae25-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ae25-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ae25-155"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ae25-155"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ae25-156">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9ae25-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ae25-157"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ae25-157"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9ae25-158">DLL</span><span class="sxs-lookup"><span data-stu-id="9ae25-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ae25-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ae25-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9ae25-160">IID</span><span class="sxs-lookup"><span data-stu-id="9ae25-160">IID</span></span><br/>                      | <span data-ttu-id="9ae25-161">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="9ae25-161">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

