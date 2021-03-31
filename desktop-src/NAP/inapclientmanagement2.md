---
title: Interface INapClientManagement2 (NapManagement. h)
description: Fornece métodos para o gerenciamento de cliente NAP. | Interface INapClientManagement2 (NapManagement. h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- INapClientManagement2 da interface NAP
- INapClientManagement2 interface NAP, descrita
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012048"
---
# <a name="inapclientmanagement2-interface"></a>Interface INapClientManagement2

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A interface **INapClientManagement2** fornece métodos para o gerenciamento de cliente NAP.

> [!Note]  
> Essa interface herda todos os métodos de [**INapClientManagement**](inapclientmanagement.md) e deve ser usada em seu lugar.

 

## <a name="members"></a>Membros

A interface **INapClientManagement2** herda de [**INapClientManagement**](inapclientmanagement.md). **INapClientManagement2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapClientManagement2** tem esses métodos.



| Método                                                                                                    | Descrição                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**INapClientManagement2::GetSystemIsolationInfoEx**](inapclientmanagement2-getsystemisolationinfoex.md) | Recupera informações sobre o estado de isolamento e o estado de isolamento estendido do cliente NAP.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

 





