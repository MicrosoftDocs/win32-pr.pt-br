---
description: 'Contém a resposta do método IDirect3DAuthenticatedChannel9:: Query.'
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089764"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a>Estrutura de saída da \_ consulta D3DAUTHENTICATEDCHANNEL \_

Contém a resposta do método [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**omac**
</dt> <dd>

Uma [**estrutura \_ OMAC do D3D**](d3d-omac.md) que contém um Message Authentication Code (Mac) dos dados. O driver usa o MAC de CBC One-key baseado em AES (OMAC) para calcular esse valor para o bloco de dados que aparece após esse membro da estrutura.

</dd> <dt>

**QueryType**
</dt> <dd>

Um GUID que especifica a consulta. Para obter uma lista de valores, consulte [proteção de conteúdo consultas](content-protection-queries.md).

</dd> <dt>

**PROCESSAMENTO**
</dt> <dd>

Um identificador para o canal autenticado.

</dd> <dt>

**UINT**
</dt> <dd>

O número de sequência da consulta.

</dd> <dt>

**ReturnCode**
</dt> <dd>

O código de resultado da consulta.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para os membros **QueryType**, **hChannel** e **SequenceNumber** , o driver usa os mesmos valores que o aplicativo forneceu na estrutura de [**\_ \_ entrada de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) . O aplicativo deve verificar se esses valores correspondem.

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

 

 




