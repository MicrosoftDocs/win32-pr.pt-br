---
title: Classe MDM_HealthAttestation
description: A \_ classe MDM HealthAttestation permite que os gerentes de ti corporativos avaliem a integridade dos dispositivos gerenciados e tomem ações de política corporativa.
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- Classe MDM_HealthAttestation
- Classe MDM_HealthAttestation, descrita
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7f76af135e7eac09b3b104e924b26efbb359b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454921"
---
# <a name="mdm_healthattestation-class"></a>\_Classe HealthAttestation do MDM

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A classe **MDM \_ HealthAttestation** permite que os gerentes de ti corporativos avaliem a integridade dos dispositivos gerenciados e tomem ações de política corporativa.

Veja a seguir uma lista de funções executadas pelo CSP HealthAttestation:

-   Coleta dados que são usados na verificação de Estados de integridade de dispositivos
-   Encaminha os dados para o Serviço de Atestado de Integridade (HAS)
-   Provisiona o certificado de atestado de integridade do qual ele recebe
-   Mediante solicitação, o encaminha o certificado de atestado de integridade (recebido de) e as informações de tempo de execução relacionadas ao servidor MDM para verificação

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

A classe **MDM \_ HealthAttestation** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MDM \_ HealthAttestation** tem esses métodos.



| Método                                                                 | Descrição                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**VerifyHealthMethod**](mdm-healthattestation-verifyhealthmethod.md) | Método para notificar o dispositivo para preparar uma solicitação de verificação de certificado de integridade.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **MDM \_ HealthAttestation** tem essas propriedades.

<dl> <dt>

[Certificado](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **octetstring**
</dt> </dl>

</dd> <dt>

[CorrelationID](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

**CurrentProtocolVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

TBD

</dd> <dt>

[ForceRetrieve](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[HASEndpoint](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
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

Tipo de acesso: leitura/gravação
</dt> </dl>

TBD

</dd> <dt>

[Momentos](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

**ParentID**
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

Tipo de acesso: leitura/gravação
</dt> </dl>

TBD

</dd> <dt>

[Status](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[TpmReadyStatus](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

