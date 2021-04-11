---
description: O método clone cria um novo objeto com seu próprio ponteiro de busca que faz referência aos mesmos bytes do objeto IByteBuffer original.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'Método IByteBuffer:: clone (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170822"
---
# <a name="ibytebufferclone-method"></a><span data-ttu-id="fdc49-103">Método IByteBuffer:: clone</span><span class="sxs-lookup"><span data-stu-id="fdc49-103">IByteBuffer::Clone method</span></span>

<span data-ttu-id="fdc49-104">\[O método **clone** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="fdc49-104">\[The **Clone** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fdc49-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fdc49-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fdc49-106">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="fdc49-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="fdc49-107">O método **clone** cria um novo objeto com seu próprio ponteiro de busca que faz referência aos mesmos bytes do objeto [**IByteBuffer**](ibytebuffer.md) original.</span><span class="sxs-lookup"><span data-stu-id="fdc49-107">The **Clone** method creates a new object with its own seek pointer that references the same bytes as the original [**IByteBuffer**](ibytebuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc49-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdc49-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="fdc49-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdc49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdc49-110">*ppByteBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fdc49-110">*ppByteBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdc49-111">Quando bem-sucedido, aponta para o local de um ponteiro [**IByteBuffer**](ibytebuffer.md) para o novo objeto Stream.</span><span class="sxs-lookup"><span data-stu-id="fdc49-111">When successful, points to the location of an [**IByteBuffer**](ibytebuffer.md) pointer to the new stream object.</span></span> <span data-ttu-id="fdc49-112">Quando você terminar de usar o ponteiro **IByteBuffer** , libere-o chamando a função [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="fdc49-112">When you have finished using the **IByteBuffer** pointer, release it by calling the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) function.</span></span> <span data-ttu-id="fdc49-113">Se ocorrer um erro, esse parâmetro será **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fdc49-113">If an error occurs, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdc49-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fdc49-114">Return value</span></span>

<span data-ttu-id="fdc49-115">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fdc49-115">The return value is an **HRESULT**.</span></span> <span data-ttu-id="fdc49-116">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fdc49-116">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdc49-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdc49-117">Remarks</span></span>

<span data-ttu-id="fdc49-118">Esse método cria um novo objeto de fluxo para acessar os mesmos bytes, mas usando um ponteiro de busca separado.</span><span class="sxs-lookup"><span data-stu-id="fdc49-118">This method creates a new stream object for accessing the same bytes but using a separate seek pointer.</span></span> <span data-ttu-id="fdc49-119">O novo objeto de fluxo vê os mesmos dados que o objeto de fluxo de origem.</span><span class="sxs-lookup"><span data-stu-id="fdc49-119">The new stream object sees the same data as the source stream object.</span></span> <span data-ttu-id="fdc49-120">As alterações gravadas em um objeto ficam imediatamente visíveis no outro.</span><span class="sxs-lookup"><span data-stu-id="fdc49-120">Changes written to one object are immediately visible in the other.</span></span> <span data-ttu-id="fdc49-121">O bloqueio de intervalo é compartilhado entre os objetos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fdc49-121">Range locking is shared between the stream objects.</span></span>

<span data-ttu-id="fdc49-122">A configuração inicial do ponteiro de busca na instância de fluxo clonado é igual à configuração atual do ponteiro de busca no fluxo original no momento da operação de clonagem.</span><span class="sxs-lookup"><span data-stu-id="fdc49-122">The initial setting of the seek pointer in the cloned stream instance is the same as the current setting of the seek pointer in the original stream at the time of the clone operation.</span></span>

## <a name="examples"></a><span data-ttu-id="fdc49-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fdc49-123">Examples</span></span>

<span data-ttu-id="fdc49-124">O exemplo a seguir mostra a clonagem da interface [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="fdc49-124">The following example shows cloning the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
```



## <a name="requirements"></a><span data-ttu-id="fdc49-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdc49-125">Requirements</span></span>



| <span data-ttu-id="fdc49-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdc49-126">Requirement</span></span> | <span data-ttu-id="fdc49-127">Valor</span><span class="sxs-lookup"><span data-stu-id="fdc49-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc49-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdc49-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc49-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fdc49-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fdc49-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdc49-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc49-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fdc49-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fdc49-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="fdc49-132">End of client support</span></span><br/>    | <span data-ttu-id="fdc49-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fdc49-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fdc49-134">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="fdc49-134">End of server support</span></span><br/>    | <span data-ttu-id="fdc49-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fdc49-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fdc49-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdc49-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdc49-137"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdc49-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fdc49-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fdc49-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="fdc49-139"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fdc49-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fdc49-140">DLL</span><span class="sxs-lookup"><span data-stu-id="fdc49-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdc49-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdc49-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fdc49-142">IID</span><span class="sxs-lookup"><span data-stu-id="fdc49-142">IID</span></span><br/>                      | <span data-ttu-id="fdc49-143">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="fdc49-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

