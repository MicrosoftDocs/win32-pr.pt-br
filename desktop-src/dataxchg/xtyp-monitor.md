---
title: Transação de XTYP_MONITOR (ddeml. h)
description: Uma função de retorno de chamada DDE do depurador troca dinâmica de dados (DDE), DdeCallback, recebe a \_ transação do monitor XTYP sempre que um evento DDE ocorre no sistema.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- Troca de dados de transação XTYP_MONITOR
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369504"
---
# <a name="xtyp_monitor-transaction"></a><span data-ttu-id="c35ef-104">Transação do monitor de XTYP \_</span><span class="sxs-lookup"><span data-stu-id="c35ef-104">XTYP\_MONITOR transaction</span></span>

<span data-ttu-id="c35ef-105">Uma função de retorno de chamada DDE do depurador troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação do **\_ Monitor XTYP** sempre que um evento DDE ocorre no sistema.</span><span class="sxs-lookup"><span data-stu-id="c35ef-105">A Dynamic Data Exchange (DDE) debugger's DDE callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_MONITOR** transaction whenever a DDE event occurs in the system.</span></span> <span data-ttu-id="c35ef-106">Para receber essa transação, um aplicativo deve especificar o valor do **\_ Monitor APPCLASS** ao chamar a função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="c35ef-106">To receive this transaction, an application must specify the **APPCLASS\_MONITOR** value when it calls the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="c35ef-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c35ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c35ef-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="c35ef-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="c35ef-109">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="c35ef-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="c35ef-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="c35ef-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="c35ef-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c35ef-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c35ef-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="c35ef-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="c35ef-113">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c35ef-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c35ef-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="c35ef-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="c35ef-115">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c35ef-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c35ef-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="c35ef-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="c35ef-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c35ef-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c35ef-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="c35ef-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="c35ef-119">Um identificador para um objeto DDE que contém informações sobre o evento DDE.</span><span class="sxs-lookup"><span data-stu-id="c35ef-119">A handle to a DDE object that contains information about the DDE event.</span></span> <span data-ttu-id="c35ef-120">O aplicativo deve usar a função [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) para obter um ponteiro para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c35ef-120">The application should use the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function to obtain a pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="c35ef-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="c35ef-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="c35ef-122">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c35ef-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c35ef-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="c35ef-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="c35ef-124">O evento DDE.</span><span class="sxs-lookup"><span data-stu-id="c35ef-124">The DDE event.</span></span> <span data-ttu-id="c35ef-125">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c35ef-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c35ef-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c35ef-126">Value</span></span>                                                                                                                                                                                                                      | <span data-ttu-id="c35ef-127">Significado</span><span class="sxs-lookup"><span data-stu-id="c35ef-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <span data-ttu-id="c35ef-128"><dt>**MF \_ RETORNOs de chamada**</dt> <dt>0x08000000</dt></span><span class="sxs-lookup"><span data-stu-id="c35ef-128"><dt>**MF\_CALLBACKS**</dt> <dt>0x08000000</dt></span></span> </dl> | <span data-ttu-id="c35ef-129">O sistema enviou uma transação para uma função de retorno de chamada DDE.</span><span class="sxs-lookup"><span data-stu-id="c35ef-129">The system sent a transaction to a DDE callback function.</span></span> <span data-ttu-id="c35ef-130">O objeto DDE contém uma estrutura [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) que fornece informações sobre a transação.</span><span class="sxs-lookup"><span data-stu-id="c35ef-130">The DDE object contains a [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) structure that provides information about the transaction.</span></span><br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <span data-ttu-id="c35ef-131"><dt>**MF \_ CONV**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="c35ef-131"><dt>**MF\_CONV**</dt> <dt>0x40000000</dt></span></span> </dl>                | <span data-ttu-id="c35ef-132">Uma conversa DDE foi estabelecida ou terminada.</span><span class="sxs-lookup"><span data-stu-id="c35ef-132">A DDE conversation was established or terminated.</span></span> <span data-ttu-id="c35ef-133">O objeto DDE contém uma estrutura [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) que fornece informações sobre a conversa.</span><span class="sxs-lookup"><span data-stu-id="c35ef-133">The DDE object contains a [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) structure that provides information about the conversation.</span></span><br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <span data-ttu-id="c35ef-134"><dt>**MF \_ ERROS**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="c35ef-134"><dt>**MF\_ERRORS**</dt> <dt>0x10000000</dt></span></span> </dl>          | <span data-ttu-id="c35ef-135">Ocorreu um erro de DDE.</span><span class="sxs-lookup"><span data-stu-id="c35ef-135">A DDE error occurred.</span></span> <span data-ttu-id="c35ef-136">O objeto DDE contém uma estrutura [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) que fornece informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="c35ef-136">The DDE object contains a [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) structure that provides information about the error.</span></span><br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <span data-ttu-id="c35ef-137"><dt>**MF \_ HSZ \_ info**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="c35ef-137"><dt>**MF\_HSZ\_INFO**</dt> <dt>0x01000000</dt></span></span> </dl>   | <span data-ttu-id="c35ef-138">Um aplicativo DDE criado, liberado ou incrementado a contagem de uso de um identificador de cadeia de caracteres, ou um identificador de cadeia de caracteres foi liberado como resultado de uma chamada para a função [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="c35ef-138">A DDE application created, freed, or incremented the usage count of a string handle, or a string handle was freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> <span data-ttu-id="c35ef-139">O objeto DDE contém uma estrutura [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) que fornece informações sobre o identificador da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c35ef-139">The DDE object contains a [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure that provides information about the string handle.</span></span><br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <span data-ttu-id="c35ef-140"><dt>**MF \_**</dt> <dt>0X20000000</dt> de links</span><span class="sxs-lookup"><span data-stu-id="c35ef-140"><dt>**MF\_LINKS**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="c35ef-141">Um aplicativo DDE iniciou ou interrompeu um loop de aviso.</span><span class="sxs-lookup"><span data-stu-id="c35ef-141">A DDE application started or stopped an advise loop.</span></span> <span data-ttu-id="c35ef-142">O objeto DDE contém uma estrutura [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) que fornece informações sobre o loop de aviso.</span><span class="sxs-lookup"><span data-stu-id="c35ef-142">The DDE object contains a [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) structure that provides information about the advise loop.</span></span><br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <span data-ttu-id="c35ef-143"><dt>**MF \_**</dt> <dt>0X04000000</dt> de mensagens</span><span class="sxs-lookup"><span data-stu-id="c35ef-143"><dt>**MF\_POSTMSGS**</dt> <dt>0x04000000</dt></span></span> </dl>    | <span data-ttu-id="c35ef-144">O sistema ou um aplicativo postou uma mensagem DDE.</span><span class="sxs-lookup"><span data-stu-id="c35ef-144">The system or an application posted a DDE message.</span></span> <span data-ttu-id="c35ef-145">O objeto DDE contém uma estrutura [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) que fornece informações sobre a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c35ef-145">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <span data-ttu-id="c35ef-146"><dt>**MF \_ SENDMSGS**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="c35ef-146"><dt>**MF\_SENDMSGS**</dt> <dt>0x02000000</dt></span></span> </dl>    | <span data-ttu-id="c35ef-147">O sistema ou um aplicativo enviou uma mensagem DDE.</span><span class="sxs-lookup"><span data-stu-id="c35ef-147">The system or an application sent a DDE message.</span></span> <span data-ttu-id="c35ef-148">O objeto DDE contém uma estrutura [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) que fornece informações sobre a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c35ef-148">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c35ef-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c35ef-149">Return value</span></span>

<span data-ttu-id="c35ef-150">Se a função de retorno de chamada processar essa transação, ela deverá retornar 0.</span><span class="sxs-lookup"><span data-stu-id="c35ef-150">If the callback function processes this transaction, it should return 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="c35ef-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c35ef-151">Requirements</span></span>



| <span data-ttu-id="c35ef-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="c35ef-152">Requirement</span></span> | <span data-ttu-id="c35ef-153">Valor</span><span class="sxs-lookup"><span data-stu-id="c35ef-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c35ef-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c35ef-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c35ef-155">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c35ef-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c35ef-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c35ef-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c35ef-157">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c35ef-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c35ef-158">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c35ef-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="c35ef-159"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c35ef-159"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c35ef-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="c35ef-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="c35ef-161">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c35ef-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c35ef-162">**DdeAccessData**</span><span class="sxs-lookup"><span data-stu-id="c35ef-162">**DdeAccessData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[<span data-ttu-id="c35ef-163">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="c35ef-163">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="c35ef-164">**DdeUninitialize**</span><span class="sxs-lookup"><span data-stu-id="c35ef-164">**DdeUninitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[<span data-ttu-id="c35ef-165">**MONCBSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c35ef-165">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[<span data-ttu-id="c35ef-166">**MONCONVSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c35ef-166">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[<span data-ttu-id="c35ef-167">**MONERRSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c35ef-167">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[<span data-ttu-id="c35ef-168">**MONHSZSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c35ef-168">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[<span data-ttu-id="c35ef-169">**MONLINKSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c35ef-169">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[<span data-ttu-id="c35ef-170">**MONMSGSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c35ef-170">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

<span data-ttu-id="c35ef-171">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c35ef-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c35ef-172">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="c35ef-172">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

