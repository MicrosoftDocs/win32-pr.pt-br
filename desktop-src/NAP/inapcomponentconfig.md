---
title: Interface INapComponentConfig (NapCommon. h)
description: Fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema).
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- INapComponentConfig da interface NAP
- INapComponentConfig interface NAP, descrita
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369482"
---
# <a name="inapcomponentconfig-interface"></a>Interface INapComponentConfig

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A interface **INapComponentConfig** fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema).

> [!Note]  
> [**INapComponentConfig2**](inapcomponentconfig2.md) e [**INapComponentConfig3**](inapcomponentconfig3.md) herdam todos os métodos dessa interface e devem ser usados em seu lugar.

 

## <a name="members"></a>Membros

A interface **INapComponentConfig** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapComponentConfig** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapComponentConfig** tem esses métodos.



| Método                                                                          | Descrição                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**INapComponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md)         | Recupera a configuração do componente SHV.<br/>                                |
| [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)           | Inicia a interface do usuário personalizada para um componente SHV.<br/>              |
| [**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md) | Especifica se o componente SHV dá suporte a uma interface do usuário personalizada.<br/> |
| [**INapComponentConfig:: setconfig**](inapcomponentconfig-setconfig.md)         | Define a configuração do componente SHV.<br/>                                     |



 

## <a name="remarks"></a>Comentários

Essa interface não deve ser implementada por agentes de integridade do sistema (SHAs) ou clientes de imposição de quarentena (QECs).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

