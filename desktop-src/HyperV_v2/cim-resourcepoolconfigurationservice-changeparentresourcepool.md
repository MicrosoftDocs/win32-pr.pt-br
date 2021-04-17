---
description: Inicie um trabalho para alterar um pool pai usando as configurações de alocação especificadas.
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: Método ChangeParentResourcePool da classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.ChangeParentResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6ef852d6af8f0973b6b3f29fca5fcd90e9ce726a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789810"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método ChangeParentResourcePool da \_ classe RESOURCEPOOLCONFIGURATIONSERVICE CIM

Inicie um trabalho para alterar um pool pai usando as configurações de alocação especificadas.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangeParentResourcePool(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPool[],
  [in]  string               Settings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ChildPool* \[ no\]
</dt> <dd>

Um [**\_ ResourcePool CIM**](cim-resourcepool.md) que faz referência ao pool filho.

</dd> <dt>

*ParentPool* \[ no\]
</dt> <dd>

Uma [**matriz \_ ResourcePool do CIM**](cim-resourcepool.md) que faz referência ao pool (s) pai.

</dd> <dt>

*Configurações* \[ do no\]
</dt> <dd>

Cadeia de caracteres opcional que contém uma representação de uma instância do [**CIM \_ SettingData**](cim-settingdata.md) que é usada para especificar as configurações para o pool pai.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Um [**\_ ConcreteJob CIM**](cim-concretejob.md) que referencia o trabalho (pode ser **nulo** se o trabalho for concluído).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

<dl> <dt>

**Trabalho concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Desconhecido** (2)
</dt> <dt>

**Tempo limite** (3)
</dt> <dt>

**Com falha** (4)
</dt> <dt>

**Parâmetro inválido** (5)
</dt> <dt>

**Em uso** (6)
</dt> <dt>

**ResourceType incorreto para o pool** (7)
</dt> <dt>

**Recursos insuficientes** (8)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Tamanho sem suporte** (4097)
</dt> <dt>

**Método reservado** (4098.. 32767)
</dt> <dt>

**Específico do fornecedor** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




