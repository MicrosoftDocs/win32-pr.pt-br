---
title: Interface INapComponentConfig3 (NapCommon.h)
description: Fornece métodos de configuração do sistema NAP para shVs (validadores de saúde do sistema) definirem e modificarem dados de configuração para uma ID de configuração específica.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- INapComponentConfig3 interface NAP
- NAP da interface INapComponentConfig3, descrita
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
ms.openlocfilehash: fea8ab7b42589fa548439b03c04ade56db498750ccd47841b806dcb6b506d3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803076"
---
# <a name="inapcomponentconfig3-interface"></a>Interface INapComponentConfig3

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A interface **INapComponentConfig3** fornece métodos de configuração do sistema NAP para shVs (validadores de saúde do sistema) definirem e modificarem dados de configuração para uma ID de configuração específica.

> [!Note]  
> Essa interface herda todos os métodos de [**INapComponentConfig2**](inapcomponentconfig2.md) e deve ser usada em vez disso.

 

## <a name="members"></a>Membros

A interface **INapComponentConfig3** herda [**de INapComponentConfig2.**](inapcomponentconfig2.md) **INapComponentConfig3** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapComponentConfig3** tem esses métodos.



| Método                                                                                | Descrição                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig3::D eleteAllConfig**](inapcomponentconfig3-deleteallconfig.md) | Implementado por SHVs para fornecer uma maneira de redefinir o armazenamento SHV para seu estado original após a instalação.<br/>      |
| [**INapComponentConfig3::D eleteConfig**](inapcomponentconfig3-deleteconfig.md)       | Implementado por SHVs para fornecer uma maneira de excluir dados de configuração para uma ID de configuração específica.<br/>  |
| [**INapComponentConfig3::GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md) | Implementado por SHVs para fornecer uma maneira de obter dados de configuração para uma ID de configuração específica.<br/>  |
| [**INapComponentConfig3::NewConfig**](inapcomponentconfig3-newconfig.md)             | Implementado por SHVs para fornecer uma maneira de criar dados de configuração para uma ID de configuração específica.<br/>  |
| [**INapComponentConfig3::SetConfigToID**](inapcomponentconfig3-setconfigtoid.md)     | Implementado por SHVs para fornecer uma maneira de definir os dados de configuração para uma ID de configuração específica.<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface não deve ser implementada por SHAs (agentes de saúde do sistema) ou QECs (clientes de imposição de quarentena).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referência nap](nap-reference.md)
</dt> </dl>

 

 





