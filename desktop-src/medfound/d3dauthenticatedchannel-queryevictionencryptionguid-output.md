---
description: Contém a resposta a uma consulta D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID.
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT estrutura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 01624b35b7c1b29267b490204a2d814adec1c7075eaf23e746e6ade04ceb0c6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942766"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a>Estrutura DE SAÍDA D3DAUTHENTICATEDCHANNEL \_ QUERBUGICTIONENCRYPTIONGUID \_

Contém a resposta a [**uma consulta D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID.**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**SAÍDA DA CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**
</dt> <dd>

Uma [**estrutura D3DAUTHENTICATEDCHANNEL \_ QUE \_ CONTÉM**](d3dauthenticatedchannel-query-output.md) uma Message Authentication Code (MAC) e outros dados.

</dd> <dt>

**EncryptionGuidIndex**
</dt> <dd>

O índice do GUID de criptografia.

</dd> <dt>

**EncryptionGuid**
</dt> <dd>

Um GUID que especifica um tipo de criptografia com suporte.

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

 

 




