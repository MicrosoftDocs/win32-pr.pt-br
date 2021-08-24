---
title: WINBIO_CREDENTIAL_STATE enumeração (Tipos \_ Winbio.h)
description: Define valores que especificam se uma credencial foi associada aos dados biométricos de um usuário final.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- WINBIO_CREDENTIAL_STATE enumeração Windows API do Biometric Framework
- PWINBIO_CREDENTIAL_STATE de enumeração Windows API do Biometric Framework
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
ms.openlocfilehash: ce0e176479a68d39b017e852e17a73691b8349d7c6faa6be62130007a09dcef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868056"
---
# <a name="winbio_credential_state-enumeration"></a>\_Enumeração WINBIO CREDENTIAL \_ STATE

Define valores que especificam se uma credencial foi associada aos dados biométricos de um usuário final. Essa enumeração é usada pela [**função WinBioGetCredentialState.**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**CREDENCIAL \_ WINBIO \_ NÃO \_ DEFINIDA**
</dt> <dd>

Uma credencial foi associada ao usuário final.

</dd> <dt>

<span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**CONJUNTO DE CREDENCIAIS DO WINBIO \_ \_**
</dt> <dd>

Uma credencial não foi associada ao usuário final.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de aplicativo cliente](client-application-enumerations.md)
</dt> <dt>

[**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





