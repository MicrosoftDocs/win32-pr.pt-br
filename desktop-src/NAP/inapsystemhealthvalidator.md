---
title: Interface INapSystemHealthValidator (NapSystemHealthValidator. h)
description: Deve ser implementado por desenvolvedores de SHV para permitir que o sistema NAP se comunique com um SHV.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- INapSystemHealthValidator da interface NAP
- INapSystemHealthValidator interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7310afe1c61dd61344bd1ed355f78735dc7785f9016bbcbb702073b2a06feba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686056"
---
# <a name="inapsystemhealthvalidator-interface"></a>Interface INapSystemHealthValidator

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O **INapSystemHealthValidator** fornece métodos que devem ser implementados por desenvolvedores de SHV para permitir que o sistema NAP se comunique com um SHV.

## <a name="members"></a>Membros

A interface **INapSystemHealthValidator** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthValidator** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapSystemHealthValidator** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidator:: Validate**](inapsystemhealthvalidator-validate-method.md) | O sistema NAP chama esse método definido pelo aplicativo para validar o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recebido de um cliente. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                    |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

