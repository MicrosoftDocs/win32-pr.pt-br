---
title: Interface INapSystemHealthValidationRequest2 (NapSystemHealthValidator. h)
description: Fornece métodos que são usados para dar suporte a validadores de integridade do sistema que são definidos pelo desenvolvedor do aplicativo.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- INapSystemHealthValidationRequest2 da interface NAP
- INapSystemHealthValidationRequest2 interface NAP, descrita
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
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769428"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a>Interface INapSystemHealthValidationRequest2

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A interface **INapSystemHealthValidationRequest2** fornece métodos que são usados para dar suporte a validadores de integridade do sistema que são definidos pelo desenvolvedor do aplicativo.

> [!Note]  
> Essa interface herda todos os métodos de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) e deve ser usada em seu lugar.

 

## <a name="members"></a>Membros

A interface **INapSystemHealthValidationRequest2** herda de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md). **INapSystemHealthValidationRequest2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapSystemHealthValidationRequest2** tem esses métodos.



| Método                                                                                                    | Descrição                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest2:: getconfigid**](inapsystemhealthvalidationrequest2-getconfigid.md) | Recupera a ID de configuração em uma solicitação de validação.<br/> |



 

## <a name="remarks"></a>Comentários

Se um SHV não oferecer suporte a [**INapComponentConfig3**](inapcomponentconfig3.md), essa interface não se aplicará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                 |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

 





