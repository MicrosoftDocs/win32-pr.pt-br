---
description: O método ChangeDir altera o diretório de cartão inteligente atual para o novo diretório especificado.
ms.assetid: 1eb53236-c88f-4b43-ac91-de67d4029433
title: 'Método ISCardFileAccess:: ChangeDir'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.ChangeDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: 147456bd705eea3073f2e65cb375494187ca2473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827144"
---
# <a name="iscardfileaccesschangedir-method"></a><span data-ttu-id="63dac-103">Método ISCardFileAccess:: ChangeDir</span><span class="sxs-lookup"><span data-stu-id="63dac-103">ISCardFileAccess::ChangeDir method</span></span>

<span data-ttu-id="63dac-104">\[O método **ChangeDir** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="63dac-104">\[The **ChangeDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="63dac-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="63dac-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="63dac-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="63dac-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="63dac-107">O método **ChangeDir** altera o diretório de [*cartão inteligente*](../secgloss/s-gly.md) atual para o novo diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="63dac-107">The **ChangeDir** method changes the current [*smart card*](../secgloss/s-gly.md) directory to the new specified directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="63dac-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63dac-108">Syntax</span></span>


```C++
HRESULT ChangeDir(
  [in] REFTYPE refType,
  [in] BSTR    bstrNewDir
);
```



## <a name="parameters"></a><span data-ttu-id="63dac-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63dac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63dac-110">*refType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63dac-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63dac-111">Tipo de referência usado em *bstrNewDir*.</span><span class="sxs-lookup"><span data-stu-id="63dac-111">Type of reference used in *bstrNewDir*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="63dac-112">**SC \_ tipo \_ por \_ nome**</span><span class="sxs-lookup"><span data-stu-id="63dac-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="63dac-113">**SC \_ tipo \_ por \_ ID**</span><span class="sxs-lookup"><span data-stu-id="63dac-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="63dac-114">**SC \_ tipo \_ por \_ curto**</span><span class="sxs-lookup"><span data-stu-id="63dac-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="63dac-115">**SC \_ tipo \_ por \_ qualquer**</span><span class="sxs-lookup"><span data-stu-id="63dac-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="63dac-116">*bstrNewDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63dac-116">*bstrNewDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63dac-117">Nome do arquivo/diretório (por *refType*) a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="63dac-117">File/directory name (by *refType*) to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63dac-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63dac-118">Return value</span></span>

<span data-ttu-id="63dac-119">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="63dac-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="63dac-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="63dac-120">Return code</span></span>                                                                                   | <span data-ttu-id="63dac-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="63dac-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="63dac-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63dac-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="63dac-123">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="63dac-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="63dac-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="63dac-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="63dac-125">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="63dac-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="63dac-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="63dac-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="63dac-127">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="63dac-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="63dac-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="63dac-128">Remarks</span></span>

<span data-ttu-id="63dac-129">Para obter um caminho absoluto para o diretório atualmente selecionado, chame [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).</span><span class="sxs-lookup"><span data-stu-id="63dac-129">To get an absolute path to the currently selected directory, call [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).</span></span>

<span data-ttu-id="63dac-130">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="63dac-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="63dac-131">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="63dac-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="63dac-132">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="63dac-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63dac-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63dac-133">Requirements</span></span>



| <span data-ttu-id="63dac-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="63dac-134">Requirement</span></span> | <span data-ttu-id="63dac-135">Valor</span><span class="sxs-lookup"><span data-stu-id="63dac-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="63dac-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63dac-136">Minimum supported client</span></span><br/> | <span data-ttu-id="63dac-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="63dac-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="63dac-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63dac-138">Minimum supported server</span></span><br/> | <span data-ttu-id="63dac-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63dac-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="63dac-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="63dac-140">End of client support</span></span><br/>    | <span data-ttu-id="63dac-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="63dac-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="63dac-142">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="63dac-142">End of server support</span></span><br/>    | <span data-ttu-id="63dac-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63dac-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="63dac-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="63dac-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63dac-145">**GetCurrentDir**</span><span class="sxs-lookup"><span data-stu-id="63dac-145">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)
</dt> <dt>

[<span data-ttu-id="63dac-146">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="63dac-146">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
