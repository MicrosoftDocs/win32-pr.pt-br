---
description: Contém a resposta a uma \_ consulta accessibilityattributes do D3DAUTHENTICATEDQUERY.
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 853488c98687825ab55d642b2e01e569f0d435c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785967"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a>Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_

Contém a resposta a uma [**consulta \_ accessibilityattributes do D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-accessibilityattributes.md) .

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DBUSTYPE                           BusType;
  BOOL                                 bAccessibleInContiguousBlocks;
  BOOL                                 bAccessibleInNonContiguousBlocks;
} D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Saída**
</dt> <dd>

Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.

</dd> <dt>

**BusType**
</dt> <dd>

Um or de bit **ou** de sinalizadores da enumeração [**D3DBUSTYPE**](d3dbustype.md) .

</dd> <dt>

**bAccessibleInContiguousBlocks**
</dt> <dd>

Se **for verdadeiro**, blocos contíguos de memória de vídeo poderão ser acessíveis para a CPU ou para o barramento.

</dd> <dt>

**bAccessibleInNonContiguousBlocks**
</dt> <dd>

Se **for verdadeiro**, blocos não contíguos de memória de vídeo poderão estar acessíveis para a CPU ou para o barramento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de vídeo do Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




