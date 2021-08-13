---
description: Retorna o tipo de criptografia que é aplicado antes que o conteúdo se torne acessível à CPU ou ao barramento.
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 483058e8b76b7a08929e905b642338c9e8f6aa6a59128907bccfcc1f2b3856f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742616"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a>D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE

Retorna o tipo de criptografia que é aplicado antes que o conteúdo se torne acessível à CPU ou ao barramento.



| Requisito | Valor |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**                                                                                   |
| Dados de entrada  | [**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)                                                         |
| Retornar dados | [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

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

[Consultas de Proteção de Conteúdo](content-protection-queries.md)
</dt> <dt>

[Proteção de Conteúdo baseado em GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




