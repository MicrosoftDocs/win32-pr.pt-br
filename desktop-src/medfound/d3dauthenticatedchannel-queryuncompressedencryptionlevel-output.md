---
description: Contém a resposta a uma consulta D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE.
ms.assetid: 66735ce3-c16b-4eca-9283-5d3bc37d73d3
title: D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT estrutura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: aa9642a37237425f1d9236632fdf0c16bf226b3f2952928cceccf1b1c577d2e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061966"
---
# <a name="d3dauthenticatedchannel_queryuncompressedencryptionlevel_output-structure"></a>Estrutura DE SAÍDA D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_

Contém a resposta a [**uma consulta D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE.**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  GUID                                 EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Saída**
</dt> <dd>

Uma [**estrutura D3DAUTHENTICATEDCHANNEL \_ QUE \_ CONTÉM**](d3dauthenticatedchannel-query-output.md) uma Message Authentication Code (MAC) e outros dados.

</dd> <dt>

**EncryptionGuid**
</dt> <dd>

Um GUID que especifica o tipo de criptografia atual.

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

 

 




