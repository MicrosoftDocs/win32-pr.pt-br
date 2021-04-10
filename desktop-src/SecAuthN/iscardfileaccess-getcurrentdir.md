---
description: O método GetCurrentDir retorna um caminho absoluto para o diretório selecionado no momento.
ms.assetid: 12196143-a98a-4772-a803-d0c9b95a66e4
title: 'Método ISCardFileAccess:: GetCurrentDir'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetCurrentDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: a779dca10a94250bf4b500585b8b50238b0267dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171995"
---
# <a name="iscardfileaccessgetcurrentdir-method"></a><span data-ttu-id="2afa2-103">Método ISCardFileAccess:: GetCurrentDir</span><span class="sxs-lookup"><span data-stu-id="2afa2-103">ISCardFileAccess::GetCurrentDir method</span></span>

<span data-ttu-id="2afa2-104">\[O método **GetCurrentDir** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2afa2-104">\[The **GetCurrentDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2afa2-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2afa2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2afa2-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="2afa2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2afa2-107">O método **GetCurrentDir** retorna um caminho absoluto para o diretório selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="2afa2-107">The **GetCurrentDir** method returns an absolute path to the currently selected directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="2afa2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2afa2-108">Syntax</span></span>


```C++
HRESULT GetCurrentDir(
  [out] BSTR *pbstrPathSpec
);
```



## <a name="parameters"></a><span data-ttu-id="2afa2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2afa2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2afa2-110">*pbstrPathSpec* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2afa2-110">*pbstrPathSpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2afa2-111">Ponteiro para um BSTR que conterá o caminho.</span><span class="sxs-lookup"><span data-stu-id="2afa2-111">Pointer to a BSTR that will contain the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2afa2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2afa2-112">Return value</span></span>

<span data-ttu-id="2afa2-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="2afa2-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2afa2-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2afa2-114">Return code</span></span>                                                                                   | <span data-ttu-id="2afa2-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="2afa2-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2afa2-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2afa2-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2afa2-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="2afa2-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="2afa2-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2afa2-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2afa2-119">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="2afa2-119">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="2afa2-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="2afa2-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2afa2-121">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="2afa2-121">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="2afa2-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2afa2-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2afa2-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="2afa2-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2afa2-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="2afa2-124">Remarks</span></span>

<span data-ttu-id="2afa2-125">Para alterar o diretório atual, chame [**ChangeDir**](iscardfileaccess-changedir.md).</span><span class="sxs-lookup"><span data-stu-id="2afa2-125">To change the current directory, call [**ChangeDir**](iscardfileaccess-changedir.md).</span></span>

<span data-ttu-id="2afa2-126">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="2afa2-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="2afa2-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2afa2-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2afa2-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2afa2-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2afa2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2afa2-129">Requirements</span></span>



| <span data-ttu-id="2afa2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2afa2-130">Requirement</span></span> | <span data-ttu-id="2afa2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="2afa2-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2afa2-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2afa2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2afa2-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2afa2-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2afa2-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2afa2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2afa2-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2afa2-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2afa2-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2afa2-136">End of client support</span></span><br/>    | <span data-ttu-id="2afa2-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2afa2-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="2afa2-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2afa2-138">End of server support</span></span><br/>    | <span data-ttu-id="2afa2-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2afa2-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="2afa2-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="2afa2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2afa2-141">**ChangeDir**</span><span class="sxs-lookup"><span data-stu-id="2afa2-141">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)
</dt> <dt>

[<span data-ttu-id="2afa2-142">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="2afa2-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
