---
description: Retorna o número de recursos compartilhados protegidos que podem ser abertos por qualquer processo sem restrições.
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a227d8aa23e7f070cebb1c73092bd0af170927eda582e417839375512e891df7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879740"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a>D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT

Retorna o número de recursos compartilhados protegidos que podem ser abertos por qualquer processo sem restrições.



| Requisito | Valor |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de Consulta  | **D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**                                                                                                    |
| Dados de entrada  | [**ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                                                                                   |
| Retornar dados | [**D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_ OUTPUT**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a>Comentários

O único tipo de canal que dá suporte a essa consulta é **D3DAUTHENTICATEDCHANNEL \_ DRIVER \_ SOFTWARE**.

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

 

 




