---
description: Revoga o acesso à sessão interativa da máquina virtual da lista especificada de relações de confiança.
ms.assetid: c6d3df04-c31e-404a-9a04-3e8653bdc14f
title: Método RevokeInteractiveSessionAccess da classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.RevokeInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ab92f375f082d3af1f04b3fe52db5cb7964e3d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662155"
---
# <a name="revokeinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a>Método RevokeInteractiveSessionAccess da \_ classe TerminalService Msvm

Revoga o acesso à sessão interativa da máquina virtual da lista especificada de relações de confiança.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RevokeInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ no\]
</dt> <dd>

Uma referência a uma instância da classe [**de \_ sistema**](cim-computersystem.md) de computador CIM que representa a máquina virtual para a qual o acesso será revogado.

</dd> <dt>

*Relações de confiança* \[ no\]
</dt> <dd>

Uma matriz de cadeias de caracteres, cada uma identificando um confiável cujos direitos de acesso serão revogados. Os identificadores de confiança devem ser especificados no formato compatível com o Windows SAM ou no formato de cadeia de caracteres SID do Windows.

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

**Sem suporte** (1)
</dt> <dt>

**Falha** (2)
</dt> <dt>

**Tempo limite** (3)
</dt> <dt>

**Parâmetro inválido** (4)
</dt> <dt>

**Estado inválido** (5)
</dt> <dt>

**Parâmetros incompatíveis** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Método reservado** (4097.. 32767)
</dt> <dt>

**Específico do fornecedor** (32768.. 65535)
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

[**Msvm \_ TerminalService**](msvm-terminalservice.md)
</dt> </dl>

 

