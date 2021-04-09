---
description: O método CopyTo copia um número especificado de bytes do ponteiro de busca atual no objeto para o ponteiro de busca atual em outro objeto.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'Método IByteBuffer:: CopyTo (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171267"
---
# <a name="ibytebuffercopyto-method"></a><span data-ttu-id="61b35-103">Método IByteBuffer:: CopyTo</span><span class="sxs-lookup"><span data-stu-id="61b35-103">IByteBuffer::CopyTo method</span></span>

<span data-ttu-id="61b35-104">\[O método **CopyTo** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="61b35-104">\[The **CopyTo** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="61b35-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="61b35-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="61b35-106">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="61b35-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="61b35-107">O método **CopyTo** copia um número especificado de bytes do ponteiro de busca atual no objeto para o ponteiro de busca atual em outro objeto.</span><span class="sxs-lookup"><span data-stu-id="61b35-107">The **CopyTo** method copies a specified number of bytes from the current seek pointer in the object to the current seek pointer in another object.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b35-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61b35-108">Syntax</span></span>


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="61b35-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61b35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61b35-110">*pByteBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61b35-110">*pByteBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61b35-111">Aponta para o fluxo de destino.</span><span class="sxs-lookup"><span data-stu-id="61b35-111">Points to the destination stream.</span></span> <span data-ttu-id="61b35-112">O fluxo apontado por *pByteBuffer* pode ser um novo fluxo ou um clone do fluxo de origem.</span><span class="sxs-lookup"><span data-stu-id="61b35-112">The stream pointed to by *pByteBuffer* can be a new stream or a clone of the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="61b35-113">*CB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61b35-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61b35-114">Número de bytes a serem copiados do fluxo de origem.</span><span class="sxs-lookup"><span data-stu-id="61b35-114">Number of bytes to copy from the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="61b35-115">*pcbRead* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="61b35-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61b35-116">Aponta para o local em que esse método grava o número real de bytes lidos da origem.</span><span class="sxs-lookup"><span data-stu-id="61b35-116">Pointer to the location where this method writes the actual number of bytes read from the source.</span></span> <span data-ttu-id="61b35-117">Você pode definir esse ponteiro como **nulo** para indicar que você não está interessado nesse valor.</span><span class="sxs-lookup"><span data-stu-id="61b35-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="61b35-118">Nesse caso, esse método não fornece o número real de bytes lidos.</span><span class="sxs-lookup"><span data-stu-id="61b35-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="61b35-119">*pcbWritten* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="61b35-119">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61b35-120">Aponta para o local em que esse método grava o número real de bytes gravados no destino.</span><span class="sxs-lookup"><span data-stu-id="61b35-120">Pointer to the location where this method writes the actual number of bytes written to the destination.</span></span> <span data-ttu-id="61b35-121">Você pode definir esse ponteiro como **nulo** para indicar que você não está interessado nesse valor.</span><span class="sxs-lookup"><span data-stu-id="61b35-121">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="61b35-122">Nesse caso, esse método não fornece o número real de bytes gravados.</span><span class="sxs-lookup"><span data-stu-id="61b35-122">In this case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61b35-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61b35-123">Return value</span></span>

<span data-ttu-id="61b35-124">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="61b35-124">The return value is an **HRESULT**.</span></span> <span data-ttu-id="61b35-125">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="61b35-125">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="61b35-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="61b35-126">Remarks</span></span>

<span data-ttu-id="61b35-127">Esse método copia os bytes especificados de um fluxo para outro.</span><span class="sxs-lookup"><span data-stu-id="61b35-127">This method copies the specified bytes from one stream to another.</span></span> <span data-ttu-id="61b35-128">Ele também pode ser usado para copiar um fluxo para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="61b35-128">It can also be used to copy a stream to itself.</span></span> <span data-ttu-id="61b35-129">O ponteiro de busca em cada instância de fluxo é ajustado para o número de bytes lidos ou gravados.</span><span class="sxs-lookup"><span data-stu-id="61b35-129">The seek pointer in each stream instance is adjusted for the number of bytes read or written.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b35-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61b35-130">Requirements</span></span>



| <span data-ttu-id="61b35-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="61b35-131">Requirement</span></span> | <span data-ttu-id="61b35-132">Valor</span><span class="sxs-lookup"><span data-stu-id="61b35-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61b35-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61b35-133">Minimum supported client</span></span><br/> | <span data-ttu-id="61b35-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="61b35-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="61b35-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61b35-135">Minimum supported server</span></span><br/> | <span data-ttu-id="61b35-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="61b35-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="61b35-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="61b35-137">End of client support</span></span><br/>    | <span data-ttu-id="61b35-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="61b35-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="61b35-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="61b35-139">End of server support</span></span><br/>    | <span data-ttu-id="61b35-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61b35-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="61b35-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61b35-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="61b35-142"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="61b35-142"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="61b35-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="61b35-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="61b35-144"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="61b35-144"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="61b35-145">DLL</span><span class="sxs-lookup"><span data-stu-id="61b35-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61b35-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61b35-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="61b35-147">IID</span><span class="sxs-lookup"><span data-stu-id="61b35-147">IID</span></span><br/>                      | <span data-ttu-id="61b35-148">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="61b35-148">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

