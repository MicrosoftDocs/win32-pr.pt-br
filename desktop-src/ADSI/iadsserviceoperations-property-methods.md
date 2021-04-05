---
title: Métodos de propriedade IADsServiceOperations (IADs. h)
description: Os métodos de propriedade da interface IADsServiceOperations lêem e gravam as propriedades descritas na lista a seguir. Para obter mais informações sobre métodos de propriedade, consulte interface Property Methods.
ms.assetid: ebddfc42-1d2f-495b-b57c-f57419b54ff8
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsServiceOperations
topic_type:
- apiref
api_name:
- IADsServiceOperations Property Methods
- IADsServiceOperations.Status
- IADsServiceOperations.get_Status
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 654a92be1052d4e4c70e0274d719a49be965d8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824343"
---
# <a name="iadsserviceoperations-property-methods"></a><span data-ttu-id="12e98-105">Métodos de propriedade IADsServiceOperations</span><span class="sxs-lookup"><span data-stu-id="12e98-105">IADsServiceOperations Property Methods</span></span>

<span data-ttu-id="12e98-106">Os métodos de propriedade da interface [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) lêem e gravam as propriedades descritas na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="12e98-106">The property methods of the [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) interface read and write the properties described in the following list.</span></span> <span data-ttu-id="12e98-107">Para obter mais informações sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="12e98-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="12e98-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12e98-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="12e98-109">**Status**</span><span class="sxs-lookup"><span data-stu-id="12e98-109">**Status**</span></span>
<span data-ttu-id="12e98-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12e98-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="12e98-111">Status do serviço.</span><span class="sxs-lookup"><span data-stu-id="12e98-111">Status of service.</span></span>

<span data-ttu-id="12e98-112">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="12e98-112">The following are possible values.</span></span>

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

<span data-ttu-id="12e98-113">**Anúncios \_ do SERVIÇO \_ interrompido** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="12e98-113">**ADS\_SERVICE\_STOPPED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

<span data-ttu-id="12e98-114">**Anúncios \_ do Início do serviço \_ \_ pendente** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="12e98-114">**ADS\_SERVICE\_START\_PENDING** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

<span data-ttu-id="12e98-115">**Anúncios \_ do Interrupção de serviço \_ \_ pendente** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="12e98-115">**ADS\_SERVICE\_STOP\_PENDING** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

<span data-ttu-id="12e98-116">**Anúncios \_ do SERVIÇO \_ em execução** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="12e98-116">**ADS\_SERVICE\_RUNNING** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

<span data-ttu-id="12e98-117">**Anúncios \_ do Continuação de serviço \_ \_ pendente** (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="12e98-117">**ADS\_SERVICE\_CONTINUE\_PENDING** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

<span data-ttu-id="12e98-118">**Anúncios \_ do Pausa de serviço \_ \_ pendente** (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="12e98-118">**ADS\_SERVICE\_PAUSE\_PENDING** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

<span data-ttu-id="12e98-119">**Anúncios \_ do SERVIÇO em \_ pausa** (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="12e98-119">**ADS\_SERVICE\_PAUSED** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

<span data-ttu-id="12e98-120">**Anúncios \_ do \_Erro de serviço** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="12e98-120">**ADS\_SERVICE\_ERROR** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="12e98-121">**Anúncios \_ do \_ \_ Processo próprio de serviço** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="12e98-121">**ADS\_SERVICE\_OWN\_PROCESS** (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="12e98-122">**Anúncios \_ do \_ \_ Processo de compartilhamento de serviço** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="12e98-122">**ADS\_SERVICE\_SHARE\_PROCESS** (0x00000020)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="12e98-123">**Anúncios \_ do \_ \_ Driver de kernel de serviço** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="12e98-123">**ADS\_SERVICE\_KERNEL\_DRIVER** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="12e98-124">**Anúncios \_ do \_Driver do \_ sistema \_ de arquivos de serviço** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="12e98-124">**ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="12e98-125">**Anúncios \_ do \_ \_ início da inicialização do serviço** (início da inicialização do serviço \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="12e98-125">**ADS\_SERVICE\_BOOT\_START** (SERVICE\_BOOT\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="12e98-126">**Anúncios \_ do \_ \_ início do sistema de serviço** (início do sistema de serviço \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="12e98-126">**ADS\_SERVICE\_SYSTEM\_START** (SERVICE\_SYSTEM\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="12e98-127">**Anúncios \_ do \_ \_ início automático do serviço** ( \_ início automático do serviço \_ )</span><span class="sxs-lookup"><span data-stu-id="12e98-127">**ADS\_SERVICE\_AUTO\_START** (SERVICE\_AUTO\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="12e98-128">**Anúncios \_ do \_ \_ início da demanda de serviço** (início da demanda de serviço \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="12e98-128">**ADS\_SERVICE\_DEMAND\_START** (SERVICE\_DEMAND\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="12e98-129">**Anúncios \_ do SERVIÇO \_ desabilitado** (serviço \_ desabilitado)</span><span class="sxs-lookup"><span data-stu-id="12e98-129">**ADS\_SERVICE\_DISABLED** (SERVICE\_DISABLED)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="12e98-130">**Anúncios \_ do \_ \_ Ignorar erro de serviço** (0)</span><span class="sxs-lookup"><span data-stu-id="12e98-130">**ADS\_SERVICE\_ERROR\_IGNORE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="12e98-131">**Anúncios \_ do Erro de serviço \_ \_ normal** (1)</span><span class="sxs-lookup"><span data-stu-id="12e98-131">**ADS\_SERVICE\_ERROR\_NORMAL** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="12e98-132">**Anúncios \_ do Erro de serviço \_ \_ grave** (2)</span><span class="sxs-lookup"><span data-stu-id="12e98-132">**ADS\_SERVICE\_ERROR\_SEVERE** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="12e98-133">**Anúncios \_ do \_Erro \_ crítico do serviço** (3)</span><span class="sxs-lookup"><span data-stu-id="12e98-133">**ADS\_SERVICE\_ERROR\_CRITICAL** (3)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="12e98-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12e98-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12e98-135">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="12e98-135">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="12e98-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="12e98-136">Examples</span></span>

<span data-ttu-id="12e98-137">O exemplo de código a seguir mostra como verificar o status de um serviço de fax da Microsoft em execução no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="12e98-137">The following code example shows how to verify the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```VB
Dim cp As IADsComputer
Dim sr As IADsService
Dim so As IADsServiceOperations
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
Set sr = cp.GetObject("Service", "Fax")
Set so = sr

Select Case so.Status
    Case ADS_SERVICE_STOPPED
        MsgBox "Microsoft Fax Service has stopped."
    Case ADS_SERVICE_RUNNING
        MsgBox "Microsoft Fax Service is running."
    Case ADS_SERVICE_PAUSED
        MsgBox "Microsoft Fax Service has paused."
    Case ADS_SERVICE_ERROR
        MsgBox "Microsoft Fax Service has errors."
End Select

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
    Set sr = Nothing
    Set so = Nothing
```



<span data-ttu-id="12e98-138">O exemplo de código a seguir verifica o status de um serviço de fax da Microsoft em execução no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="12e98-138">The following code example verifies the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```C++
IADsContainer *pCont = NULL;
IADsServiceOperations *pSrvOp = NULL;
LPWSTR adsPath = L"WinNT://myMachine,computer";
IDispatch *pDisp = NULL;
long status = 0;

HRESULT hr = S_OK;

hr = ADsGetObject(adsPath,IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->GetObject(CComBSTR("Service"), CComBSTR("Fax"), &pDisp);
if(FAILED(hr)) {goto Cleanup;}

hr = pDisp->QueryInterface(IID_IADsServiceOperations,(void**)&pSrvOp);
if(FAILED(hr)) {goto Cleanup;}

hr = pSrvOp->get_Status(&status);
switch (status) 
{
    case ADS_SERVICE_STOPPED:
        printf("The service has stopped.\n");
        break;
    case ADS_SERVICE_RUNNING:
        printf("The service is running.\n");
        break;
    case ADS_SERVICE_PAUSED:
        printf("The service has paused.\n");
        break;
    case ADS_SERVICE_ERROR:
        printf("The service has errors.\n");
        break;
}

Cleanup:
    if(pDisp) pDisp->Release();
    if(pCont) pCont->Release();
    if(pSrvOp) pSrvOp->Release();
```



## <a name="requirements"></a><span data-ttu-id="12e98-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12e98-139">Requirements</span></span>



| <span data-ttu-id="12e98-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="12e98-140">Requirement</span></span> | <span data-ttu-id="12e98-141">Valor</span><span class="sxs-lookup"><span data-stu-id="12e98-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e98-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12e98-142">Minimum supported client</span></span><br/> | <span data-ttu-id="12e98-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12e98-143">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="12e98-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12e98-144">Minimum supported server</span></span><br/> | <span data-ttu-id="12e98-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12e98-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="12e98-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12e98-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="12e98-147"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="12e98-147"><dt>Iads.h</dt></span></span> </dl>        |
| <span data-ttu-id="12e98-148">DLL</span><span class="sxs-lookup"><span data-stu-id="12e98-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12e98-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12e98-149"><dt>Activeds.dll</dt></span></span> </dl>  |
| <span data-ttu-id="12e98-150">IID</span><span class="sxs-lookup"><span data-stu-id="12e98-150">IID</span></span><br/>                      | <span data-ttu-id="12e98-151">IID \_ IADsServiceOperations é definido como 5D7B33F0-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="12e98-151">IID\_IADsServiceOperations is defined as 5D7B33F0-31CA-11CF-A98A-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12e98-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="12e98-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e98-153">**IADsFileService**</span><span class="sxs-lookup"><span data-stu-id="12e98-153">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="12e98-154">**IADsFileServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="12e98-154">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="12e98-155">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="12e98-155">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="12e98-156">**IADsServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="12e98-156">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 





