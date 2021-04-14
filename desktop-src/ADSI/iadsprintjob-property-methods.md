---
title: Métodos de propriedade IADsPrintJob (IADs. h)
description: Métodos de propriedade para a interface IADsPrintJob Obtém ou define as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 23e7cbf3-09ce-44ce-b618-2c0fa6b34428
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsPrintJob
topic_type:
- apiref
api_name:
- IADsPrintJob Property Methods
- IADsPrintJob.Description
- IADsPrintJob.get_Description
- IADsPrintJob.put_Description
- IADsPrintJob.HostPrintQueue
- IADsPrintJob.get_HostPrintQueue
- IADsPrintJob.Notify
- IADsPrintJob.get_Notify
- IADsPrintJob.put_Notify
- IADsPrintJob.NotifyPath
- IADsPrintJob.get_NotifyPath
- IADsPrintJob.put_NotifyPath
- IADsPrintJob.Priority
- IADsPrintJob.get_Priority
- IADsPrintJob.put_Priority
- IADsPrintJob.Size
- IADsPrintJob.get_Size
- IADsPrintJob.StartTime
- IADsPrintJob.get_StartTime
- IADsPrintJob.put_StartTime
- IADsPrintJob.TimeSubmitted
- IADsPrintJob.get_TimeSubmitted
- IADsPrintJob.TotalPages
- IADsPrintJob.get_TotalPages
- IADsPrintJob.UntilTime
- IADsPrintJob.get_UntilTime
- IADsPrintJob.User
- IADsPrintJob.get_User
- IADsPrintJob.UserPath
- IADsPrintJob.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1680484ff16d563ef5bc89de6d5abbfec2ce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455614"
---
# <a name="iadsprintjob-property-methods"></a><span data-ttu-id="bc4c2-105">Métodos de propriedade IADsPrintJob</span><span class="sxs-lookup"><span data-stu-id="bc4c2-105">IADsPrintJob Property Methods</span></span>

<span data-ttu-id="bc4c2-106">Métodos de propriedade para a interface [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) Obtém ou define as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-106">Property methods for the [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="bc4c2-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="bc4c2-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="bc4c2-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bc4c2-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="bc4c2-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-109">**Description**</span></span>
<span data-ttu-id="bc4c2-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-111">A descrição do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-111">The description of the print job.</span></span>

<dt>

<span data-ttu-id="bc4c2-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4c2-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc4c2-114">**HostPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-114">**HostPrintQueue**</span></span>
<span data-ttu-id="bc4c2-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-116">A cadeia de caracteres ADsPath da fila de impressão que processa o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-116">The ADsPath string of the Print Queue that processes the print job.</span></span>

<dt>

<span data-ttu-id="bc4c2-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc4c2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostPrintQueue(
  [out] BSTR* pbstrHostPrintQueue
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc4c2-119">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-119">**Notify**</span></span>
<span data-ttu-id="bc4c2-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-121">O usuário a ser notificado quando o trabalho for concluído.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-121">The user to be notified when job is completed.</span></span>

<dt>

<span data-ttu-id="bc4c2-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4c2-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Notify(
  [out] BSTR* pbstrNotify
);
HRESULT put_Notify(
  [in] BSTR bstrNotify
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc4c2-124">**NotifyPath**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-124">**NotifyPath**</span></span>
<span data-ttu-id="bc4c2-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-126">A cadeia de caracteres ADsPath do objeto de usuário a ser notificado quando o trabalho de impressão for concluído.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-126">The ADsPath string of the user object to be notified when the print job is completed.</span></span>

<dt>

<span data-ttu-id="bc4c2-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4c2-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-128">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NotifyPath(
  [out] BSTR* pbstrNotifyPath
);
HRESULT put_NotifyPath(
  [in] BSTR bstrNotifyPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc4c2-129">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-129">**Priority**</span></span>
<span data-ttu-id="bc4c2-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-131">A prioridade do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-131">The priority of the print job.</span></span>

<dt>

<span data-ttu-id="bc4c2-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4c2-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-133">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Priority(
  [out] LONG* plPriority
);
HRESULT put_Priority(
  [in] LONG lPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc4c2-134">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-134">**Size**</span></span>
<span data-ttu-id="bc4c2-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-136">O tamanho, em bytes, do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-136">The size, in bytes, of the print job.</span></span>

<dt>

<span data-ttu-id="bc4c2-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc4c2-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-138">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Size(
  [out] LONG* plSize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc4c2-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-139">**StartTime**</span></span>
<span data-ttu-id="bc4c2-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-141">A hora mais antiga em que o trabalho de impressão deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-141">The earliest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="bc4c2-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4c2-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-143">Tipo de dados de script: **Data**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-143">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartTime(
  [out] DATE* pdateStartTime
);
HRESULT put_StartTime(
  [in] DATE dateStartTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc4c2-144">**Timeenvio**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-144">**TimeSubmitted**</span></span>
<span data-ttu-id="bc4c2-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-146">A hora em que o trabalho foi enviado para a fila.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-146">The time when the job was submitted to the queue.</span></span>

<dt>

<span data-ttu-id="bc4c2-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc4c2-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-148">Tipo de dados de script: **Data**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-148">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeSubmitted(
  [out] DATE* pdateTimeSubmitted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc4c2-149">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-149">**TotalPages**</span></span>
<span data-ttu-id="bc4c2-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-151">O número total de páginas no trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-151">The total number of pages in the print job.</span></span>

<dt>

<span data-ttu-id="bc4c2-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc4c2-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-153">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-153">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TotalPages(
  [out] LONG* plTotalPages
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc4c2-154">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-154">**UntilTime**</span></span>
<span data-ttu-id="bc4c2-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-156">A última hora em que o trabalho de impressão deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-156">The latest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="bc4c2-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4c2-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-158">Tipo de dados de script: **Data**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-158">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc4c2-159">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-159">**User**</span></span>
<span data-ttu-id="bc4c2-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-161">O nome do usuário que enviou o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-161">The name of user who submitted the print job.</span></span>

<dt>

<span data-ttu-id="bc4c2-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc4c2-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-163">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-163">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bc4c2-164">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-164">**UserPath**</span></span>
<span data-ttu-id="bc4c2-165"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bc4c2-165"></dt> <dd> <dl></span></span>

<span data-ttu-id="bc4c2-166">A cadeia de caracteres ADsPath do objeto de usuário que enviou este trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-166">The ADsPath string of the user object that submitted this print job.</span></span>

<dt>

<span data-ttu-id="bc4c2-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc4c2-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc4c2-168">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="bc4c2-169">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc4c2-169">Examples</span></span>

<span data-ttu-id="bc4c2-170">O exemplo de código a seguir mostra como trabalhar com propriedades de um objeto de trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-170">The following code example shows how to work with properties of a print job object.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pj As IADsPrintJob
On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    MsgBox "Host Printer: " & pj.HostPrintQueue
    MsgBox "Job description: " & pj.Description
    MsgBox "job requester: " & pj.User 
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pj = Nothing
```



<span data-ttu-id="bc4c2-171">O exemplo de código a seguir mostra como trabalhar com propriedades de um objeto de trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="bc4c2-171">The following code example shows how to work with properties of a print job object.</span></span>


```C++
IADsPrintQueueOperations *pqo = NULL;
IADsPrintJob *pJob = NULL;
HRESULT hr = S_OK;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
LPWSTR adsPath =L"WinNT://aMachine/aPrinter";

VariantInit(&var);

hr = ADsGetObject(adsPath, 
                  IID_IADsPrintQueueOperations, 
                  (void**)&pqo);
if(FAILED(hr)){goto Cleanup;}


hr = pqo->PrintJobs(&pColl);

// Enumerate print jobs. Code omitted.

hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)){goto Cleanup;}


IEnumVARIANT *pEnum;
hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)){goto Cleanup;}


// Now Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
if(FAILED(hr)){goto Cleanup;}

while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsPrintJob, (void**)&pJob);

        pJob->get_HostPrintQueue(&bstr);
        printf("HostPrintQueue: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_Description(&bstr);
        printf("Print job name: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_User(&bstr);
        printf("Requester: %S\n",bstr);
        SysFreeString(bstr);

        pJob->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="bc4c2-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc4c2-172">Requirements</span></span>



| <span data-ttu-id="bc4c2-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc4c2-173">Requirement</span></span> | <span data-ttu-id="bc4c2-174">Valor</span><span class="sxs-lookup"><span data-stu-id="bc4c2-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc4c2-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc4c2-175">Minimum supported client</span></span><br/> | <span data-ttu-id="bc4c2-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc4c2-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc4c2-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc4c2-177">Minimum supported server</span></span><br/> | <span data-ttu-id="bc4c2-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc4c2-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc4c2-179">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc4c2-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc4c2-180"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c2-180"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="bc4c2-181">DLL</span><span class="sxs-lookup"><span data-stu-id="bc4c2-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc4c2-182"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c2-182"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc4c2-183">IID</span><span class="sxs-lookup"><span data-stu-id="bc4c2-183">IID</span></span><br/>                      | <span data-ttu-id="bc4c2-184">IID \_ IADsPrintJob é definido como 32FB6780-1ED0-11CF-A988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="bc4c2-184">IID\_IADsPrintJob is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="bc4c2-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc4c2-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc4c2-186">**IADsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="bc4c2-186">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="bc4c2-187">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="bc4c2-187">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





