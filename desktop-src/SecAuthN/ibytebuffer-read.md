---
description: O método Read lê um número especificado de bytes do objeto buffer na memória, começando no ponteiro de busca atual.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'Método IByteBuffer:: Read (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0574fb640d60fd8af824ff54abce5d109675ba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171262"
---
# <a name="ibytebufferread-method"></a><span data-ttu-id="79676-103">Método IByteBuffer:: Read</span><span class="sxs-lookup"><span data-stu-id="79676-103">IByteBuffer::Read method</span></span>

<span data-ttu-id="79676-104">\[O método **Read** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="79676-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="79676-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79676-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="79676-106">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="79676-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="79676-107">O método **Read** lê um número especificado de bytes do objeto buffer na memória, começando no ponteiro de busca atual.</span><span class="sxs-lookup"><span data-stu-id="79676-107">The **Read** method reads a specified number of bytes from the buffer object into memory starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="79676-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79676-108">Syntax</span></span>


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="79676-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79676-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79676-110">*pByte* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="79676-110">*pByte* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79676-111">Aponta para o buffer no qual os dados de fluxo são lidos.</span><span class="sxs-lookup"><span data-stu-id="79676-111">Points to the buffer into which the stream data is read.</span></span> <span data-ttu-id="79676-112">Se ocorrer um erro, esse valor será **NULL**.</span><span class="sxs-lookup"><span data-stu-id="79676-112">If an error occurs, this value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="79676-113">*CB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79676-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79676-114">Número de bytes de dados para tentar ler do objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="79676-114">Number of bytes of data to attempt to read from the stream object.</span></span>

</dd> <dt>

<span data-ttu-id="79676-115">*pcbRead* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="79676-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79676-116">Endereço de uma variável **longa** que recebe o número real de bytes lidos do objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="79676-116">Address of a **LONG** variable that receives the actual number of bytes read from the stream object.</span></span> <span data-ttu-id="79676-117">Você pode definir esse ponteiro como **nulo** para indicar que você não está interessado nesse valor.</span><span class="sxs-lookup"><span data-stu-id="79676-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="79676-118">Nesse caso, esse método não fornece o número real de bytes lidos.</span><span class="sxs-lookup"><span data-stu-id="79676-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79676-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79676-119">Return value</span></span>

<span data-ttu-id="79676-120">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="79676-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="79676-121">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="79676-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="79676-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="79676-122">Remarks</span></span>

<span data-ttu-id="79676-123">Esse método lê bytes deste objeto de fluxo na memória.</span><span class="sxs-lookup"><span data-stu-id="79676-123">This method reads bytes from this stream object into memory.</span></span> <span data-ttu-id="79676-124">O objeto de fluxo deve ser aberto no \_ modo de leitura STGM.</span><span class="sxs-lookup"><span data-stu-id="79676-124">The stream object must be opened in STGM\_READ mode.</span></span> <span data-ttu-id="79676-125">Esse método ajusta o ponteiro de busca pelo número real de bytes lidos.</span><span class="sxs-lookup"><span data-stu-id="79676-125">This method adjusts the seek pointer by the actual number of bytes read.</span></span>

<span data-ttu-id="79676-126">O número de bytes realmente lidos também é retornado no parâmetro *pcbRead* .</span><span class="sxs-lookup"><span data-stu-id="79676-126">The number of bytes actually read is also returned in the *pcbRead* parameter.</span></span>

<span data-ttu-id="79676-127">Notas aos Chamadores</span><span class="sxs-lookup"><span data-stu-id="79676-127">Notes to Callers</span></span>

<span data-ttu-id="79676-128">O número real de bytes lidos pode ser menor que o número de bytes solicitados se ocorrer um erro ou se o final do fluxo for atingido durante a operação de leitura.</span><span class="sxs-lookup"><span data-stu-id="79676-128">The actual number of bytes read can be fewer than the number of bytes requested if an error occurs or if the end of the stream is reached during the read operation.</span></span>

<span data-ttu-id="79676-129">Algumas implementações podem retornar um erro se o final do fluxo for atingido durante a leitura.</span><span class="sxs-lookup"><span data-stu-id="79676-129">Some implementations might return an error if the end of the stream is reached during the read.</span></span> <span data-ttu-id="79676-130">Você deve estar preparado para lidar com os valores de retorno de erro ou erros \_ de retorno em OK no fim das leituras de fluxo.</span><span class="sxs-lookup"><span data-stu-id="79676-130">You must be prepared to deal with the error return or S\_OK return values on end of stream reads.</span></span>

## <a name="examples"></a><span data-ttu-id="79676-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="79676-131">Examples</span></span>

<span data-ttu-id="79676-132">O exemplo a seguir mostra os bytes de leitura do buffer.</span><span class="sxs-lookup"><span data-stu-id="79676-132">The following example shows reading bytes from the buffer.</span></span>


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="79676-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79676-133">Requirements</span></span>



| <span data-ttu-id="79676-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="79676-134">Requirement</span></span> | <span data-ttu-id="79676-135">Valor</span><span class="sxs-lookup"><span data-stu-id="79676-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79676-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79676-136">Minimum supported client</span></span><br/> | <span data-ttu-id="79676-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="79676-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="79676-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79676-138">Minimum supported server</span></span><br/> | <span data-ttu-id="79676-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="79676-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="79676-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="79676-140">End of client support</span></span><br/>    | <span data-ttu-id="79676-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="79676-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="79676-142">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="79676-142">End of server support</span></span><br/>    | <span data-ttu-id="79676-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="79676-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="79676-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79676-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="79676-145"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="79676-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="79676-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="79676-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="79676-147"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="79676-147"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="79676-148">DLL</span><span class="sxs-lookup"><span data-stu-id="79676-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79676-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79676-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="79676-150">IID</span><span class="sxs-lookup"><span data-stu-id="79676-150">IID</span></span><br/>                      | <span data-ttu-id="79676-151">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="79676-151">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

