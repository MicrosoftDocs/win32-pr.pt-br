---
title: Métodos de propriedade IADsSession (IADs. h)
description: Os métodos de propriedade da interface IADsSession obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações e uma discussão geral sobre métodos de propriedade, consulte interface Property Methods.
ms.assetid: b2366da7-c51c-4279-8931-2000d3110d72
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsSession
topic_type:
- apiref
api_name:
- IADsSession Property Methods
- IADsSession.Computer
- IADsSession.get_Computer
- IADsSession.ComputerPath
- IADsSession.get_ComputerPath
- IADsSession.ConnectTime
- IADsSession.get_ConnectTime
- IADsSession.IdleTime
- IADsSession.get_IdleTime
- IADsSession.User
- IADsSession.get_User
- IADsSession.UserPath
- IADsSession.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf7dd9abe25d731ba63385cd8d632c4212ea349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824342"
---
# <a name="iadssession-property-methods"></a><span data-ttu-id="54fac-105">Métodos de propriedade IADsSession</span><span class="sxs-lookup"><span data-stu-id="54fac-105">IADsSession Property Methods</span></span>

<span data-ttu-id="54fac-106">Os métodos de propriedade da interface [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="54fac-106">The property methods of the [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="54fac-107">Para obter mais informações e uma discussão geral sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="54fac-107">For more information and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="54fac-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="54fac-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="54fac-109">**Computador**</span><span class="sxs-lookup"><span data-stu-id="54fac-109">**Computer**</span></span>
<span data-ttu-id="54fac-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="54fac-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="54fac-111">Nome da estação de trabalho cliente.</span><span class="sxs-lookup"><span data-stu-id="54fac-111">Name of the client workstation.</span></span>

<dt>

<span data-ttu-id="54fac-112">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54fac-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54fac-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="54fac-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Computer(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="54fac-114">**ComputerPath**</span><span class="sxs-lookup"><span data-stu-id="54fac-114">**ComputerPath**</span></span>
<span data-ttu-id="54fac-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="54fac-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="54fac-116">ADsPath do objeto de computador para a estação de trabalho cliente.</span><span class="sxs-lookup"><span data-stu-id="54fac-116">ADsPath of the computer object for the client workstation.</span></span>

<dt>

<span data-ttu-id="54fac-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54fac-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54fac-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="54fac-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerPath(
  [out] BSTR* pbstrComputerPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="54fac-119">**Connecttime**</span><span class="sxs-lookup"><span data-stu-id="54fac-119">**ConnectTime**</span></span>
<span data-ttu-id="54fac-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="54fac-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="54fac-121">Tempo decorrido, em segundos, desde que a sessão foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="54fac-121">Elapsed time, in seconds, since the session started.</span></span>

<dt>

<span data-ttu-id="54fac-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54fac-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54fac-123">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="54fac-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ConnectTime(
  [out] LONG* plConnectTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="54fac-124">**Tempo ocioso**</span><span class="sxs-lookup"><span data-stu-id="54fac-124">**IdleTime**</span></span>
<span data-ttu-id="54fac-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="54fac-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="54fac-126">Tempo ocioso, em segundos, da sessão.</span><span class="sxs-lookup"><span data-stu-id="54fac-126">Idle time, in seconds, of the session.</span></span>

<dt>

<span data-ttu-id="54fac-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54fac-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54fac-128">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="54fac-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IdleTime(
  [out] LONG* plIdleTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="54fac-129">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="54fac-129">**User**</span></span>
<span data-ttu-id="54fac-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="54fac-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="54fac-131">O nome do usuário da sessão.</span><span class="sxs-lookup"><span data-stu-id="54fac-131">The name of the user of the session.</span></span>

<dt>

<span data-ttu-id="54fac-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54fac-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54fac-133">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="54fac-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="54fac-134">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="54fac-134">**UserPath**</span></span>
<span data-ttu-id="54fac-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="54fac-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="54fac-136">O ADsPath do objeto de usuário para o usuário desta sessão.</span><span class="sxs-lookup"><span data-stu-id="54fac-136">The ADsPath of the user object for the user of this session.</span></span>

<dt>

<span data-ttu-id="54fac-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54fac-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54fac-138">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="54fac-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="54fac-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="54fac-139">Examples</span></span>

<span data-ttu-id="54fac-140">O exemplo de código a seguir mostra como examinar sessões para um serviço de arquivo.</span><span class="sxs-lookup"><span data-stu-id="54fac-140">The following code example shows how to examine sessions for a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
On Error GoTo Cleanup

' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate sessions.
If (IsEmpty(fso) = False) Then
    For Each session In fso.sessions
        MsgBox "Session Computer: " & session.Computer
        MsgBox "Session User: " & session.User
    Next Session
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="54fac-141">O exemplo de código a seguir enumera uma coleção de sessões.</span><span class="sxs-lookup"><span data-stu-id="54fac-141">The following code example enumerates a collection of sessions.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsSession *pSes = NULL;
IADsCollection *pColl = NULL;
HRESULT hr = S_OK;
IUnknown *pUnk = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IEnumVARIANT *pEnum = NULL;

VariantInit(&var);

LPWSTR adsPath = L"WinNT://aMachine/LanmanServer";

hr = ADsGetObject(adsPath,IID_IADsFileServiceOperations,
                  (void**)&pFso);

if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Sessions(&pColl);

// Enumerate sessions. 
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsSession, (void**)&pSes);
        pSes->get_Computer(&bstr);
        printf("Session host: %S\n",bstr);
        SysFreeString(bstr);

        pSes->get_User(&bstr);
        printf("Session user: %S\n",bstr);
        SysFreeString(bstr);

        pRes->Release();
    }

    VariantClear(&var);
    pDisp=NULL;
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pFso) pFso->Release();
    if(pColl) pColl->Release();
    if(pUnk) pUnk->Release();
    if(pEnum) pEnum->Release();
```



## <a name="requirements"></a><span data-ttu-id="54fac-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54fac-142">Requirements</span></span>



| <span data-ttu-id="54fac-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="54fac-143">Requirement</span></span> | <span data-ttu-id="54fac-144">Valor</span><span class="sxs-lookup"><span data-stu-id="54fac-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54fac-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54fac-145">Minimum supported client</span></span><br/> | <span data-ttu-id="54fac-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54fac-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54fac-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54fac-147">Minimum supported server</span></span><br/> | <span data-ttu-id="54fac-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54fac-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54fac-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54fac-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="54fac-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="54fac-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="54fac-151">DLL</span><span class="sxs-lookup"><span data-stu-id="54fac-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54fac-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54fac-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="54fac-153">IID</span><span class="sxs-lookup"><span data-stu-id="54fac-153">IID</span></span><br/>                      | <span data-ttu-id="54fac-154">IID \_ IADsSession é definido como 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="54fac-154">IID\_IADsSession is defined as 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="54fac-155">Consulte também</span><span class="sxs-lookup"><span data-stu-id="54fac-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54fac-156">**IADsFileServiceOperations:: sessões**</span><span class="sxs-lookup"><span data-stu-id="54fac-156">**IADsFileServiceOperations::Sessions**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-sessions)
</dt> <dt>

[<span data-ttu-id="54fac-157">**IADsSession**</span><span class="sxs-lookup"><span data-stu-id="54fac-157">**IADsSession**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssession)
</dt> </dl>

 

 





