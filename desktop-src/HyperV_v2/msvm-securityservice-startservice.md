---
description: Método StartService da classe Msvm_SecurityService – inicia o serviço.
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: Método StartService da classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31e16eea84cf61ace11c241b6409a5810f74b8f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111394"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a>Método StartService da classe Msvm \_ SecurityService

Inicia o serviço.

## <a name="syntax"></a>Sintaxe


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Em caso de sucesso, retorna um 0; caso contrário, retornará um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Msvm \_ SecurityService**](msvm-securityservice.md)
</dt> </dl>

 

 




