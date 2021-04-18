---
description: Representa as fábricas de ativação registradas chamando a função RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814058"
---
# <a name="ro_registration_cookie"></a>\_cookie de registro ro \_

Representa as fábricas de ativação registradas chamando a função [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Comentários

A função [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) retorna um **\_ \_ Cookie ro de registro** quando uma fábricas de classe ativável é registrada com o Windows Runtime. A função [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) usa o cookie para remover as fábricas de classes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Roapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
