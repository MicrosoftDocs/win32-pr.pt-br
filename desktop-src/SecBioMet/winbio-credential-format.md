---
title: Enumeração de WINBIO_CREDENTIAL_FORMAT (WinBio \_ Types. h)
description: Define sinalizadores que podem ser usados para especificar o formato de credencial do usuário final.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- API de Windows Biometric Framework de enumeração de WINBIO_CREDENTIAL_FORMAT
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
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085561"
---
# <a name="winbio_credential_format-enumeration"></a>\_Enumeração de formato de credencial WINBIO \_

Define sinalizadores que podem ser usados para especificar o formato de credencial do usuário final. Essa enumeração é usada pela função [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) .

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO \_ senha \_ genérica**
</dt> <dd>

A senha está em um formato genérico.

</dd> <dt>

<span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO \_ senha \_ empacotada**
</dt> <dd>

A senha está em um formato compactado.

</dd> <dt>

<span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ \_ protegido por senha**
</dt> <dd>

A credencial de senha foi encapsulada com [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de aplicativos cliente](client-application-enumerations.md)
</dt> <dt>

[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

