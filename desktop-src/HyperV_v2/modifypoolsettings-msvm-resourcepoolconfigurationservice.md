---
description: Altera as configurações de um pool filho que não estão relacionadas à alocação.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Método ModifyPoolSettings da classe Msvm_ResourcePoolConfigurationService dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e1c8d71f8f380d5049d6bd2743e1f1d48573407431372c53aaeaacf4297ec56e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694036"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Método ModifyPoolSettings da classe Msvm \_ ResourcePoolConfigurationService

Altera as configurações de um pool filho que não estão relacionadas à alocação.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ChildPool* \[ Em\]
</dt> <dd>

Uma referência a uma instância da classe [**\_ ResourcePool cim**](cim-resourcepool.md) que representa o pool filho a ser modificado.

</dd> <dt>

*PoolSettings* \[ Em\]
</dt> <dd>

Uma instância inserida da [**classe Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) usada para especificar as novas configurações para o pool.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Trabalho concluído sem erro** (0)
</dt> <dt>

**DMTF Reservado** (..)
</dt> <dt>

**Parâmetros de método verificados – Trabalho iniciado** (4096)
</dt> <dt>

**Método Reservado** (4097..32767)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

**Desconhecido** (32771)
</dt> <dt>

**Tempoout** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

**Em uso** (32774)
</dt> <dt>

**Estado inválido** (32775)
</dt> <dt>

**Tipo de recurso incorreto para o pool** (32776)
</dt> <dt>

**Indisponível** (32777)
</dt> <dt>

**Memória sem** memória (32778)
</dt> <dt>

**Fornecedor Reservado** (32779)
</dt> <dt>

**Recursos insuficientes** (32780)
</dt> <dt>

**Objeto não encontrado** (32781..32787)
</dt> <dt>

**Object Exists** (32788)
</dt> <dt>

**Específico do** fornecedor (32768..65535)
</dt> </dl>

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

[**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

