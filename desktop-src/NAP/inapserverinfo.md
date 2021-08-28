---
title: Interface INapServerInfo (NapServerManagement.h)
description: Os clientes de gerenciamento (por exemplo, provedores WMI ou ferramentas de linha de comando) usam para consultar o status do sistema de servidores NAP.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- INapServerInfo interface NAP
- NAP da interface INapServerInfo, descrita
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
ms.openlocfilehash: 556c2a5b7e7545038995d5091d46931352f9ee32bddfa31b91237dfa54d69620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626096"
---
# <a name="inapserverinfo-interface"></a>Interface INapServerInfo

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **INapServerInfo** fornece métodos que os clientes de Gerenciamento (por exemplo, provedores WMI ou ferramentas de linha de comando) usam para consultar o status do sistema de servidor NAP.

## <a name="members"></a>Membros

A interface **INapServerInfo** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapServerInfo** também tem estes tipos de membros:

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
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                               |
| Cabeçalho<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referência nap](nap-reference.md)
</dt> </dl>

 

