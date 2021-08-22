---
description: Contém dados de entrada para um comando D3DAUTHENTICATEDCONFIGURE \_ PROTECTION.
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 3f7c202a29347d59bfaf79792806fcab56532637045985440c899eeae304a4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828766"
---
# <a name="d3dauthenticatedchannel_configureprotection-structure"></a>Estrutura D3DAUTHENTICATEDCHANNEL \_ CONFIGUREPROTECTION

Contém dados de entrada para um [**comando D3DAUTHENTICATEDCONFIGURE \_ PROTECTION.**](d3dauthenticatedconfigure-protection.md)

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT  Parameters;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS Protections;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION;
```



## <a name="members"></a>Membros

<dl> <dt>

**Parâmetros**
</dt> <dd>

Uma [**estrutura D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT**](d3dauthenticatedchannel-configure-input.md) que contém o GUID do comando e outros dados.

</dd> <dt>

**Proteções**
</dt> <dd>

Uma [**estrutura D3DAUTHENTICATEDCHANNEL \_ PROTECTION \_ FLAGS**](d3dauthenticatedchannel-protection-flags.md) que especifica o nível de proteção.

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

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




