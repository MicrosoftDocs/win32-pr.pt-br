---
description: Retorna o tipo de barramento de E/S usado para enviar dados para a GPU.
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9d7d4daaec3d52b7aabafe61c5763304c400b6a36be1367e01b0a9163f2f9e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828676"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a>D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES

Retorna o tipo de barramento de E/S usado para enviar dados para a GPU.



| Requisito | Valor |
|-------------|--------------------------------------------------------------------------------------------------------------|
| GUID de Consulta  | **D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**                                                           |
| Dados de entrada  | [**ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                         |
| Retornar dados | [**SAÍDA D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_**](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a>Comentários

Essa consulta também retorna informações sobre como o conteúdo é acessível quando colocado na memória de vídeo.

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

 

 




