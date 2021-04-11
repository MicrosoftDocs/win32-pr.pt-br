---
description: Contém dados de entrada para um \_ comando de inicialização D3DAUTHENTICATEDCONFIGURE.
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
title: Estrutura de D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 072d7886a024b1c28e8c3b7f0609dc8dd3e6add8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010319"
---
# <a name="d3dauthenticatedchannel_configureinitialize-structure"></a>\_Estrutura D3DAUTHENTICATEDCHANNEL CONFIGUREINITIALIZE

Contém dados de entrada para um comando de [**\_ inicialização D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-initialize.md) .

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  UINT                                    StartSequenceQuery;
  UINT                                    StartSequenceConfigure;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Parâmetros**
</dt> <dd>

Um [**D3DAUTHENTICATEDCHANNEL \_ configura \_**](d3dauthenticatedchannel-configure-input.md) a estrutura de entrada que contém o GUID de comando e outros dados.

</dd> <dt>

**StartSequenceQuery**
</dt> <dd>

O número de sequência inicial para consultas.

</dd> <dt>

**StartSequenceConfigure**
</dt> <dd>

O número de sequência inicial para comandos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros **StartSequenceQuery** e **StartSequenceConfigure** contêm um número aleatório de 32 bits de segurança criptograficamente seguro.

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

[**IDirect3DAuthenticatedChannel9:: configurar**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




