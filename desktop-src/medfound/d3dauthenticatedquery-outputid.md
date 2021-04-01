---
description: Retorna um dos identificadores de saída associados a uma sessão criptográfica especificada e ao dispositivo Direct3D.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646598"
---
# <a name="d3dauthenticatedquery_outputid"></a>Saída de D3DAUTHENTICATEDQUERY \_

Retorna um dos identificadores de saída associados a uma sessão criptográfica especificada e ao dispositivo Direct3D.



| Requisito | Valor |
|-------------|--------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **Saída de D3DAUTHENTICATEDQUERY \_**                                                                    |
| Dados de entrada  | [**\_Entrada D3DAUTHENTICATEDCHANNEL QUERYOUTPUTID \_**](d3dauthenticatedchannel-queryoutputid-input.md)   |
| Retornar dados | [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYOUTPUTID \_**](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a>Comentários

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

 

 




