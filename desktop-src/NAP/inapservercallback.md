---
title: Interface INapServerCallback (NapSystemHealthValidator.h)
description: ShVs usam para sinalizar a conclusão da solicitação assíncrona.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- INapServerCallback interface NAP
- NAP da interface INapServerCallback, descrita
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
ms.openlocfilehash: 47876290a58d6029559ef4d18baa9067913fe9034cbf218e40f0e382902270e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626146"
---
# <a name="inapservercallback-interface"></a>Interface INapServerCallback

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **INapServerCallback** fornece um método usado por SHVs para sinalizar a conclusão da solicitação assíncrona.

## <a name="members"></a>Membros

A interface **INapServerCallback** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapServerCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapServerCallback** tem esses métodos.



| Método                                                                         | Descrição                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapServerCallback::OnComplete**](inapservercallback-oncomplete-method.md) | Usado por SHVs para sinalizar a conclusão da solicitação assíncrona.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                    |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referência nap](nap-reference.md)
</dt> </dl>

 

