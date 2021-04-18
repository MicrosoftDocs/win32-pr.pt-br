---
description: Interrompe o serviço.
ms.assetid: c96ca784-c935-41a4-b1aa-8360cf270c9e
title: Método StopService da classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f26efeefb7cd9ace2e17db565c4ff71190fa2814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778582"
---
# <a name="stopservice-method-of-the-msvm_terminalservice-class"></a>Método StopService da classe Msvm \_ TerminalService

Interrompe o serviço.

## <a name="syntax"></a>Sintaxe


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos seguintes valores:

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
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

[**Msvm \_ TerminalService**](msvm-terminalservice.md)
</dt> </dl>

 

 




