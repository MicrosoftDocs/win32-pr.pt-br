---
description: Contém dados de entrada para um comando D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION.
ms.assetid: eed5591d-20b0-495c-8c05-b9cb3b91deab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: bfb65687eaae82b11e670653d625e0f6ffa36c1d091a3c049829e5a221507556
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942908"
---
# <a name="d3dauthenticatedchannel_configurecryptosession-structure"></a>Estrutura D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION

Contém dados de entrada para [**um comando D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION.**](d3dauthenticatedconfigure-cryptosession.md)

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  HANDLE                                  DXVA2DecodeHandle;
  HANDLE                                  CryptoSessionHandle;
  HANDLE                                  DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION;
```



## <a name="members"></a>Membros

<dl> <dt>

**Parâmetros**
</dt> <dd>

Uma [**estrutura D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT**](d3dauthenticatedchannel-configure-input.md) que contém o GUID do comando e outros dados.

</dd> <dt>

**DXVA2DecodeHandle**
</dt> <dd>

Um handle para o dispositivo decodificador DXVA-2 (Aceleração de Vídeo DirectX 2).

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

Um alça para a sessão criptográfica.

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Um alça para o dispositivo Direct3D.

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

 

 




