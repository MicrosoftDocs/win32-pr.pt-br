---
description: 'Contém dados de entrada para o método IDirect3DAuthenticatedChannel9:: Configure.'
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: Estrutura de D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: de968c83fee7ae68dcd756bdf83d529593eeb30b3c2776b03cda812bcd442c50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974735"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ Configurar a \_ estrutura de entrada

Contém dados de entrada para o método [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
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

Um identificador para o canal autenticado. Para obter o identificador, chame [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).

</dd> <dt>

**SequenceNumber**
</dt> <dd>

O número de sequência da consulta. No início da sessão, gere um número aleatório de 32 bits de segurança criptograficamente seguro para usar como o número de sequência inicial. Para cada comando, aumente o número de sequência em 1.

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

[**IDirect3DAuthenticatedChannel9:: configurar**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




