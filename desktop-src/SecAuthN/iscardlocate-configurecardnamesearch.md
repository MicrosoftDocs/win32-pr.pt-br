---
description: O método ConfigureCardNameSearch especifica os nomes de cartão a serem usados na pesquisa do cartão inteligente.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'Método ISCardLocate:: ConfigureCardNameSearch (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170022"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a><span data-ttu-id="5049f-103">Método ISCardLocate:: ConfigureCardNameSearch</span><span class="sxs-lookup"><span data-stu-id="5049f-103">ISCardLocate::ConfigureCardNameSearch method</span></span>

<span data-ttu-id="5049f-104">\[O método **ConfigureCardNameSearch** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="5049f-104">\[The **ConfigureCardNameSearch** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5049f-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5049f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5049f-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="5049f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5049f-107">O método **ConfigureCardNameSearch** especifica os nomes de cartão a serem usados na pesquisa do [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5049f-107">The **ConfigureCardNameSearch** method specifies the card names to be used in the search for the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5049f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5049f-108">Syntax</span></span>


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5049f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5049f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5049f-110">*pCardNames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5049f-110">*pCardNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5049f-111">Um ponteiro para uma matriz segura de automação de nomes de cartão na forma BSTR.</span><span class="sxs-lookup"><span data-stu-id="5049f-111">A pointer to an Automation safe array of card names in BSTR form.</span></span>

</dd> <dt>

<span data-ttu-id="5049f-112">*pGroupNames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5049f-112">*pGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5049f-113">Um ponteiro para uma matriz segura de automação de nomes de grupos de cartões/leitores no formato BSTR para adicionar à pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5049f-113">A pointer to an Automation safe array of names of card/reader groups in BSTR form to add to the search.</span></span>

</dd> <dt>

<span data-ttu-id="5049f-114">*bstrTitle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5049f-114">*bstrTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5049f-115">Título da caixa de diálogo para o controle comum de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5049f-115">Dialog box title for the search common control.</span></span>

</dd> <dt>

<span data-ttu-id="5049f-116">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5049f-116">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5049f-117">Especifica quando a [*interface do usuário*](../secgloss/u-gly.md) é exibida.</span><span class="sxs-lookup"><span data-stu-id="5049f-117">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed.</span></span>



| <span data-ttu-id="5049f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5049f-118">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="5049f-119">Significado</span><span class="sxs-lookup"><span data-stu-id="5049f-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="5049f-120"><dt>**\_ \_ IU mínima SC \_ Dlg**</dt></span><span class="sxs-lookup"><span data-stu-id="5049f-120"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="5049f-121">Exibe a caixa de diálogo somente se o cartão que está sendo pesquisado pelo aplicativo de chamada não estiver localizado e disponível para uso em um leitor.</span><span class="sxs-lookup"><span data-stu-id="5049f-121">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="5049f-122">Isso permite que o cartão seja encontrado, conectado (por meio de um mecanismo de caixa de diálogo interno ou usando as funções de retorno de chamada do usuário) e retornado ao aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="5049f-122">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="5049f-123"><dt>**SC \_ DLG \_ sem \_ interface do usuário**</dt></span><span class="sxs-lookup"><span data-stu-id="5049f-123"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="5049f-124">Não faz nenhuma exibição da interface do usuário, independentemente do resultado da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5049f-124">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="5049f-125"><dt>**\_IU de \_ força \_ do SC Dlg**</dt></span><span class="sxs-lookup"><span data-stu-id="5049f-125"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="5049f-126">Faz com que a interface do usuário seja exibida, independentemente do resultado da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5049f-126">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5049f-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5049f-127">Return value</span></span>

<span data-ttu-id="5049f-128">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="5049f-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5049f-129">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5049f-129">Return code</span></span>                                                                                   | <span data-ttu-id="5049f-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="5049f-130">Description</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="5049f-131"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5049f-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5049f-132">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="5049f-132">Operation completed successfully.</span></span><br/>                          |
| <dl> <span data-ttu-id="5049f-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5049f-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5049f-134">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="5049f-134">Invalid parameter.</span></span><br/>                                         |
| <dl> <span data-ttu-id="5049f-135"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="5049f-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5049f-136">Um ponteiro inadequado foi passado em *pCardNames* ou *pGroupNames*.</span><span class="sxs-lookup"><span data-stu-id="5049f-136">A bad pointer was passed in *pCardNames* or *pGroupNames*.</span></span><br/> |
| <dl> <span data-ttu-id="5049f-137"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5049f-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5049f-138">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="5049f-138">Out of memory.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="5049f-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="5049f-139">Remarks</span></span>

<span data-ttu-id="5049f-140">Para localizar o [*cartão inteligente*](../secgloss/s-gly.md), chame [**FindCard**](iscardlocate-findcard.md).</span><span class="sxs-lookup"><span data-stu-id="5049f-140">To locate the [*smart card*](../secgloss/s-gly.md), call [**FindCard**](iscardlocate-findcard.md).</span></span>

<span data-ttu-id="5049f-141">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardLocate**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="5049f-141">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="5049f-142">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="5049f-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5049f-143">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5049f-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5049f-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5049f-144">Requirements</span></span>



| <span data-ttu-id="5049f-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="5049f-145">Requirement</span></span> | <span data-ttu-id="5049f-146">Valor</span><span class="sxs-lookup"><span data-stu-id="5049f-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5049f-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5049f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="5049f-148">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5049f-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5049f-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5049f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="5049f-150">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5049f-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5049f-151">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5049f-151">End of client support</span></span><br/>    | <span data-ttu-id="5049f-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5049f-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5049f-153">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="5049f-153">End of server support</span></span><br/>    | <span data-ttu-id="5049f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5049f-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5049f-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5049f-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="5049f-156"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="5049f-156"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="5049f-157">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5049f-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="5049f-158"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5049f-158"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5049f-159">DLL</span><span class="sxs-lookup"><span data-stu-id="5049f-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5049f-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5049f-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5049f-161">IID</span><span class="sxs-lookup"><span data-stu-id="5049f-161">IID</span></span><br/>                      | <span data-ttu-id="5049f-162">IID \_ ISCardLocate é definido como 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="5049f-162">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="5049f-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="5049f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5049f-164">**FindCard**</span><span class="sxs-lookup"><span data-stu-id="5049f-164">**FindCard**</span></span>](iscardlocate-findcard.md)
</dt> <dt>

[<span data-ttu-id="5049f-165">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="5049f-165">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
