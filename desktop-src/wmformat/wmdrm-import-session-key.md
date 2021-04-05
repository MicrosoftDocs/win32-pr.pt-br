---
title: Estrutura de WMDRM_IMPORT_SESSION_KEY (Drmexternals. h)
description: A estrutura de chave de sessão de importação do WMDRM \_ \_ \_ contém a chave de sessão para importar conteúdo protegido.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_IMPORT_SESSION_KEY
- estruturar formato de mídia do Windows
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
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086097"
---
# <a name="wmdrm_import_session_key-structure"></a>\_Estrutura de \_ chave de sessão de importação WMDRM \_

A estrutura de chave de sessão de importação do WMDRM contém a chave de sessão para importar conteúdo protegido. **\_ \_ \_**

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

Tipo de chave de sessão. Defina como WMDRM \_ KeyType \_ RC4.

</dd> <dt>

**cbKey**
</dt> <dd>

Tamanho da chave de sessão, em bytes. Esse valor pode ser tão grande quanto necessário, considerando os limites de uma única operação RSA OAEP sobre toda a mensagem (essa estrutura e a chave de sessão).

</dd> <dt>

**rgbKey**
</dt> <dd>

Endereço de um buffer que contém a chave de sessão. O tamanho do buffer deve corresponder ao valor de **cbKey**. Os dados no buffer são um valor de chave gerado aleatoriamente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura, incluindo o buffer que contém a chave de sessão, deve ser criptografada com a chave pública do computador DRM do Windows Media e incluída no membro **pbEncryptedSessionKeyMessage** da estrutura de [**\_ \_ \_ struct init Import do WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                      |
| Versão<br/>                  | SDK do Windows Media Format 11<br/>                                                    |
| parâmetro<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





