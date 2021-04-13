---
description: 'O método REVERT descarta todas as alterações feitas em um fluxo transacionado desde a última chamada IByteBuffer:: Commit.'
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'Método IByteBuffer:: Revert (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164407"
---
# <a name="ibytebufferrevert-method"></a><span data-ttu-id="f049d-103">Método IByteBuffer:: Revert</span><span class="sxs-lookup"><span data-stu-id="f049d-103">IByteBuffer::Revert method</span></span>

<span data-ttu-id="f049d-104">\[O método **REVERT** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="f049d-104">\[The **Revert** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f049d-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f049d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f049d-106">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="f049d-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="f049d-107">O método **REVERT** descarta todas as alterações feitas em um fluxo transacionado desde a última chamada [**IByteBuffer:: Commit**](ibytebuffer-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="f049d-107">The **Revert** method discards all changes that have been made to a transacted stream since the last [**IByteBuffer::Commit**](ibytebuffer-commit.md) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="f049d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f049d-108">Syntax</span></span>


```C++
HRESULT Revert();
```



## <a name="parameters"></a><span data-ttu-id="f049d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f049d-109">Parameters</span></span>

<span data-ttu-id="f049d-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f049d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f049d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f049d-111">Return value</span></span>

<span data-ttu-id="f049d-112">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f049d-112">The return value is an **HRESULT**.</span></span> <span data-ttu-id="f049d-113">Um valor de S \_ OK indica que a chamada foi bem-sucedida e que o fluxo foi revertido para sua versão anterior.</span><span class="sxs-lookup"><span data-stu-id="f049d-113">A value of S\_OK indicates the call was successful and the stream was reverted to its previous version.</span></span>

## <a name="remarks"></a><span data-ttu-id="f049d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f049d-114">Remarks</span></span>

<span data-ttu-id="f049d-115">Esse método descarta as alterações feitas em um fluxo transacionado desde a última operação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="f049d-115">This method discards changes made to a transacted stream since the last commit operation.</span></span>

## <a name="examples"></a><span data-ttu-id="f049d-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f049d-116">Examples</span></span>

<span data-ttu-id="f049d-117">O exemplo a seguir mostra a reversão de um fluxo transacionado para a última operação confirmada.</span><span class="sxs-lookup"><span data-stu-id="f049d-117">The following example shows reverting a transacted stream to the last-committed operation.</span></span>


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a><span data-ttu-id="f049d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f049d-118">Requirements</span></span>



| <span data-ttu-id="f049d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f049d-119">Requirement</span></span> | <span data-ttu-id="f049d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f049d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f049d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f049d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f049d-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f049d-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f049d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f049d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f049d-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f049d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f049d-125">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f049d-125">End of client support</span></span><br/>    | <span data-ttu-id="f049d-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f049d-126">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f049d-127">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="f049d-127">End of server support</span></span><br/>    | <span data-ttu-id="f049d-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f049d-128">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f049d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f049d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f049d-130"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f049d-130"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f049d-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f049d-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="f049d-132"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f049d-132"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f049d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f049d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f049d-134"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f049d-134"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f049d-135">IID</span><span class="sxs-lookup"><span data-stu-id="f049d-135">IID</span></span><br/>                      | <span data-ttu-id="f049d-136">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="f049d-136">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

