---
description: Retorna os handles para a sessão criptográfica e o dispositivo Direct3D associados a um dispositivo decodificador DXVA-2 (Aceleração de Vídeo DirectX 2) especificado.
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 3ee1cabc69122ebd7eb7d81c64eb761439e6a3c0cde20dd376c3581b9aed0738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974665"
---
# <a name="d3dauthenticatedquery_cryptosession"></a>D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION

Retorna os handles para a sessão criptográfica e o dispositivo Direct3D associados a um dispositivo decodificador DXVA-2 (Aceleração de Vídeo DirectX 2) especificado.



| Requisito | Valor |
|-------------|------------------------------------------------------------------------------------------------------------------|
| GUID de Consulta  | **D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**                                                                         |
| Dados de entrada  | [**ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                             |
| Retornar dados | [**SAÍDA D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_**](d3dauthenticatedchannel-querycryptosession-output.md) |



 

## <a name="remarks"></a>Comentários

Os seguintes tipos de canal são suportados por esta consulta:

-   **HARDWARE DO DRIVER D3DAUTHENTICATEDCHANNEL \_ \_**
-   **SOFTWARE DO DRIVER D3DAUTHENTICATEDCHANNEL \_ \_**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Proteção de Conteúdo consultas](content-protection-queries.md)
</dt> <dt>

[Dados baseados em GPU Proteção de Conteúdo](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




