---
title: Interface INapComponentConfig3 (NapCommon. h)
description: Fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema) para definir e modificar dados de configuração para uma ID de configuração específica.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- INapComponentConfig3 da interface NAP
- INapComponentConfig3 interface NAP, descrita
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782308"
---
# <a name="inapcomponentconfig3-interface"></a>Interface INapComponentConfig3

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A interface **INapComponentConfig3** fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema) para definir e modificar dados de configuração para uma ID de configuração específica.

> [!Note]  
> Essa interface herda todos os métodos de [**INapComponentConfig2**](inapcomponentconfig2.md) e deve ser usada em seu lugar.

 

## <a name="members"></a>Membros

A interface **INapComponentConfig3** herda de [**INapComponentConfig2**](inapcomponentconfig2.md). **INapComponentConfig3** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapComponentConfig3** tem esses métodos.



| Método                                                                                | Descrição                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig3::D eleteAllConfig**](inapcomponentconfig3-deleteallconfig.md) | Implementado por SHVs para fornecer uma maneira de redefinir o armazenamento SHV para seu estado original após a instalação.<br/>      |
| [**INapComponentConfig3::D eleteConfig**](inapcomponentconfig3-deleteconfig.md)       | Implementado por SHVs para fornecer uma maneira de excluir dados de configuração para uma ID de configuração específica.<br/>  |
| [**INapComponentConfig3::GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md) | Implementado por SHVs para fornecer uma maneira de obter dados de configuração para uma ID de configuração específica.<br/>  |
| [**INapComponentConfig3:: NewConfig**](inapcomponentconfig3-newconfig.md)             | Implementado por SHVs para fornecer uma maneira de criar dados de configuração para uma ID de configuração específica.<br/>  |
| [**INapComponentConfig3::SetConfigToID**](inapcomponentconfig3-setconfigtoid.md)     | Implementado por SHVs para fornecer uma maneira de definir os dados de configuração para uma ID de configuração específica.<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface não deve ser implementada por agentes de integridade do sistema (SHAs) ou clientes de imposição de quarentena (QECs).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

 





