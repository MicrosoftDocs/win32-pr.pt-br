---
description: Solicita que o dispositivo virtual Serviços de Área de Trabalho Remota inicie uma conexão de pipe com a máquina virtual.
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Método EnableEndPoints da classe Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a668e6a2605a52c7021f630145d6e4897e1c76ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164624"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a>Método EnableEndPoints da \_ classe RdvComponent Msvm

Solicita que o dispositivo virtual Serviços de Área de Trabalho Remota inicie uma conexão de pipe com a máquina virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

**Memória insuficiente** (32774)
</dt> <dt>

**Arquivo não encontrado** (32775)
</dt> <dt>

 (32776)
</dt> <dt>

 (32777)
</dt> <dt>

 (32778)
</dt> <dt>

 (32779)
</dt> <dt>

 (32780)
</dt> <dt>

 (32781)
</dt> <dt>

 (32782)
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

[**Msvm \_ RdvComponent**](msvm-rdvcomponent.md)
</dt> </dl>

 

 




