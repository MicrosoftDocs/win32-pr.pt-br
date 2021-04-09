---
description: O método Open abre o arquivo especificado para uso posterior.
ms.assetid: a970daba-ed04-45f0-9b2d-3883807050df
title: 'Método ISCardFileAccess:: Open'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Open
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1b68c004d4de308b641a1c4cb187312150f4d2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091524"
---
# <a name="iscardfileaccessopen-method"></a><span data-ttu-id="56596-103">Método ISCardFileAccess:: Open</span><span class="sxs-lookup"><span data-stu-id="56596-103">ISCardFileAccess::Open method</span></span>

<span data-ttu-id="56596-104">\[O método **Open** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="56596-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="56596-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="56596-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="56596-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="56596-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="56596-107">O método **Open** abre o arquivo especificado para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="56596-107">The **Open** method opens the specified file for further use.</span></span>

## <a name="syntax"></a><span data-ttu-id="56596-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56596-108">Syntax</span></span>


```C++
HRESULT Open(
  [in]  REFTYPE     refType,
  [in]  BSTR        bstrPathSpec,
  [out] HSCARD_FILE *phFile
);
```



## <a name="parameters"></a><span data-ttu-id="56596-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56596-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56596-110">*refType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="56596-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56596-111">Tipo de referência usado em *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="56596-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="56596-112">**SC \_ tipo \_ por \_ nome**</span><span class="sxs-lookup"><span data-stu-id="56596-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="56596-113">**SC \_ tipo \_ por \_ ID**</span><span class="sxs-lookup"><span data-stu-id="56596-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="56596-114">**SC \_ tipo \_ por \_ curto**</span><span class="sxs-lookup"><span data-stu-id="56596-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="56596-115">**SC \_ tipo \_ por \_ qualquer**</span><span class="sxs-lookup"><span data-stu-id="56596-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="56596-116">*bstrPathSpec* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="56596-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56596-117">Arquivo a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="56596-117">File to open.</span></span>

</dd> <dt>

<span data-ttu-id="56596-118">*phFile* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="56596-118">*phFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56596-119">Ponteiro para um \_ arquivo HSCARD que conterá o identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="56596-119">Pointer to an HSCARD\_FILE that will hold the file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56596-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56596-120">Return value</span></span>

<span data-ttu-id="56596-121">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="56596-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="56596-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="56596-122">Return code</span></span>                                                                                   | <span data-ttu-id="56596-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="56596-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="56596-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="56596-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="56596-125">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="56596-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="56596-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="56596-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="56596-127">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="56596-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="56596-128"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="56596-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="56596-129">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="56596-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="56596-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="56596-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="56596-131">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="56596-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="56596-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="56596-132">Remarks</span></span>

<span data-ttu-id="56596-133">Para fechar um arquivo, chame [**fechar**](iscardfileaccess-close.md).</span><span class="sxs-lookup"><span data-stu-id="56596-133">To close a file, call [**Close**](iscardfileaccess-close.md).</span></span>

<span data-ttu-id="56596-134">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="56596-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="56596-135">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="56596-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="56596-136">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="56596-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56596-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56596-137">Requirements</span></span>



| <span data-ttu-id="56596-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="56596-138">Requirement</span></span> | <span data-ttu-id="56596-139">Valor</span><span class="sxs-lookup"><span data-stu-id="56596-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="56596-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56596-140">Minimum supported client</span></span><br/> | <span data-ttu-id="56596-141">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="56596-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="56596-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56596-142">Minimum supported server</span></span><br/> | <span data-ttu-id="56596-143">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56596-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="56596-144">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="56596-144">End of client support</span></span><br/>    | <span data-ttu-id="56596-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="56596-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="56596-146">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="56596-146">End of server support</span></span><br/>    | <span data-ttu-id="56596-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56596-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="56596-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="56596-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56596-149">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="56596-149">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="56596-150">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="56596-150">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
