---
description: Contém dados de entrada para um comando D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE estrutura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 0dbff67921f2ec6ad634c20b11b86b0384923db5548bcef113128fe5ede6bdd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742902"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a>Estrutura D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE

Contém dados de entrada para [**um comando D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE.**](d3dauthenticatedconfigure-sharedresource.md)

Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Parâmetros**
</dt> <dd>

Uma [**estrutura D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT**](d3dauthenticatedchannel-configure-input.md) que contém o GUID do comando e outros dados.

</dd> <dt>

**ProcessIdentiferType**
</dt> <dd>

Um [**valor D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) que especifica o tipo de processo. Para especificar o processo Gerenciador de Janelas da Área de Trabalho (DWM), de definir esse membro como **PROCESSIDTYPE \_ DWM.** Caso contrário, de definir esse membro **como PROCESSIDTYPE \_ HANDLE** e de definir o **membro ProcessHandle** como um handle válido.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Um alça de processo. Se o **membro ProcessIdentifier** for igual a **PROCESSTIDTYPE \_ HANDLE,** o membro **ProcessHandle** especificará um identificador para um processo. Caso contrário, o valor será ignorado.

</dd> <dt>

**AllowAccess**
</dt> <dd>

Se **TRUE**, o processo especificado terá acesso a recursos compartilhados restritos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de vídeo do Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




