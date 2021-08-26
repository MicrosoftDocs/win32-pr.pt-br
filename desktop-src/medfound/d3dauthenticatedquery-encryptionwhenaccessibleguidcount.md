---
description: Retorna o número de tipos de criptografia que podem ser usados para criptografar conteúdo antes que ele se torne acessível para a CPU ou o barramento.
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: f47074947cc2f758d35691e05dda9b39f2f823feb6d647a7d77c0a3cc0030c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942756"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a>D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT

Retorna o número de tipos de criptografia que podem ser usados para criptografar conteúdo antes que ele se torne acessível para a CPU ou o barramento.



| Requisito | Valor |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de Consulta  | **D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**                                                                                 |
| Dados de entrada  | [**ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                                                         |
| Retornar dados | [**D3DAUTHENTICATEDCHANNEL \_ QUERBUGICTIONENCRYPTIONGUIDCOUNT \_ OUTPUT**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

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

 

 




