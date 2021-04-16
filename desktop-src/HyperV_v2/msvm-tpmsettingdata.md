---
description: Representa o estado configurado do dispositivo TPM.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Classe Msvm_TPMSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502194"
---
# <a name="msvm_tpmsettingdata-class"></a>\_Classe Msvm TPMSettingData

Representa o estado configurado do dispositivo TPM.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ TPMSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ TPMSettingData** tem essas propriedades.

<dl> <dt>

**Protegido por dataprotegida**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para definir uma política para proteger os dados de uma VM; caso contrário, **false**. Um TPM recém-criado está desabilitado, portanto, o estado inicial da proteção de dados é **false**.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Os Estados habilitado e desabilitado de um elemento. O valor padrão é **desabilitado**.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Keyprotector**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers), **octetstring**
</dt> </dl>

O protetor de chave do cliente do serviço guardião de host.

</dd> <dt>

**LastKnownGoodKeyProtector**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers), **octetstring**
</dt> </dl>

O último protetor de chave válido criptografou com êxito o estado do dispositivo TPM na última inicialização da VM.

Essa propriedade é somente leitura para o cliente WMI e só pode ser modificada pelo dispositivo TPM de VM.

</dd> <dt>

**Blindado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para definir uma política que protege uma máquina virtual; caso contrário, **false**. Um TPM recém-criado está desabilitado, portanto, o estado de blindagem inicial é **false**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Fim do suporte do cliente<br/>    | Windows 10<br/>                                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

