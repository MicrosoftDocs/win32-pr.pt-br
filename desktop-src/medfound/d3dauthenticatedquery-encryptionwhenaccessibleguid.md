---
description: Retorna um dos tipos de criptografia que podem ser usados para criptografar o conteúdo antes que ele se torne acessível à CPU ou ao barramento.
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b5755a2707ec9d7440cda9b4692eed36ac6deff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770573"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a>D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID

Retorna um dos tipos de criptografia que podem ser usados para criptografar o conteúdo antes que ele se torne acessível à CPU ou ao barramento.



| Requisito | Valor |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**                                                                            |
| Dados de entrada  | [**\_Entrada D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID \_**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| Retornar dados | [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID \_**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

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

 

 




