---
title: Métodos de propriedade IADsFileShare (IADs. h)
description: Os métodos de propriedade da interface IADsFileshare obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: c5a81c42-507f-4a68-b6f4-83097bd0fa01
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsFileShare
topic_type:
- apiref
api_name:
- IADsFileShare Property Methods
- IADsFileShare.CurrentUserCount
- IADsFileShare.get_CurrentUserCount
- IADsFileShare.Description
- IADsFileShare.get_Description
- IADsFileShare.put_Description
- IADsFileShare.HostComputer
- IADsFileShare.get_HostComputer
- IADsFileShare.put_HostComputer
- IADsFileShare.MaxUserCount
- IADsFileShare.get_MaxUserCount
- IADsFileShare.Path
- IADsFileShare.get_Path
- IADsFileShare.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38369a4054f1848d5e35ff8bdb2dda9e9423a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086042"
---
# <a name="iadsfileshare-property-methods"></a><span data-ttu-id="0895f-105">Métodos de propriedade IADsFileShare</span><span class="sxs-lookup"><span data-stu-id="0895f-105">IADsFileShare Property Methods</span></span>

<span data-ttu-id="0895f-106">Os métodos de propriedade da interface [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0895f-106">The property methods of the [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="0895f-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="0895f-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="0895f-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0895f-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="0895f-109">**CurrentUserCount**</span><span class="sxs-lookup"><span data-stu-id="0895f-109">**CurrentUserCount**</span></span>
<span data-ttu-id="0895f-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0895f-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="0895f-111">O número de usuários conectados ao compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="0895f-111">The number of users connected to the share.</span></span>

<dt>

<span data-ttu-id="0895f-112">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0895f-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0895f-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="0895f-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CurrentUserCount(
  [out] LONG* plCurrentUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0895f-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0895f-114">**Description**</span></span>
<span data-ttu-id="0895f-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0895f-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="0895f-116">A descrição do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="0895f-116">The description of the file share.</span></span>

<dt>

<span data-ttu-id="0895f-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0895f-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0895f-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0895f-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="0895f-119">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="0895f-119">**HostComputer**</span></span>
<span data-ttu-id="0895f-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0895f-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="0895f-121">Uma referência de ADsPath para o computador host.</span><span class="sxs-lookup"><span data-stu-id="0895f-121">An ADsPath reference to the host computer.</span></span>

<dt>

<span data-ttu-id="0895f-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0895f-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0895f-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0895f-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0895f-124">**MaxUserCount**</span><span class="sxs-lookup"><span data-stu-id="0895f-124">**MaxUserCount**</span></span>
<span data-ttu-id="0895f-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0895f-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="0895f-126">O número máximo de usuários com permissão para acessar o compartilhamento ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="0895f-126">The maximum number of users allowed to access the share at one time.</span></span>

<dt>

<span data-ttu-id="0895f-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0895f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0895f-128">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="0895f-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0895f-129">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="0895f-129">**Path**</span></span>
<span data-ttu-id="0895f-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0895f-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="0895f-131">O caminho do sistema de arquivos para o diretório compartilhado.</span><span class="sxs-lookup"><span data-stu-id="0895f-131">The file system path to the shared directory.</span></span>

<dt>

<span data-ttu-id="0895f-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0895f-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0895f-133">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0895f-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="0895f-134">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0895f-134">Examples</span></span>

<span data-ttu-id="0895f-135">Para acessar as propriedades de compartilhamentos de arquivos em um computador, você deve primeiro ligar a "LanmanServer" no computador.</span><span class="sxs-lookup"><span data-stu-id="0895f-135">To access the properties of file shares on a computer, you must first bind to the "LanmanServer" on the machine.</span></span> <span data-ttu-id="0895f-136">O exemplo de código a seguir mostra como configurar a descrição e o número máximo de usuários permitidos para todos os compartilhamentos de arquivos públicos no computador, nomeados como "mymachine", no domínio padrão.</span><span class="sxs-lookup"><span data-stu-id="0895f-136">The following code example shows how to set up the description and the maximum number of allowed users for all the public file shares on the computer, named as "myMachine", in the default domain.</span></span>


```VB
Dim fs As IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://myMachine/LanmanServer")
If (fs.class = "FileService") Then
    For Each share In fs
        share.description = share.name & " is my working folder."
        share.MaxUserCount =  10
        share.SetInfo
    Next share
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
```



<span data-ttu-id="0895f-137">O exemplo de código a seguir mostra como tornar o diretório C: \\ MyFolder existente um compartilhamento de arquivo público.</span><span class="sxs-lookup"><span data-stu-id="0895f-137">The following code example shows how to make the existing C:\\MyFolder directory a public file share.</span></span>


```VB
Dim fs As IADsFileShare
Dim cont As IADsContainer
On Error GoTo Cleanup
 
Set cont = GetObject("WinNT://yourDomain/yourMachineName/LanmanServer")
 
Set fs = cont.Create("FileShare", "Public")
Debug.Print fs.Class
fs.Path = "C:\MyFolder"
fs.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set fs = Nothing
```



<span data-ttu-id="0895f-138">O exemplo de código a seguir torna o diretório C: \\ MyFolder existente um compartilhamento de arquivo público.</span><span class="sxs-lookup"><span data-stu-id="0895f-138">The following code example makes the existing C:\\MyFolder directory a public file share.</span></span>


```C++
IADsFileShare *pShare = NULL;
IADsContainer *pCont = NULL;
LPWSTR adsPath = L"WinNT://yourMachineName/LanmanServer";
HRESULT hr = S_OK;

hr = ADsGetObject(adsPath, IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->Create(CComBSTR("FileShare"), CComBSTR("Public"), (IDispatch**)&pShare);

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->put_Path(CComBSTR("c:\\public"));

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->SetInfo();

Cleanup:
    if(pCont) pCont->Release();
    if(pShare) pShare->Release();
```



## <a name="requirements"></a><span data-ttu-id="0895f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0895f-139">Requirements</span></span>



| <span data-ttu-id="0895f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0895f-140">Requirement</span></span> | <span data-ttu-id="0895f-141">Valor</span><span class="sxs-lookup"><span data-stu-id="0895f-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0895f-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0895f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0895f-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0895f-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0895f-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0895f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0895f-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0895f-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0895f-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0895f-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="0895f-147"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="0895f-147"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="0895f-148">DLL</span><span class="sxs-lookup"><span data-stu-id="0895f-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0895f-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0895f-149"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="0895f-150">IID</span><span class="sxs-lookup"><span data-stu-id="0895f-150">IID</span></span><br/>                      | <span data-ttu-id="0895f-151">IID \_ IADsFileShare é definido como EB6DCAF0-4B83-11CF-A995-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="0895f-151">IID\_IADsFileShare is defined as EB6DCAF0-4B83-11CF-A995-00AA006BC149</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="0895f-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="0895f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0895f-153">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="0895f-153">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="0895f-154">**IADsFileShare**</span><span class="sxs-lookup"><span data-stu-id="0895f-154">**IADsFileShare**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileshare)
</dt> <dt>

[<span data-ttu-id="0895f-155">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="0895f-155">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





