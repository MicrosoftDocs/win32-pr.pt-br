---
description: O método Commit garante que todas as alterações feitas em um objeto aberto no modo transacionado sejam refletidas no armazenamento pai.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'Método IByteBuffer:: Commit (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 066925361d0ee4391bcd1eaafe33e0ae2d4b9120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750505"
---
# <a name="ibytebuffercommit-method"></a><span data-ttu-id="f2796-103">Método IByteBuffer:: Commit</span><span class="sxs-lookup"><span data-stu-id="f2796-103">IByteBuffer::Commit method</span></span>

<span data-ttu-id="f2796-104">\[O método **Commit** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="f2796-104">\[The **Commit** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f2796-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f2796-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f2796-106">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="f2796-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="f2796-107">O método **Commit** garante que todas as alterações feitas em um objeto aberto no modo transacionado sejam refletidas no armazenamento pai.</span><span class="sxs-lookup"><span data-stu-id="f2796-107">The **Commit** method ensures that any changes made to an object open in transacted mode are reflected in the parent storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2796-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2796-108">Syntax</span></span>


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f2796-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2796-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2796-110">*grfCommitFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2796-110">*grfCommitFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2796-111">Controla como as alterações no objeto de fluxo são confirmadas.</span><span class="sxs-lookup"><span data-stu-id="f2796-111">Controls how the changes for the stream object are committed.</span></span> <span data-ttu-id="f2796-112">Para obter uma definição desses valores, consulte a enumeração STGC.</span><span class="sxs-lookup"><span data-stu-id="f2796-112">For a definition of these values, see the STGC enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2796-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2796-113">Return value</span></span>

<span data-ttu-id="f2796-114">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f2796-114">The return value is an **HRESULT**.</span></span> <span data-ttu-id="f2796-115">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f2796-115">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2796-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2796-116">Remarks</span></span>

<span data-ttu-id="f2796-117">Esse método garante que as alterações em um objeto de fluxo aberto no modo transacionado sejam refletidas no armazenamento pai.</span><span class="sxs-lookup"><span data-stu-id="f2796-117">This method ensures that changes to a stream object opened in transacted mode are reflected in the parent storage.</span></span> <span data-ttu-id="f2796-118">As alterações que foram feitas no fluxo desde que ela foi aberta ou confirmadas pela última vez são refletidas no objeto de armazenamento pai.</span><span class="sxs-lookup"><span data-stu-id="f2796-118">Changes that have been made to the stream since it was opened or last committed are reflected to the parent storage object.</span></span> <span data-ttu-id="f2796-119">Se o pai for aberto no modo transacionado, o pai ainda poderá ser revertido em um momento posterior, revertendo as alterações para esse objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f2796-119">If the parent is opened in transacted mode, the parent may still revert at a later time rolling back the changes to this stream object.</span></span> <span data-ttu-id="f2796-120">A implementação do arquivo composto não oferece suporte à abertura de fluxos no modo transacionado, portanto, esse método tem muito pouco efeito além de liberar buffers de memória.</span><span class="sxs-lookup"><span data-stu-id="f2796-120">The compound file implementation does not support opening streams in transacted mode, so this method has very little effect other than to flush memory buffers.</span></span>

## <a name="examples"></a><span data-ttu-id="f2796-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2796-121">Examples</span></span>

<span data-ttu-id="f2796-122">O exemplo a seguir mostra a confirmação de alterações no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f2796-122">The following example shows committing changes to storage.</span></span>


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
```



## <a name="requirements"></a><span data-ttu-id="f2796-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2796-123">Requirements</span></span>



| <span data-ttu-id="f2796-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2796-124">Requirement</span></span> | <span data-ttu-id="f2796-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f2796-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2796-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2796-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f2796-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f2796-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f2796-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2796-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f2796-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2796-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2796-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f2796-130">End of client support</span></span><br/>    | <span data-ttu-id="f2796-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f2796-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f2796-132">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="f2796-132">End of server support</span></span><br/>    | <span data-ttu-id="f2796-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2796-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f2796-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2796-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2796-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2796-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2796-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f2796-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2796-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f2796-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f2796-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f2796-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2796-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2796-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2796-140">IID</span><span class="sxs-lookup"><span data-stu-id="f2796-140">IID</span></span><br/>                      | <span data-ttu-id="f2796-141">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="f2796-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

