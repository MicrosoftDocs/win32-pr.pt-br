---
description: Recupera um erro devido a um trabalho com falha.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: Método GetError da classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0b43d433bf9d2a3967efcc4a2e927d3bf687ebfa5ac67d7c7e34c48c34832c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813262"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a>Método GetError da \_ classe CIM ConcreteJob

Recupera um erro devido a um trabalho com falha. Quando o trabalho está em execução ou foi encerrado sem erros, esse método não retorna nenhuma instância de [**\_ erro CIM**](cim-error.md) . No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma instância de **\_ erro CIM** é retornada.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Erro* \[ do fora\]
</dt> <dd>

Retorna uma instância de [**\_ erro CIM**](cim-error.md) se o **OperationalStatus** no trabalho não for "OK"; caso contrário, retornará **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Erro não especificado** (2)
</dt> <dt>

**Tempo limite** (3)
</dt> <dt>

**Com falha** (4)
</dt> <dt>

**Parâmetro inválido** (5)
</dt> <dt>

**Acesso negado** (6)
</dt> <dt>

**DMTF reservado** (..)
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

[**\_CONCRETEJOB CIM**](cim-concretejob.md)
</dt> </dl>

 

 




