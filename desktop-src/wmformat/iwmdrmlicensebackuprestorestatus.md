---
title: Interface IWMDRMLicenseBackupRestoreStatus
description: A interface IWMDRMLicenseBackupRestoreStatus fornece um método para recuperar informações detalhadas de status sobre uma operação de backup ou restauração de licença. Essa interface é entregue com eventos de progresso gerados durante as operações de backup e restauração de licença.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- Formato de mídia do Windows da interface IWMDRMLicenseBackupRestoreStatus
- Formato de mídia do Windows da interface IWMDRMLicenseBackupRestoreStatus, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294346"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a>Interface IWMDRMLicenseBackupRestoreStatus

A interface **IWMDRMLicenseBackupRestoreStatus** fornece um método para recuperar informações detalhadas de status sobre uma operação de backup ou restauração de licença.

Essa interface é entregue com eventos de progresso gerados durante as operações de backup e restauração de licença. Vários eventos **MEWMDRMLicenseBackupProgress** são gerados durante o backup de licença, cada um deles com uma instância de acompanhamento dessa interface. O mesmo é verdadeiro para eventos **MEWMDRMLicenseRestoreProgress** , que são gerados durante a restauração da licença.

Para recuperar um ponteiro para uma instância da interface **IWMDRMLicenseBackupRestoreStatus** , você deve primeiro chamar o método **IMFMediaEvent:: GetValue** do evento Progress. O valor que você recupera do evento é um ponteiro para a interface **IUnknown** do objeto que implementa a interface **IWMDRMLicenseBackupRestoreStatus** .

## <a name="members"></a>Membros

A interface **IWMDRMLicenseBackupRestoreStatus** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicenseBackupRestoreStatus** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMLicenseBackupRestoreStatus** tem esses métodos.



| Método                                                          | Descrição                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) | Recupera informações detalhadas de status sobre uma operação de backup ou restauração de licença.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

