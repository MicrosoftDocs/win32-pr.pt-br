---
description: Contém a resposta a uma consulta D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT.
ms.assetid: 168f9455-8dc6-473a-ad2c-e51996b63650
title: D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT estrutura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: dc1ee0c4a0adb7f841796b542e7518188af741f8636e507c5411634d670b8bd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064575"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguidcount_output-structure"></a>Estrutura DE SAÍDA D3DAUTHENTICATEDCHANNEL \_ QUERBUGICTIONENCRYPTIONGUIDCOUNT \_

Contém a resposta a [**uma consulta D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT.**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  NumEncryptionGuids                   UINT;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Saída**
</dt> <dd>

Uma [**estrutura D3DAUTHENTICATEDCHANNEL \_ QUE \_**](d3dauthenticatedchannel-query-output.md) contém uma Message Authentication Code (MAC) e outros dados.

</dd> <dt>

**UINT**
</dt> <dd>

O número de GUIDs de criptografia.

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

 

 




