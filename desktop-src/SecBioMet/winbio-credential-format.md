---
title: WINBIO_CREDENTIAL_FORMAT enumeração (Tipos \_ Winbio.h)
description: Define sinalizadores que podem ser usados para especificar o formato de credencial do usuário final.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- WINBIO_CREDENTIAL_FORMAT enumeração Windows API do Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82185bdb9d8170abbdba04e758010443dc8be6a37e198edb27a137024dacf9af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910819"
---
# <a name="winbio_credential_format-enumeration"></a>\_Enumeração WINBIO CREDENTIAL \_ FORMAT

Define sinalizadores que podem ser usados para especificar o formato de credencial do usuário final. Essa enumeração é usada pela [**função WinBioSetCredential.**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)

## <a name="syntax"></a>Sintaxe


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**SENHA WINBIO \_ \_ GENÉRICA**
</dt> <dd>

A senha está em um formato genérico.

</dd> <dt>

<span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**SENHA WINBIO \_ \_ EMPACOTADA**
</dt> <dd>

A senha está em um formato compactado.

</dd> <dt>

<span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**SENHA WINBIO \_ \_ PROTEGIDA**
</dt> <dd>

A credencial de senha foi empacotada [**com CredProtect.**](/windows/desktop/api/wincred/nf-wincred-credprotecta)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de aplicativo cliente](client-application-enumerations.md)
</dt> <dt>

[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

