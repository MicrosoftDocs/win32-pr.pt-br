---
title: Estrutura de DRM_PLAYLIST_CONTENT_ID (Drmexternals. h)
description: A estrutura de ID de conteúdo de playlist do DRM \_ \_ \_ contém informações sobre o conteúdo a ser copiado para o CD como parte de uma gravação de playlist.
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- Formato de mídia do Windows de estrutura de DRM_PLAYLIST_CONTENT_ID
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105765629"
---
# <a name="drm_playlist_content_id-structure"></a>\_Estrutura de \_ ID de conteúdo de playlist DRM \_

A estrutura de ID de conteúdo de playlist do DRM contém informações sobre o conteúdo a ser copiado para o CD como parte de uma gravação de playlist. **\_ \_ \_**

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**lpcwszV2Header**
</dt> <dd>

Cabeçalho DRM. Use esse membro se o conteúdo estiver protegido pelo Windows Media DRM versão 2 ou posterior.

</dd> <dt>

**lpcszV1KID**
</dt> <dd>

A ID da chave. Use esse membro se o conteúdo estiver protegido pelo Windows Media DRM versão 1.

</dd> <dt>

**pbOtherData**
</dt> <dd>

Buffer que contém dados suplementares.

</dd> <dt>

**cbOtherData**
</dt> <dd>

Tamanho do buffer **pbOtherData** em bytes.

</dd> <dt>

**dwUniqueIDForSession**
</dt> <dd>

Identificador exclusivo do conteúdo a ser usado na sessão atual.

</dd> <dt>

**dwValidFields**
</dt> <dd>

**DWORD** que indica os campos válidos desta estrutura.

</dd> </dl>

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

 

 





