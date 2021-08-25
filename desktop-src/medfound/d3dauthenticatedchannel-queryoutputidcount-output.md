---
description: Contém a resposta a uma consulta D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT.
ms.assetid: 8b9fa0dc-bbe5-4382-8acc-59aeadfca825
title: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT estrutura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: c97f55d05aff3feb1857456ec04c4fa48872487decc5812912081b894896dce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777546"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_output-structure"></a>Estrutura DE SAÍDA D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_

Contém a resposta a uma [**consulta D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT.**](d3dauthenticatedquery-outputidcount.md)

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
  HANDLE                               CryptoSessionHandle;
  UINT                                 NumOutputIDs;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Saída**
</dt> <dd>

Uma [**estrutura D3DAUTHENTICATEDCHANNEL \_ QUE \_**](d3dauthenticatedchannel-query-output.md) contém uma Message Authentication Code (MAC) e outros dados.

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Um alça para o dispositivo.

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

Um alça para a sessão criptográfica.

</dd> <dt>

**NumOutputIDs**
</dt> <dd>

O número de IDs de saída associadas ao dispositivo especificado e à sessão criptográfica.

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

 

 




