---
title: MDM_HealthAttestation classe
description: A classe MDM HealthAttestation permite que os gerentes de IT empresariais avaliem a saúde dos \_ dispositivos gerenciados e tomeem medidas de política corporativa.
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- MDM_HealthAttestation classe
- MDM_HealthAttestation, descrita
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81d1ebf7e4df529c54dc3af125e87569ea0d300f8bb6de3a42e5b670dc43cdd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118165809"
---
# <a name="mdm_healthattestation-class"></a>Classe MDM \_ HealthAttestation

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A **classe MDM \_ HealthAttestation** permite que os gerentes de IT empresariais avaliem a saúde dos dispositivos gerenciados e tomeem medidas de política corporativa.

Veja a seguir uma lista de funções executadas pelo CSP healthAttestation:

-   Coleta dados usados para verificar os estados de saúde de um dispositivo
-   Encaminha os dados para o Serviço de Atestado de Integridade (HAS)
-   Provisiona o certificado de atestado de saúde que ele recebe do HAS
-   Mediante solicitação, encaminha o Certificado de Atestado de Saúde (recebido de HAS) e as informações de runtime relacionadas ao Servidor MDM para verificação

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_HealthAttestation
{
  string  InstanceID;
  string  ParentID;
  sint32  Status;
  boolean ForceRetrieve;
  string  Certificate;
  string  Nonce;
  string  CorrelationID;
  sint32  TpmReadyStatus;
  sint32  MaxSupportedProtocolVersion;
  sint32  PreferredMaxProtocolVersion;
  sint32  CurrentProtocolVersion;
  string  HASEndpoint;
};
```

## <a name="members"></a>Membros

A **classe MDM \_ HealthAttestation** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe MDM \_ HealthAttestation** tem esses métodos.



| Método                                                                 | Descrição                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**VerifyHealthMethod**](mdm-healthattestation-verifyhealthmethod.md) | Método para notificar o dispositivo para preparar uma solicitação de verificação de certificado de saúde.<br/> |



 

### <a name="properties"></a>Propriedades

A **classe MDM \_ HealthAttestation** tem essas propriedades.

<dl> <dt>

[Certificado](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **Octetstring**
</dt> </dl>

</dd> <dt>

[Correlationid](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

**CurrentProtocolVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

TBD

</dd> <dt>

[ForceRetrieve](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

[HASEndpoint](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica o nome do nó pai. Para essa classe, a cadeia de caracteres é "HealthAttestation".

</dd> <dt>

**MaxSupportedProtocolVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

TBD

</dd> <dt>

[Nonce](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"

</dd> <dt>

**PreferredMaxProtocolVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

TBD

</dd> <dt>

[Status](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

[TpmReadyStatus](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Cimv2 \\ mdm \\ dmmap raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

