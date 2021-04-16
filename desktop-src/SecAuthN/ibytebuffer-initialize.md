---
description: O método Initialize prepara o objeto IByteBuffer para uso. Esse método deve ser chamado antes de chamar qualquer outro método na interface IByteBuffer.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'Método IByteBuffer:: Initialize (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 245f9282174ddeef66b130597f0f20ddf21ededc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747855"
---
# <a name="ibytebufferinitialize-method"></a><span data-ttu-id="6fd18-104">Método IByteBuffer:: Initialize</span><span class="sxs-lookup"><span data-stu-id="6fd18-104">IByteBuffer::Initialize method</span></span>

<span data-ttu-id="6fd18-105">\[O método **Initialize** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6fd18-105">\[The **Initialize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6fd18-106">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior.</span><span class="sxs-lookup"><span data-stu-id="6fd18-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later.</span></span> <span data-ttu-id="6fd18-107">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="6fd18-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="6fd18-108">O método **Initialize** prepara o objeto [**IByteBuffer**](ibytebuffer.md) para uso.</span><span class="sxs-lookup"><span data-stu-id="6fd18-108">The **Initialize** method prepares the [**IByteBuffer**](ibytebuffer.md) object for use.</span></span> <span data-ttu-id="6fd18-109">Esse método deve ser chamado antes de chamar qualquer outro método na interface **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="6fd18-109">This method must be called prior to calling any other methods in the **IByteBuffer** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd18-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fd18-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a><span data-ttu-id="6fd18-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fd18-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fd18-112">*lSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fd18-112">*lSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fd18-113">Tamanho inicial, em bytes, dos dados que o fluxo deve conter.</span><span class="sxs-lookup"><span data-stu-id="6fd18-113">Initial size, in bytes, of the data the stream is to contain.</span></span>

</dd> <dt>

<span data-ttu-id="6fd18-114">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fd18-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fd18-115">Se não for **NULL**, os dados iniciais a serem gravados no fluxo.</span><span class="sxs-lookup"><span data-stu-id="6fd18-115">If not **NULL**, the initial data to write to the stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fd18-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fd18-116">Return value</span></span>

<span data-ttu-id="6fd18-117">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6fd18-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="6fd18-118">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6fd18-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fd18-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fd18-119">Remarks</span></span>

<span data-ttu-id="6fd18-120">Ao usar um novo fluxo de [**IByteBuffer**](ibytebuffer.md) , chame esse método antes de usar qualquer um dos outros métodos de **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="6fd18-120">When using a new [**IByteBuffer**](ibytebuffer.md) stream, call this method prior to using any of the other **IByteBuffer** methods.</span></span>

## <a name="examples"></a><span data-ttu-id="6fd18-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6fd18-121">Examples</span></span>

<span data-ttu-id="6fd18-122">O exemplo a seguir mostra a inicialização do objeto [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6fd18-122">The following example shows initializing the [**IByteBuffer**](ibytebuffer.md) object.</span></span>


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
```



## <a name="requirements"></a><span data-ttu-id="6fd18-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fd18-123">Requirements</span></span>



| <span data-ttu-id="6fd18-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fd18-124">Requirement</span></span> | <span data-ttu-id="6fd18-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6fd18-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd18-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fd18-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6fd18-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6fd18-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6fd18-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fd18-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6fd18-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6fd18-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6fd18-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6fd18-130">End of client support</span></span><br/>    | <span data-ttu-id="6fd18-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6fd18-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6fd18-132">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="6fd18-132">End of server support</span></span><br/>    | <span data-ttu-id="6fd18-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6fd18-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6fd18-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fd18-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fd18-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fd18-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6fd18-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6fd18-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="6fd18-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6fd18-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6fd18-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6fd18-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fd18-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fd18-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6fd18-140">IID</span><span class="sxs-lookup"><span data-stu-id="6fd18-140">IID</span></span><br/>                      | <span data-ttu-id="6fd18-141">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="6fd18-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

