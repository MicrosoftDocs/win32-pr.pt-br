---
description: O método Seek seleciona o objeto do qual o acesso (leitura/gravação) será feito.
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: 'Método ISCardFileAccess:: Seek'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662282"
---
# <a name="iscardfileaccessseek-method"></a><span data-ttu-id="55283-103">Método ISCardFileAccess:: Seek</span><span class="sxs-lookup"><span data-stu-id="55283-103">ISCardFileAccess::Seek method</span></span>

<span data-ttu-id="55283-104">\[O método **Seek** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="55283-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="55283-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="55283-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="55283-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="55283-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="55283-107">O método **Seek** seleciona o objeto do qual o acesso (leitura/gravação) será feito.</span><span class="sxs-lookup"><span data-stu-id="55283-107">The **Seek** method selects the object from which (read/write) access will be done.</span></span>

## <a name="syntax"></a><span data-ttu-id="55283-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55283-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a><span data-ttu-id="55283-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55283-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55283-110">*hFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55283-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55283-111">Identificador do arquivo aberto.</span><span class="sxs-lookup"><span data-stu-id="55283-111">Handle of the open file.</span></span>

</dd> <dt>

<span data-ttu-id="55283-112">*Buscar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55283-112">*Seek* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55283-113">Local em que a busca deve começar.</span><span class="sxs-lookup"><span data-stu-id="55283-113">Location where the seek should begin.</span></span>



| <span data-ttu-id="55283-114">Valor</span><span class="sxs-lookup"><span data-stu-id="55283-114">Value</span></span>                                                                                                | <span data-ttu-id="55283-115">Significado</span><span class="sxs-lookup"><span data-stu-id="55283-115">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="55283-116"><dt>SC \_ Seek \_ do \_ início</dt></span><span class="sxs-lookup"><span data-stu-id="55283-116"><dt>SC\_SEEK\_FROM\_BEGINNING</dt></span></span> </dl> | <span data-ttu-id="55283-117">Comece a pesquisa no início.</span><span class="sxs-lookup"><span data-stu-id="55283-117">Begin search at the beginning.</span></span><br/>          |
| <dl> <span data-ttu-id="55283-118"><dt>SC \_ Seek \_ do \_ final </dt></span><span class="sxs-lookup"><span data-stu-id="55283-118"><dt>SC\_SEEK\_FROM\_END </dt></span></span> </dl>      | <span data-ttu-id="55283-119">Comece a pesquisa a partir do final.</span><span class="sxs-lookup"><span data-stu-id="55283-119">Begin search from the end.</span></span><br/>              |
| <dl> <span data-ttu-id="55283-120"><dt>SC \_ Seek \_ relativo</dt></span><span class="sxs-lookup"><span data-stu-id="55283-120"><dt>SC\_SEEK\_RELATIVE</dt></span></span> </dl>        | <span data-ttu-id="55283-121">Comece a Pesquisar a partir da posição atual.</span><span class="sxs-lookup"><span data-stu-id="55283-121">Begin search from the current position.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="55283-122">*lOffset* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55283-122">*lOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55283-123">Número de objetos de dados do objeto de referência.</span><span class="sxs-lookup"><span data-stu-id="55283-123">Number of data objects from the reference object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55283-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55283-124">Return value</span></span>

<span data-ttu-id="55283-125">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="55283-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="55283-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="55283-126">Return code</span></span>                                                                                   | <span data-ttu-id="55283-127">Description</span><span class="sxs-lookup"><span data-stu-id="55283-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="55283-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55283-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="55283-129">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="55283-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="55283-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="55283-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="55283-131">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="55283-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="55283-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="55283-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="55283-133">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="55283-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="55283-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="55283-134">Remarks</span></span>

<span data-ttu-id="55283-135">Para ler ou gravar um arquivo, chame [**Read**](iscardfileaccess-read.md) ou [**Write**](iscardfileaccess-write.md) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="55283-135">To read to or write from a file, call [**Read**](iscardfileaccess-read.md) or [**Write**](iscardfileaccess-write.md) respectively.</span></span>

<span data-ttu-id="55283-136">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="55283-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="55283-137">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="55283-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="55283-138">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="55283-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55283-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55283-139">Requirements</span></span>



| <span data-ttu-id="55283-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="55283-140">Requirement</span></span> | <span data-ttu-id="55283-141">Valor</span><span class="sxs-lookup"><span data-stu-id="55283-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="55283-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55283-142">Minimum supported client</span></span><br/> | <span data-ttu-id="55283-143">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="55283-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="55283-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55283-144">Minimum supported server</span></span><br/> | <span data-ttu-id="55283-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="55283-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="55283-146">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="55283-146">End of client support</span></span><br/>    | <span data-ttu-id="55283-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="55283-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="55283-148">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="55283-148">End of server support</span></span><br/>    | <span data-ttu-id="55283-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="55283-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="55283-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="55283-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55283-151">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="55283-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="55283-152">**Ler**</span><span class="sxs-lookup"><span data-stu-id="55283-152">**Read**</span></span>](iscardfileaccess-read.md)
</dt> <dt>

[<span data-ttu-id="55283-153">**Gravar**</span><span class="sxs-lookup"><span data-stu-id="55283-153">**Write**</span></span>](iscardfileaccess-write.md)
</dt> </dl>

 

 
