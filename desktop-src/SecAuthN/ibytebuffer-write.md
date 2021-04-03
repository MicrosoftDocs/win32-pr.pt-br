---
description: O método Write grava um número especificado de bytes no objeto de fluxo a partir do ponteiro de busca atual.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'Método IByteBuffer:: Write (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5f9b60a296041a18fbd850f1405088f5b0da2ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829764"
---
# <a name="ibytebufferwrite-method"></a><span data-ttu-id="a4c9b-103">Método IByteBuffer:: Write</span><span class="sxs-lookup"><span data-stu-id="a4c9b-103">IByteBuffer::Write method</span></span>

<span data-ttu-id="a4c9b-104">\[O método **Write** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a4c9b-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a4c9b-106">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a4c9b-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="a4c9b-107">O método **Write** grava um número especificado de bytes no objeto de fluxo a partir do ponteiro de busca atual.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-107">The **Write** method writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c9b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4c9b-108">Syntax</span></span>


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="a4c9b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4c9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4c9b-110">*pByte* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4c9b-110">*pByte* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c9b-111">Endereço do buffer que contém os dados que serão gravados no fluxo.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-111">Address of the buffer containing the data that is to be written to the stream.</span></span> <span data-ttu-id="a4c9b-112">Um ponteiro válido deve ser fornecido para esse parâmetro mesmo quando *CB* for zero.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-112">A valid pointer must be provided for this parameter even when *cb* is zero.</span></span>

</dd> <dt>

<span data-ttu-id="a4c9b-113">*CB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4c9b-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c9b-114">Número de bytes de dados para tentar gravar no fluxo.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-114">Number of bytes of data to attempt to write into the stream.</span></span> <span data-ttu-id="a4c9b-115">Esse parâmetro pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-115">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a4c9b-116">*pcbWritten* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a4c9b-116">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c9b-117">Endereço de uma variável **longa** em que esse método grava o número real de bytes gravados no objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-117">Address of a **LONG** variable where this method writes the actual number of bytes written to the stream object.</span></span> <span data-ttu-id="a4c9b-118">O chamador pode definir esse ponteiro como **NULL**; nesse caso, esse método não fornece o número real de bytes gravados.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-118">The caller can set this pointer to **NULL**, in which case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4c9b-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4c9b-119">Return value</span></span>

<span data-ttu-id="a4c9b-120">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="a4c9b-121">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c9b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4c9b-122">Remarks</span></span>

<span data-ttu-id="a4c9b-123">O método **IByteBuffer:: Write** grava os dados especificados em um objeto Stream.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-123">The **IByteBuffer::Write** method writes the specified data to a stream object.</span></span> <span data-ttu-id="a4c9b-124">O ponteiro de busca é ajustado para o número de bytes realmente gravados.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-124">The seek pointer is adjusted for the number of bytes actually written.</span></span> <span data-ttu-id="a4c9b-125">O número de bytes realmente gravados é retornado no parâmetro *pcbWritten* .</span><span class="sxs-lookup"><span data-stu-id="a4c9b-125">The number of bytes actually written is returned in the *pcbWritten* parameter.</span></span> <span data-ttu-id="a4c9b-126">Se a contagem de bytes for zero bytes, a operação de gravação não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-126">If the byte count is zero bytes, the write operation has no effect.</span></span>

<span data-ttu-id="a4c9b-127">Se o ponteiro de busca estiver no momento após o final do fluxo e a contagem de bytes for diferente de zero, esse método aumentará o tamanho do fluxo para o ponteiro de busca e gravará os bytes especificados a partir do ponteiro de busca.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-127">If the seek pointer is currently past the end of the stream and the byte count is nonzero, this method increases the size of the stream to the seek pointer and writes the specified bytes starting at the seek pointer.</span></span> <span data-ttu-id="a4c9b-128">Os bytes de preenchimento gravados no fluxo não são inicializados para nenhum valor específico.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-128">The fill bytes written to the stream are not initialized to any particular value.</span></span> <span data-ttu-id="a4c9b-129">Isso é o mesmo que o comportamento final do arquivo no sistema de arquivos FAT do MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-129">This is the same as the end-of-file behavior in the MS-DOS FAT file system.</span></span>

<span data-ttu-id="a4c9b-130">Com uma contagem de bytes zero e um ponteiro de busca após o final do fluxo, esse método não cria os bytes de preenchimento para aumentar o fluxo para o ponteiro de busca.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-130">With a zero byte count and a seek pointer past the end of the stream, this method does not create the fill bytes to increase the stream to the seek pointer.</span></span> <span data-ttu-id="a4c9b-131">Nesse caso, você deve chamar o método [**IByteBuffer:: SetSize**](ibytebuffer-setsize.md) para aumentar o tamanho do fluxo e gravar os bytes de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-131">In this case, you must call the [**IByteBuffer::SetSize**](ibytebuffer-setsize.md) method to increase the size of the stream and write the fill bytes.</span></span>

<span data-ttu-id="a4c9b-132">O parâmetro *pcbWritten* pode ter um valor mesmo se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-132">The *pcbWritten* parameter can have a value even if an error occurs.</span></span>

<span data-ttu-id="a4c9b-133">Na implementação fornecida COM, os objetos de fluxo não são esparsos.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-133">In the COM-provided implementation, stream objects are not sparse.</span></span> <span data-ttu-id="a4c9b-134">Todos os bytes de preenchimento são eventualmente alocados no disco e atribuídos ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-134">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

## <a name="examples"></a><span data-ttu-id="a4c9b-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4c9b-135">Examples</span></span>

<span data-ttu-id="a4c9b-136">O exemplo a seguir mostra a gravação de bytes no objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a4c9b-136">The following example shows writing bytes into the stream object.</span></span>


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
```



## <a name="requirements"></a><span data-ttu-id="a4c9b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4c9b-137">Requirements</span></span>



| <span data-ttu-id="a4c9b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4c9b-138">Requirement</span></span> | <span data-ttu-id="a4c9b-139">Valor</span><span class="sxs-lookup"><span data-stu-id="a4c9b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c9b-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4c9b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c9b-141">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a4c9b-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a4c9b-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4c9b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c9b-143">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a4c9b-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a4c9b-144">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a4c9b-144">End of client support</span></span><br/>    | <span data-ttu-id="a4c9b-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a4c9b-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a4c9b-146">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a4c9b-146">End of server support</span></span><br/>    | <span data-ttu-id="a4c9b-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a4c9b-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a4c9b-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4c9b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4c9b-149"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4c9b-149"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4c9b-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a4c9b-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4c9b-151"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a4c9b-151"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a4c9b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="a4c9b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4c9b-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4c9b-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4c9b-154">IID</span><span class="sxs-lookup"><span data-stu-id="a4c9b-154">IID</span></span><br/>                      | <span data-ttu-id="a4c9b-155">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="a4c9b-155">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

