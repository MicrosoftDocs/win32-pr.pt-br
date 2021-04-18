---
description: O método stat recupera informações estatísticas do objeto Stream.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'Método IByteBuffer:: stat (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752229"
---
# <a name="ibytebufferstat-method"></a><span data-ttu-id="00499-103">Método IByteBuffer:: stat</span><span class="sxs-lookup"><span data-stu-id="00499-103">IByteBuffer::Stat method</span></span>

<span data-ttu-id="00499-104">\[O método **stat** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="00499-104">\[The **Stat** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="00499-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="00499-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="00499-106">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="00499-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="00499-107">O método **stat** recupera informações estatísticas do objeto Stream.</span><span class="sxs-lookup"><span data-stu-id="00499-107">The **Stat** method retrieves statistical information from the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="00499-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00499-108">Syntax</span></span>


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a><span data-ttu-id="00499-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00499-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00499-110">*pStatStg* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="00499-110">*pstatstg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00499-111">Aponta para uma estrutura **STATSTRUCT** em que esse método coloca informações sobre este objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="00499-111">Points to a **STATSTRUCT** structure where this method places information about this stream object.</span></span> <span data-ttu-id="00499-112">Esse ponteiro será **nulo** se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="00499-112">This pointer is **NULL** if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="00499-113">*grfStatFlag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00499-113">*grfStatFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00499-114">Especifica que esse método não retorna alguns dos campos na estrutura **STATSTRUCT** , salvando assim uma operação de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="00499-114">Specifies that this method does not return some of the fields in the **STATSTRUCT** structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="00499-115">Os valores são obtidos da enumeração [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag)</span><span class="sxs-lookup"><span data-stu-id="00499-115">Values are taken from the [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag) enumeration</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00499-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00499-116">Return value</span></span>

<span data-ttu-id="00499-117">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="00499-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="00499-118">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="00499-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="00499-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="00499-119">Remarks</span></span>

<span data-ttu-id="00499-120">O método **IByteBuffer:: stat** recupera um ponteiro para a estrutura **STATSTRUCT** que contém informações sobre esse fluxo aberto.</span><span class="sxs-lookup"><span data-stu-id="00499-120">The **IByteBuffer::Stat** method retrieves a pointer to the **STATSTRUCT** structure that contains information about this open stream.</span></span>

## <a name="examples"></a><span data-ttu-id="00499-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="00499-121">Examples</span></span>

<span data-ttu-id="00499-122">O exemplo a seguir mostra a recuperação de informações estatísticas do fluxo.</span><span class="sxs-lookup"><span data-stu-id="00499-122">The following example shows retrieving statistical information from the stream.</span></span>


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
```



## <a name="requirements"></a><span data-ttu-id="00499-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00499-123">Requirements</span></span>



| <span data-ttu-id="00499-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="00499-124">Requirement</span></span> | <span data-ttu-id="00499-125">Valor</span><span class="sxs-lookup"><span data-stu-id="00499-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00499-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00499-126">Minimum supported client</span></span><br/> | <span data-ttu-id="00499-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="00499-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="00499-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00499-128">Minimum supported server</span></span><br/> | <span data-ttu-id="00499-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="00499-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="00499-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="00499-130">End of client support</span></span><br/>    | <span data-ttu-id="00499-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="00499-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="00499-132">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="00499-132">End of server support</span></span><br/>    | <span data-ttu-id="00499-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00499-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="00499-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00499-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="00499-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="00499-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="00499-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="00499-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="00499-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="00499-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="00499-138">DLL</span><span class="sxs-lookup"><span data-stu-id="00499-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00499-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00499-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="00499-140">IID</span><span class="sxs-lookup"><span data-stu-id="00499-140">IID</span></span><br/>                      | <span data-ttu-id="00499-141">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="00499-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

