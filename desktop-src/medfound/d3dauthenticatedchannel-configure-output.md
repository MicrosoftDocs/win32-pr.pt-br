---
description: 'Contém a resposta a uma chamada para o método IDirect3DAuthenticatedChannel9:: Configure.'
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: Estrutura de D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a849967e798db0ae0364e843221bfe2bf0f3305f773a784b6330a21bb84e5427
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942926"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ Configurar a \_ estrutura de saída

Contém a resposta a uma chamada para o método [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**omac**
</dt> <dd>

Uma [**estrutura \_ OMAC do D3D**](d3d-omac.md) que contém um Message Authentication Code (Mac) dos dados. O driver usa o MAC de CBC One-key baseado em AES (OMAC) para calcular esse valor para o bloco de dados que aparece após esse membro da estrutura.

</dd> <dt>

**Configuratype**
</dt> <dd>

Um GUID que especifica o comando. Para obter uma lista de valores, consulte [proteção de conteúdo comandos](content-protection-commands.md).

</dd> <dt>

**hChannel**
</dt> <dd>

Um identificador para o canal autenticado.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

O número de sequência do comando.

</dd> <dt>

**ReturnCode**
</dt> <dd>

O código de resultado do comando.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para os membros **configuratype**, **hChannel** e **SequenceNumber** , o driver usa os mesmos valores que o aplicativo fornecido no D3DAUTHENTICATEDCHANNEL configurar a estrutura de [**\_ \_ entrada**](d3dauthenticatedchannel-configure-input.md) . O aplicativo deve verificar se esses valores correspondem.

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

[**IDirect3DAuthenticatedChannel9:: configurar**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




