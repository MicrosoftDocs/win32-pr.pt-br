---
title: Interface INapEnforcementClientConnection2 (NapEnforcementClient. h)
description: Permitir o gerenciamento de conexão do cliente. | Interface INapEnforcementClientConnection2 (NapEnforcementClient. h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- INapEnforcementClientConnection2 da interface NAP
- INapEnforcementClientConnection2 interface NAP, descrita
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60e91ffbc12534bb3b5a8ac22cbd13a1238ba32e09b4f56b4ab570ffd1ea8be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144389"
---
# <a name="inapenforcementclientconnection2-interface"></a>Interface INapEnforcementClientConnection2

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O **INapEnforcementClientConnection2** fornece métodos que permitem o gerenciamento de conexão do cliente.

> [!Note]  
> Essa interface herda todos os métodos de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) e deve ser usada em seu lugar.

 

## <a name="members"></a>Membros

A interface **INapEnforcementClientConnection2** herda de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md). **INapEnforcementClientConnection2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapEnforcementClientConnection2** tem esses métodos.



| Método                                                                                                              | Descrição                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection2::GetInstalledShvs**](inapenforcementclientconnection2-getinstalledshvs.md)     | Usado para obter as IDs dos SHVs instalados para o cliente.<br/>             |
| [**INapEnforcementClientConnection2::GetIsolationInfoEx**](inapenforcementclientconnection2-getisolationinfoex.md) | Usado para obter as informações de isolamento para o cliente.<br/>                 |
| [**INapEnforcementClientConnection2::SetInstalledShvs**](inapenforcementclientconnection2-setinstalledshvs.md)     | Usado pelo NapAgent para definir as IDs SHV instaladas para o cliente.<br/>     |
| [**INapEnforcementClientConnection2::SetIsolationInfoEx**](inapenforcementclientconnection2-setisolationinfoex.md) | Usado pelo NapAgent para definir as informações de isolamento para o cliente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

 





