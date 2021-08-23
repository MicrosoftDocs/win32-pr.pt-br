---
description: Contém a resposta a uma \_ consulta outputid D3DAUTHENTICATEDQUERY.
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9861de1dc97a606821060fcb7665cac557a08c084271c319c3804740169af7d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600776"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a>Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYROUTPUTID \_

Contém a resposta a uma [**consulta \_ outputid D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputid.md) .

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Saída de consulta D3DAUTHENTICATEDCHANNEL \_**
</dt> <dd>

Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Um identificador para o dispositivo.

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

Um identificador para a sessão de criptografia.

</dd> <dt>

**OutputIDIndex**
</dt> <dd>

O índice da ID de saída fornecida no membro **outputid** .

</dd> <dt>

**Outputid**
</dt> <dd>

Uma ID de saída associada ao dispositivo especificado e à sessão criptográfica.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de vídeo do Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




