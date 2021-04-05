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
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644500"
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
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

