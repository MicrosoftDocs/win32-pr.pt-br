---
description: O método FindCard pesquisa o cartão inteligente e abre uma conexão válida com ele.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'Método ISCardLocate:: FindCard (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bf3cf05ff6e6040d5cac2bde161fa2eea07d5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747853"
---
# <a name="iscardlocatefindcard-method"></a><span data-ttu-id="a2222-103">Método ISCardLocate:: FindCard</span><span class="sxs-lookup"><span data-stu-id="a2222-103">ISCardLocate::FindCard method</span></span>

<span data-ttu-id="a2222-104">\[O método **FindCard** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a2222-104">\[The **FindCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a2222-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a2222-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a2222-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a2222-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a2222-107">O método **FindCard** pesquisa o [*cartão inteligente*](../secgloss/s-gly.md) e abre uma conexão válida com ele.</span><span class="sxs-lookup"><span data-stu-id="a2222-107">The **FindCard** method searches for the [*smart card*](../secgloss/s-gly.md) and opens a valid connection to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2222-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2222-108">Syntax</span></span>


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a2222-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2222-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2222-110">*ShareMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2222-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2222-111">Modo no qual compartilhar ou não compartilhar o cartão inteligente quando uma conexão é aberta a ele.</span><span class="sxs-lookup"><span data-stu-id="a2222-111">Mode in which to share or not share the smart card when a connection is opened to it.</span></span>



| <span data-ttu-id="a2222-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a2222-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="a2222-113">Significado</span><span class="sxs-lookup"><span data-stu-id="a2222-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="a2222-114"><dt>**Exclude**</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="a2222-115">Ninguém mais usa essa conexão com o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="a2222-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="a2222-116"><dt>**COMPARTILHADO**</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="a2222-117">Outros aplicativos podem usar essa conexão.</span><span class="sxs-lookup"><span data-stu-id="a2222-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="a2222-118">*Protocolos* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a2222-118">*Protocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2222-119">Protocolo a ser usado ao conectar-se ao cartão.</span><span class="sxs-lookup"><span data-stu-id="a2222-119">Protocol to use when connecting to the card.</span></span>

<span data-ttu-id="a2222-120">T0</span><span class="sxs-lookup"><span data-stu-id="a2222-120">T0</span></span>

<span data-ttu-id="a2222-121">T1</span><span class="sxs-lookup"><span data-stu-id="a2222-121">T1</span></span>

<span data-ttu-id="a2222-122">RAW</span><span class="sxs-lookup"><span data-stu-id="a2222-122">RAW</span></span>

<span data-ttu-id="a2222-123">T0 \| T1</span><span class="sxs-lookup"><span data-stu-id="a2222-123">T0\|T1</span></span>

</dd> <dt>

<span data-ttu-id="a2222-124">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2222-124">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2222-125">Especifica quando a [*interface do usuário*](../secgloss/u-gly.md) é exibida:</span><span class="sxs-lookup"><span data-stu-id="a2222-125">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed:</span></span>



| <span data-ttu-id="a2222-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a2222-126">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="a2222-127">Significado</span><span class="sxs-lookup"><span data-stu-id="a2222-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="a2222-128"><dt>**\_ \_ IU mínima SC \_ Dlg**</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-128"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="a2222-129">Exibe a caixa de diálogo somente se o cartão que está sendo pesquisado pelo aplicativo de chamada não estiver localizado e disponível para uso em um leitor.</span><span class="sxs-lookup"><span data-stu-id="a2222-129">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="a2222-130">Isso permite que o cartão seja encontrado, conectado (por meio de um mecanismo de caixa de diálogo interno ou usando as funções de retorno de chamada do usuário) e retornado ao aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="a2222-130">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="a2222-131"><dt>**SC \_ DLG \_ sem \_ interface do usuário**</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-131"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="a2222-132">Não faz nenhuma exibição da interface do usuário, independentemente do resultado da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a2222-132">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="a2222-133"><dt>**\_IU de \_ força \_ do SC Dlg**</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-133"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="a2222-134">Faz com que a interface do usuário seja exibida, independentemente do resultado da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a2222-134">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="a2222-135">*ppCardInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a2222-135">*ppCardInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2222-136">Ponteiro para um ponteiro para uma estrutura de dados que contém ou retorna informações sobre o [*cartão inteligente*](../secgloss/s-gly.md)aberto, se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a2222-136">Pointer to a pointer to a data structure that contains or returns information about the opened [*smart card*](../secgloss/s-gly.md), if successful.</span></span> <span data-ttu-id="a2222-137">Será **NULL** se a operação falhar.</span><span class="sxs-lookup"><span data-stu-id="a2222-137">Will be **NULL** if operation has failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2222-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2222-138">Return value</span></span>

<span data-ttu-id="a2222-139">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a2222-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a2222-140">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a2222-140">Return code</span></span>                                                                                   | <span data-ttu-id="a2222-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2222-141">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a2222-142"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a2222-143">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a2222-143">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="a2222-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a2222-145">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="a2222-145">Invalid parameter.</span></span><br/>                        |
| <dl> <span data-ttu-id="a2222-146"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a2222-147">Um ponteiro inadequado foi passado em *ppCardInfo*.</span><span class="sxs-lookup"><span data-stu-id="a2222-147">A bad pointer was passed in *ppCardInfo*.</span></span><br/> |
| <dl> <span data-ttu-id="a2222-148"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a2222-149">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="a2222-149">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="a2222-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2222-150">Remarks</span></span>

<span data-ttu-id="a2222-151">Para definir os critérios de pesquisa da pesquisa, chame [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) para especificar os nomes dos cartões do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="a2222-151">To set the search criteria of the search, call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to specify a smart card's card names.</span></span>

<span data-ttu-id="a2222-152">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardLocate**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="a2222-152">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="a2222-153">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a2222-153">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a2222-154">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a2222-154">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2222-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2222-155">Requirements</span></span>



| <span data-ttu-id="a2222-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2222-156">Requirement</span></span> | <span data-ttu-id="a2222-157">Valor</span><span class="sxs-lookup"><span data-stu-id="a2222-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2222-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2222-158">Minimum supported client</span></span><br/> | <span data-ttu-id="a2222-159">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a2222-159">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a2222-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2222-160">Minimum supported server</span></span><br/> | <span data-ttu-id="a2222-161">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2222-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a2222-162">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a2222-162">End of client support</span></span><br/>    | <span data-ttu-id="a2222-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a2222-163">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a2222-164">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a2222-164">End of server support</span></span><br/>    | <span data-ttu-id="a2222-165">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2222-165">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a2222-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2222-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2222-167"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-167"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2222-168">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a2222-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="a2222-169"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-169"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a2222-170">DLL</span><span class="sxs-lookup"><span data-stu-id="a2222-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2222-171"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2222-171"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a2222-172">IID</span><span class="sxs-lookup"><span data-stu-id="a2222-172">IID</span></span><br/>                      | <span data-ttu-id="a2222-173">IID \_ ISCardLocate é definido como 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a2222-173">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="a2222-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2222-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2222-175">**ConfigureCardNameSearch**</span><span class="sxs-lookup"><span data-stu-id="a2222-175">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[<span data-ttu-id="a2222-176">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="a2222-176">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
