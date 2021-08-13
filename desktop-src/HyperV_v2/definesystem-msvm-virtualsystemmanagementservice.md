---
description: Cria uma nova instância de máquina virtual.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Método DefineSystem da classe Msvm_VirtualSystemManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 47b01a2fb0935873b5a36d69376eb09bfe6d4555613c0eb8dc8907589d4f5f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645796"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método DefineSystem da classe Msvm \_ VirtualSystemManagementService

Cria uma nova instância de máquina virtual. As propriedades que não são especificadas serão populadas com valores padrão.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SystemSettings* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma instância inserida da [**classe Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) usada para definir os atributos da máquina virtual a ser criada. Este parâmetro é necessário.

</dd> <dt>

*ResourceSettings* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres \[ \]**

Várias instâncias inseridas da [**classe Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (ou classes derivadas dela). Juntas, essas instâncias descrevem os recursos virtuais da máquina virtual. Um conjunto padrão de dispositivos será criado para a máquina virtual, independentemente de esse parâmetro estar definido. Por exemplo, o processador e a memória são criados e configurados automaticamente com valores padrão.

</dd> <dt>

*ReferenceConfiguration* \[ Em\]
</dt> <dd>

Tipo: **CIM \_ VirtualSystemSettingData**

Uma referência a uma instância da [**classe Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que é o objeto de nível superior de uma configuração de máquina virtual de referência. A configuração de referência será usada para complementar a configuração da nova máquina virtual se os *parâmetros SystemSettings* e *ResourceSettings* não fornecerem as respectivas informações.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Tipo: **Cim \_ ComputerSystem**

Uma referência a uma instância da classe [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual recém-criada.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Tipo: **CIM \_ ConcreteJob**

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Se esse método for executado de forma síncrona, ele retornará 0 se for bem-sucedido. Se esse método for executado de forma assíncrona, ele retornará 4096 e o parâmetro *de* saída do trabalho poderá ser usado para acompanhar o progresso da operação assíncrona. Qualquer outro valor de retorno indica um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Falha** (2)
</dt> <dt>

**Tempoout** (3)
</dt> <dt>

**Parâmetro inválido** (4)
</dt> <dt>

**DMTF Reservado** (..)
</dt> <dt>

**Parâmetros de método verificados – Trabalho iniciado** (4096)
</dt> <dt>

**Método Reservado** (4097..32767)
</dt> <dt>

**Específico do** fornecedor (32768..65535)
</dt> </dl>

## <a name="remarks"></a>Comentários

O acesso à [**classe \_ VirtualSystemManagementService do Msvm**](msvm-virtualsystemmanagementservice.md) pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

