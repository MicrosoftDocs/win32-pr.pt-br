---
description: Representa as configurações usadas para testar a conectividade de rede de uma máquina virtual.
ms.assetid: d719d9c9-7ca9-40a0-ada8-185b8cd44c22
title: Msvm_NetworkConnectionDiagnosticSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticSettingData
- Msvm_NetworkConnectionDiagnosticSettingData.IsSender
- Msvm_NetworkConnectionDiagnosticSettingData.SenderIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverMac
- Msvm_NetworkConnectionDiagnosticSettingData.IsolationId
- Msvm_NetworkConnectionDiagnosticSettingData.SequenceNumber
- Msvm_NetworkConnectionDiagnosticSettingData.PayloadSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: da7774e2cf9f36460b1f153d1b498e0c2fa18a19078442ffd5226b9d2dcdb174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521006"
---
# <a name="msvm_networkconnectiondiagnosticsettingdata-class"></a>Classe Msvm \_ NetworkConnectionDiagnosticSettingData

Representa as configurações usadas para testar a conectividade de rede de uma máquina virtual. Usado pelo [**método DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) da [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticSettingData : CIM_SettingData
{
  boolean IsSender;
  string  SenderIP;
  string  ReceiverIP;
  string  ReceiverMac;
  uint32  IsolationId;
  uint32  SequenceNumber;
  uint32  PayloadSize;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ NetworkConnectionDiagnosticSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ NetworkConnectionDiagnosticSettingData** tem essas propriedades.

<dl> <dt>

**IsolationId**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

A ID de isolamento.

</dd> <dt>

**IsSender**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica se esse método está sendo invocado no remetente ou no receptor.

</dd> <dt>

**PayloadSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O tamanho do payload.

</dd> <dt>

**ReceiverIP**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O endereço IP do receptor.

</dd> <dt>

**ReceiverMac**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O endereço MAC do receptor.

</dd> <dt>

**SenderIP**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O endereço IP do remetente.

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O número de sequência.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1703 somente \[ aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração \_ cimData**](cim-settingdata.md)
</dt> </dl>

 

 




