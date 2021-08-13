---
description: Define o nível de criptografia que é executado antes que o conteúdo protegido se torne acessível à CPU ou ao barramento.
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: f785931cf70ae48082cb45c436dd1c50b7c329fef61619738a3ef0a08240d7b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742643"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a>D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE

Define o nível de criptografia que é executado antes que o conteúdo protegido se torne acessível à CPU ou ao barramento.



| Requisito | Valor |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| GUID de comando | **D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**                                                                     |
| Dados de entrada   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

## <a name="remarks"></a>Comentários

Os seguintes tipos de canal dão suporte a esta consulta:

-   **\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**
-   **\_Software de driver D3DAUTHENTICATEDCHANNEL \_**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Comandos de Proteção de Conteúdo](content-protection-commands.md)
</dt> <dt>

[Proteção de Conteúdo baseado em GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: configurar**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




