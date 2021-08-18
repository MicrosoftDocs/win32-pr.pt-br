---
title: WMDRM_IMPORT_SESSION_KEY estrutura (Drmexternals.h)
description: A estrutura WMDRM \_ IMPORT SESSION KEY contém a chave de sessão para importar conteúdo \_ \_ protegido.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- WMDRM_IMPORT_SESSION_KEY formato de mídia do Windows
- formato de mídia de janelas de estrutura
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34cdff6d17ad6ce60dd40478b56c9718be0863295422d2e5c60fee2c437dc6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844055"
---
# <a name="wmdrm_import_session_key-structure"></a>Estrutura DE CHAVE DE \_ \_ SESSÃO DE \_ IMPORTAÇÃO DO WMDRM

A **estrutura WMDRM \_ IMPORT SESSION \_ \_ KEY** contém a chave de sessão para importar conteúdo protegido.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwKeyType**
</dt> <dd>

Tipo de chave de sessão. Definido como WMDRM \_ KEYTYPE \_ RC4.

</dd> <dt>

**cbKey**
</dt> <dd>

Tamanho da chave de sessão, em bytes. Esse valor pode ser tão grande quanto você precisar, considerando os limites de uma única operação RSA OAEP em toda a mensagem (essa estrutura mais a chave de sessão).

</dd> <dt>

**Rgbkey**
</dt> <dd>

Endereço de um buffer que contém a chave de sessão. O tamanho do buffer deve corresponder ao valor **de cbKey.** Os dados no buffer são um valor de chave gerado aleatoriamente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura, incluindo o buffer que contém a chave de sessão, deve ser criptografada com a chave pública do computador drm de mídia Windows e incluída no **membro pbEncryptedSessionKeyMessage** da estrutura [**\_ \_ \_ STRUCT WMDRM IMPORT INIT.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                      |
| Versão<br/>                  | Windows SDK do Formato de Mídia 11<br/>                                                    |
| Cabeçalho<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





