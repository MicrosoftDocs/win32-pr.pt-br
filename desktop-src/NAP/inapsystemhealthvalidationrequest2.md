---
title: Interface INapSystemHealthValidationRequest2 (NapSystemHealthValidator.h)
description: Fornece métodos usados para dar suporte a validadores de saúde do sistema que são definidos pelo desenvolvedor do aplicativo.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- INapSystemHealthValidationRequest2 interface NAP
- NAP da interface INapSystemHealthValidationRequest2, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6438394120ecd901c6de6d7a8ccac40f742d9f73d27a36682de894d9c5a7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620845"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a>Interface INapSystemHealthValidationRequest2

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A interface **INapSystemHealthValidationRequest2** fornece métodos usados para dar suporte a validadores de saúde do sistema que são definidos pelo desenvolvedor do aplicativo.

> [!Note]  
> Essa interface herda todos os métodos de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) e deve ser usada em vez disso.

 

## <a name="members"></a>Membros

A interface **INapSystemHealthValidationRequest2** herda de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md). **INapSystemHealthValidationRequest2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapSystemHealthValidationRequest2** tem esses métodos.



| Método                                                                                                    | Descrição                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest2::GetConfigId**](inapsystemhealthvalidationrequest2-getconfigid.md) | Recupera a ID de configuração em uma solicitação de validação.<br/> |



 

## <a name="remarks"></a>Comentários

Se um SHV não dá suporte [**a INapComponentConfig3,**](inapcomponentconfig3.md)essa interface não se aplica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                 |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referência nap](nap-reference.md)
</dt> </dl>

 

 





