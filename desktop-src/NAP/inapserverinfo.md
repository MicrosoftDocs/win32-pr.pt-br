---
title: Interface INapServerInfo (NapServerManagement. h)
description: Os clientes de gerenciamento (por exemplo, provedores WMI ou ferramentas de linha de comando) usam para consultar o status do sistema de servidor NAP.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- INapServerInfo da interface NAP
- INapServerInfo interface NAP, descrita
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec17e3303fe4af4d359279de6c5fa7aa5f34d409
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760692"
---
# <a name="inapserverinfo-interface"></a>Interface INapServerInfo

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O **INapServerInfo** fornece métodos que os clientes de gerenciamento (por exemplo, provedores WMI ou ferramentas de linha de comando) usam para consultar o status do sistema de servidor NAP.

## <a name="members"></a>Membros

A interface **INapServerInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapServerInfo** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapServerInfo** tem esses métodos.



| Método                                                                                                                   | Descrição                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**INapServerInfo::GetFailureCategoryMappings**](inapserverinfo-getfailurecategorymappings-method.md)                   | Recupera os mapeamentos de categoria de falha para um SHV especificado.<br/> |
| [**INapServerInfo::GetNapServerInfo**](inapserverinfo-getnapserverinfo-method.md)                                       | Recupera informações sobre o servidor NAP.<br/>                  |
| [**INapServerInfo::GetRegisteredSystemHealthValidators**](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | Recupera uma lista de SHVs registrados.<br/>                         |



 

## <a name="remarks"></a>Comentários

Esses métodos fornecem apenas informações estáticas sobre o servidor NAP e seus componentes no sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                               |
| parâmetro<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

