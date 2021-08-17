---
description: Associa uma sessão criptográfica a um dispositivo decodificador do DirectX Video Acceleration 2 (DXVA-2) e a um dispositivo Direct3D.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 3e1df4b58750d5b2d82eb518d5dfc0ef24bdbe4e5569ebcaf708b8df60691d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449436"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a>D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION

Associa uma sessão criptográfica a um dispositivo decodificador do DirectX Video Acceleration 2 (DXVA-2) e a um dispositivo Direct3D.



| Requisito | Valor |
|--------------|-----------------------------------------------------------------------------------------------------------|
| GUID de comando | **D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**                                                              |
| Dados de entrada   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a>Comentários

Depois que esse comando for enviado, você poderá enviar a consulta [D3DAUTHENTICATEDQUERY \_ outputid](d3dauthenticatedquery-outputid.md) para descobrir quais saídas de vídeo estão associadas à sessão criptográfica.

Os seguintes tipos de canal dão suporte a este comando:

-   **D3DAUTHENTICATEDCHANNEL \_ d3d9**
-   **\_Software de driver D3DAUTHENTICATEDCHANNEL \_**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Comandos de Proteção de Conteúdo](content-protection-commands.md)
</dt> <dt>

[Proteção de Conteúdo baseado em GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: configurar**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




