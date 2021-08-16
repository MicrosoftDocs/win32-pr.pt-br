---
description: Contém dados de entrada para uma \_ consulta D3DAUTHENTICATEDQUERY RESTRICTEDSHAREDRESOURCEPROCESS.
ms.assetid: a1ceb394-7af9-4f05-9f58-a3103bf0150e
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 361b107b527fc1a4ecd37ee564dd440447a9233e55f9ae4027933a57fd715b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958756"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_input-structure"></a>Estrutura de entrada do D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_

Contém dados de entrada para uma consulta [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                ProcessIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Entrada**
</dt> <dd>

Uma estrutura de [**\_ \_ entrada de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) que contém o GUID para a consulta e outros dados.

</dd> <dt>

**ProcessIndex**
</dt> <dd>

O índice do processo.

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

 

 




