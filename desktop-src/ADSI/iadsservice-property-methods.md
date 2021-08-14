---
title: Métodos de propriedade IADsService (IADs. h)
description: Leia e grave as propriedades descritas neste tópico.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsService
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babbd7605b990776141d158d455e9df2aeb9864d7619158e16bab7e113f84d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690975"
---
# <a name="iadsservice-property-methods"></a>Métodos de propriedade IADsService

Os métodos de propriedade da interface [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) lêem e gravam as propriedades descritas neste tópico. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Dependências**
</dt> <dd> <dl>

Matriz de nomes **BSTR** de serviços ou grupos de carregamento que devem ser carregados para que esse serviço seja carregado. A sintaxe da entrada é "serviço:" seguida do nome do serviço ou "Grupo:" seguido pelo nome do grupo de carregamento.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

**DisplayName**
</dt> <dd> <dl>

O nome amigável do serviço.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

**ErrorControl**
</dt> <dd> <dl>

A ação a ser executada se esse serviço falhar na inicialização. Veja a seguir os valores válidos para essa propriedade.

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>erro de serviço do ADS \_ \_ \_ ignorar * * * *


</dt> <dd>

O programa de inicialização registra o erro, mas continua a operação de inicialização.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\_erro de serviço ADS \_ \_ normal * * * *


</dt> <dd>

O programa de inicialização registra o erro e apresenta uma caixa de mensagem, mas continua a operação de inicialização.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\_erro de serviço ADS \_ \_ grave * * * *


</dt> <dd>

O programa de inicialização registra o erro. Se a última configuração válida for iniciada, a operação de inicialização continuará. Caso contrário, o sistema será reiniciado com a última configuração válida.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\_erro crítico do serviço ADS \_ \_ * * * *


</dt> <dd>

O programa de inicialização registra o erro, se possível. Se a última configuração válida estiver sendo iniciada, a operação de inicialização falhará. Caso contrário, o sistema será reiniciado com a última configuração válida conhecida.

</dd> </dl> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

**HostComputer**
</dt> <dd> <dl>

A cadeia de caracteres ADsPath do host deste serviço.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
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

**LoadOrderGroup**
</dt> <dd> <dl>

Nome do grupo de ordem de carregamento do qual este serviço é membro.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

**Caminho**
</dt> <dd> <dl>

Caminho e nome de arquivo para o executável deste serviço.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
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


</dt> </dl> </dd> <dt>

**ServiceAccountName**
</dt> <dd> <dl>

Nome da conta que esse serviço usa para se autenticar na inicialização.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

**ServiceAccountPath**
</dt> <dd> <dl>

Caminho da conta especificada pela propriedade **ServiceAccountPath** .

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

**ServiceType**
</dt> <dd> <dl>

A descrição de como um serviço se apresenta no computador host. Essa propriedade pode ser zero ou uma combinação de um ou mais dos valores a seguir.

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

Driver de kernel de serviço do ADS * * * * \_ \_ \_ (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

Driver do sistema de arquivos do serviço ADS * * * * \_ \_ \_ \_ (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

Processo próprio de serviço do ADS * * * * \_ \_ \_ (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

\_Processo de \_ compartilhamento do serviço ADS \_ * * * * (0x00000020)


</dt> <dd></dd> </dl> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

**StartType**
</dt> <dd> <dl>

Determina como iniciar o serviço. Veja a seguir os valores válidos para essa propriedade.

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\_início da inicialização do serviço ADS \_ \_ * * * *


</dt> <dd>

O serviço é um driver de dispositivo iniciado pelo carregador do sistema. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\_início do sistema de serviço ADS \_ \_ * * * *


</dt> <dd>

O serviço é um driver de dispositivo iniciado pela função **IoInitSystem** . Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\_início automático do serviço ADS * * * \_ \_ *


</dt> <dd>

O serviço será iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\_início da demanda de serviço ADS \_ \_ * * * *


</dt> <dd>

O serviço será iniciado pelo Gerenciador de controle de serviço quando um processo chamar a função [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) .

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\_serviço ADS \_ desabilitado * * * *


</dt> <dd>

Não é possível iniciar o serviço. As tentativas de iniciar o serviço resultam no código de erro **serviço de erro \_ \_ desabilitado**.

</dd> </dl> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

**StartupParameters**
</dt> <dd> <dl>

Parâmetros passados para o serviço na inicialização.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

**Versão**
</dt> <dd> <dl>

Versão do serviço.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como listar todos os serviços do sistema disponíveis em execução no computador host, "mymachine", junto com o local para encontrar os executáveis dos serviços.


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsService é definido como 68AF66E0-31CA-11CF-A98A-00AA006BC149<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[Métodos de propriedade de interface](interface-property-methods.md)
</dt> </dl>

 

