---
description: Verifica se a replicação pode ser habilitada do sistema de host atual para o sistema de recuperação especificado.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Método TestReplicationConnection da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768498"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a>Método TestReplicationConnection da \_ classe ReplicationService Msvm

Verifica se a replicação pode ser habilitada do sistema de host atual para o sistema de recuperação especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RecoveryConnectionPoint* \[ no\]
</dt> <dd>

O nome do ponto de conexão. Para um cluster de recuperação, esse é o nome da extremidade do agente. Para um servidor de recuperação autônomo, esse é o nome do sistema do host.

</dd> <dt>

*RecoveryServerPortNumber* \[ no\]
</dt> <dd>

O número da porta do ponto de conexão de recuperação.

</dd> <dt>

*AuthenticationType* \[ no\]
</dt> <dd>

O esquema de autenticação de recuperação. Deve ser um dos valores a seguir.

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Autenticação integrada** (1)


</dt> <dd>

Autenticação Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticação baseada em certificado** (2)


</dt> <dd>

Autenticação baseada em certificado.

</dd> </dl> </dd> <dt>

*CertificateThumbPrint* \[ no\]
</dt> <dd>

Impressão digital do certificado a ser usada quando o parâmetro *AuthenticationType* for autenticação baseada em certificado.

</dd> <dt>

*BypassProxyServer* \[ no\]
</dt> <dd>

Ignore o servidor proxy ao se conectar ao servidor de réplica.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

O **status é desconhecido** (32771)
</dt> <dt>

**Tempo limite** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

O **sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

O **sistema não está disponível** (32777)
</dt> <dt>

**Memória insuficiente** (32778)
</dt> <dt>

**Arquivo não encontrado** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

