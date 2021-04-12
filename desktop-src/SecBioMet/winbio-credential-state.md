---
title: Enumeração de WINBIO_CREDENTIAL_STATE (WinBio \_ Types. h)
description: Define os valores que especificam se uma credencial foi associada aos dados biométricos para um usuário final.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- API de Windows Biometric Framework de enumeração de WINBIO_CREDENTIAL_STATE
- PWINBIO_CREDENTIAL_STATE Windows Biometric Framework API do ponteiro de enumeração
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b8292cbbaefeeda0f6bf349f55e8f825f1756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294769"
---
# <a name="winbio_credential_state-enumeration"></a>\_Enumeração de estado de credencial WINBIO \_

Define os valores que especificam se uma credencial foi associada aos dados biométricos para um usuário final. Essa enumeração é usada pela função [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**\_credencial WINBIO \_ não \_ definida**
</dt> <dd>

Uma credencial foi associada ao usuário final.

</dd> <dt>

<span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**\_conjunto de credenciais WINBIO \_**
</dt> <dd>

Uma credencial não foi associada ao usuário final.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de aplicativos cliente](client-application-enumerations.md)
</dt> <dt>

[**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





