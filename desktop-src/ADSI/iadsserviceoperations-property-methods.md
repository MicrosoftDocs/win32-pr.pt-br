---
title: Métodos de propriedade IADsServiceOperations (Iads.h)
description: Os métodos de propriedade da interface IADsServiceOperations leem e escrevem as propriedades descritas na lista a seguir. Para obter mais informações sobre métodos de propriedade, consulte Métodos de propriedade de interface.
ms.assetid: ebddfc42-1d2f-495b-b57c-f57419b54ff8
ms.tgt_platform: multiple
keywords:
- Métodos de propriedade IADsServiceOperations ADSI
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
ms.openlocfilehash: c7f60b8fe1280e257ccd33f505b2b696a0d1a16228ebfaf8b0cabf7f1319964a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427602"
---
# <a name="iadsserviceoperations-property-methods"></a>Métodos de propriedade IADsServiceOperations

Os métodos de propriedade da interface [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) leem e escrevem as propriedades descritas na lista a seguir. Para obter mais informações sobre métodos de propriedade, consulte [Métodos de propriedade de interface](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Status**
</dt> <dd> <dl>

Status do serviço.

A seguir estão os valores possíveis.

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

**ADS \_ SERVIÇO \_ PARADO** (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

**ADS \_ INÍCIO \_ DO \_ SERVIÇO PENDENTE** (0X00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

**ADS \_ PARADA \_ DE \_ SERVIÇO PENDENTE** (0X00000003)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

**ADS \_ SERVIÇO \_ EM EXECUÇÃO** (0x00000004)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

**ADS \_ SERVIÇO \_ CONTINUAR \_ PENDENTE** (0x00000005)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

**ADS \_ PAUSA \_ DE \_ SERVIÇO PENDENTE** (0X00000006)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

**ADS \_ SERVIÇO \_ PAUSADO** (0x00000007)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

**ADS \_ ERRO \_ DE** SERVIÇO (0x00000008)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

**ADS \_ PROCESSO \_ PRÓPRIO \_ DE SERVIÇO** (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

**ADS \_ PROCESSO \_ DE \_ COMPARTILHAMENTO DE** SERVIÇO (0x00000020)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

**ADS \_ DRIVER \_ DE KERNEL \_ DE** SERVIÇO (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

**ADS \_ DRIVER \_ DO SISTEMA DE ARQUIVOS \_ \_ DE** SERVIÇO (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

**ADS \_ INICIALIZAÇÃO \_ DO \_ SERVIÇO (INÍCIO** \_ DA INICIALIZAÇÃO DO \_ SERVIÇO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

**ADS \_ INÍCIO \_ DO SISTEMA DE \_ SERVIÇO** (INÍCIO \_ DO SISTEMA DE \_ SERVIÇO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

**ADS \_ INÍCIO \_ AUTOMÁTICO \_ DO SERVIÇO** (INÍCIO AUTOMÁTICO DO \_ \_ SERVIÇO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

**ADS \_ INÍCIO \_ DA DEMANDA DE \_ SERVIÇO** (INÍCIO \_ DA DEMANDA DO \_ SERVIÇO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

**ADS \_ SERVIÇO \_ DESABILITADO** (SERVIÇO \_ DESABILITADO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

**ADS \_ ERRO \_ DE \_ SERVIÇO IGNORAR** (0)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

**ADS \_ ERRO \_ DE \_ SERVIÇO NORMAL** (1)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

**ADS \_ ERRO \_ DE \_ SERVIÇO GRAVE** (2)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

**ADS \_ ERRO \_ DE \_ SERVIÇO CRÍTICO** (3)


</dt> <dd></dd> </dl> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como verificar o status de um Serviço de Fax da Microsoft em execução Windows 2000.


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



O exemplo de código a seguir verifica o status de um Serviço de Fax da Microsoft em execução Windows 2000.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Iads.h</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IADsServiceOperations é definido como 5D7B33F0-31CA-11CF-A98A-00AAA006BC149<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 





