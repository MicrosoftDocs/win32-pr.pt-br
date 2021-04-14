---
description: Retorna o tipo de barramento de e/s usado para enviar dados para a GPU.
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types. h)
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
ms.openlocfilehash: 5119da4e7efaf0c27db1065dacc56e3388a77474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370532"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a>\_Acessibilidade D3DAUTHENTICATEDQUERY

Retorna o tipo de barramento de e/s usado para enviar dados para a GPU.



| Requisito | Valor |
|-------------|--------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **\_Acessibilidade D3DAUTHENTICATEDQUERY**                                                           |
| Dados de entrada  | [**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)                         |
| Retornar dados | [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYINFOBUSTYPE \_**](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a>Comentários

Essa consulta também retorna informações sobre como o conteúdo é acessível quando colocado na memória de vídeo.

Os seguintes tipos de canal dão suporte a esta consulta:

-   **\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**
-   **\_Software de driver D3DAUTHENTICATEDCHANNEL \_**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Consultas de Proteção de Conteúdo](content-protection-queries.md)
</dt> <dt>

[Proteção de Conteúdo baseado em GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




