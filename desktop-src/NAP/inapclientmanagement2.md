---
title: Interface INapClientManagement2 (NapManagement.h)
description: Fornece métodos para gerenciamento de cliente NAP. | Interface INapClientManagement2 (NapManagement.h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- INapClientManagement2 interface NAP
- NAP da interface INapClientManagement2, descrita
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
ms.openlocfilehash: 4f459e6fa0d883203bf52ebbd0aaab06ee93cef00d1fb52af3d670f71cf7ab52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800096"
---
# <a name="inapclientmanagement2-interface"></a>Interface INapClientManagement2

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A interface **INapClientManagement2** fornece métodos para gerenciamento de cliente NAP.

> [!Note]  
> Essa interface herda todos os métodos de [**INapClientManagement**](inapclientmanagement.md) e deve ser usada em vez disso.

 

## <a name="members"></a>Membros

A interface **INapClientManagement2** herda de [**INapClientManagement.**](inapclientmanagement.md) **INapClientManagement2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapClientManagement2** tem esses métodos.



| Método                                                                                                    | Descrição                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**INapClientManagement2::GetSystemIsolationInfoEx**](inapclientmanagement2-getsystemisolationinfoex.md) | Recupera informações sobre o estado de isolamento e o estado de isolamento estendido do cliente Nap.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referência nap](nap-reference.md)
</dt> </dl>

 

 





