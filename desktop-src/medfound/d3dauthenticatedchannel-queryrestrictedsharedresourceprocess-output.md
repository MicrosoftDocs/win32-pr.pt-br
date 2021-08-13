---
description: Contém a resposta a uma \_ consulta D3DAUTHENTICATEDQUERY RESTRICTEDSHAREDRESOURCEPROCESS.
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a8a9f3f916dff486be01584d98bef59aa3bda4851d41e2b03f8f86819be28ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742912"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output-structure"></a>Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_

Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT          Output;
  UINT                                          ProcessIndex;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentifer;
  HANDLE                                        ProcessHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Saída**
</dt> <dd>

Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.

</dd> <dt>

**ProcessIndex**
</dt> <dd>

O índice do processo na lista de processos.

</dd> <dt>

**ProcessIdentifer**
</dt> <dd>

Um valor de [**\_ PROCESSIDENTIFIERTYPE D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-processidentifiertype.md) que especifica o tipo de processo.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Um identificador de processo. Se o membro **ProcessIdentifier** for igual ao **\_ identificador processidtype**, o membro **ProcessHandle** conterá um identificador válido para um processo. Caso contrário, esse membro será ignorado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O processo de Gerenciador de Janelas da Área de Trabalho (DWM) é identificado pela definição de **ProcessIdentifier** igual a **processidtype \_ DWM**. Outros processos são identificados definindo o identificador de processo em **ProcessHandle** e definindo **ProcessIdentifier** igual ao **\_ identificador processidtype**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de vídeo do Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




