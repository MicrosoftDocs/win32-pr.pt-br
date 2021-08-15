---
description: Contém dados de entrada para o método IDirect3DAuthenticatedChannel9::Query.
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: D3DAUTHENTICATEDCHANNEL_QUERY_INPUT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 50f9c781ca6d495acd06d3aa67c337dee76b2310f5399615599a52e15000382c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974684"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a>Estrutura DE ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_

Contém dados de entrada para [**o método IDirect3DAuthenticatedChannel9::Query.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT {
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
} D3DAUTHENTICATEDCHANNEL_QUERY_INPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**QueryType**
</dt> <dd>

Um GUID que especifica a consulta. Para ver uma lista de valores, [consulte Proteção de Conteúdo Consultas](content-protection-queries.md).

</dd> <dt>

**Lidar com**
</dt> <dd>

Um alça para o canal autenticado. Para obter o handle, chame [**IDirect3DDevice9Video::CreateAuthenticatedChannel.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)

</dd> <dt>

**UINT**
</dt> <dd>

O número da sequência de consulta. No início da sessão, gere um número aleatório criptograficamente seguro de 32 bits a ser usado como o número de sequência inicial. Para cada consulta, incremente o número de sequência em 1.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de vídeo do Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




