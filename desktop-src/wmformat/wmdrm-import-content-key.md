---
title: Estrutura de WMDRM_IMPORT_CONTENT_KEY (Drmexternals. h)
description: A estrutura de chave de conteúdo de importação do WMDRM \_ \_ \_ armazena a chave de conteúdo usada na importação de conteúdo protegido.
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_IMPORT_CONTENT_KEY
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369282"
---
# <a name="wmdrm_import_content_key-structure"></a>\_Estrutura de \_ chave de conteúdo de importação do WMDRM \_

A estrutura de chave de conteúdo de importação do WMDRM armazena a chave de conteúdo usada na importação de conteúdo protegido. **\_ \_ \_**

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**DW**
</dt> <dd>

Versão.

</dd> <dt>

**cbStructSize**
</dt> <dd>

Tamanho da estrutura em bytes.

</dd> <dt>

**dwIVKeyType**
</dt> <dd>

Tipo de chave do vetor de inicialização. Defina como WMDRM \_ KeyType \_ RC4.

</dd> <dt>

**cbIVKey**
</dt> <dd>

Tamanho da chave do vetor de inicialização em bytes.

</dd> <dt>

**dwContentKeyType**
</dt> <dd>

Tipo de chave de conteúdo. Defina para o \_ tipo de KeyType cocktail de WMDRM \_ .

</dd> <dt>

**cbContentKey**
</dt> <dd>

Tamanho da chave de conteúdo em bytes.

</dd> <dt>

**rgbKeyData**
</dt> <dd>

Endereço de um buffer que contém a chave de conteúdo. O tamanho do buffer deve corresponder ao valor de **cbContentKey**. Essa chave deve corresponder à chave importada da mensagem de licença XMR.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura, incluindo o buffer que contém a chave de sessão, deve ser criptografada com a chave de sessão e incluída no membro **pbEncryptedKeyMessage** da estrutura de [**\_ \_ \_ struct init de importação do WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .

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

 

 





