---
description: Representa as fábricas de ativação registradas chamando a função RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8efc7d3364f02c11750e6b42ddec6d2a3dee3f83368d277bc979a22ea3a0854a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741593"
---
# <a name="ro_registration_cookie"></a>COOKIE DE \_ REGISTRO RO \_

Representa as fábricas de ativação registradas chamando a [**função RoRegisterActivationFactories.**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Comentários

A [**função RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) retorna um COOKIE de **\_ REGISTRO \_ RO** quando as fábricas de classes ativas são registradas com o Windows Runtime. A [**função RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) usa o cookie para remover as fábricas de classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Roapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
