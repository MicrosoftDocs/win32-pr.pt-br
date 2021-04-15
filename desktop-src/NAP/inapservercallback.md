---
title: Interface INapServerCallback (NapSystemHealthValidator. h)
description: Os SHVs usam para sinalizar a conclusão da solicitação assíncrona.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- INapServerCallback da interface NAP
- INapServerCallback interface NAP, descrita
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454663"
---
# <a name="inapservercallback-interface"></a>Interface INapServerCallback

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O **INapServerCallback** fornece um método que os SHVs usam para sinalizar a conclusão da solicitação assíncrona.

## <a name="members"></a>Membros

A interface **INapServerCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapServerCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapServerCallback** tem esses métodos.



| Método                                                                         | Descrição                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapServerCallback:: OnComplete**](inapservercallback-oncomplete-method.md) | Usado por SHVs para sinalizar a conclusão da solicitação assíncrona.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

