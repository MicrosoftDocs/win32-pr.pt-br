---
description: Retorna um identificador para o dispositivo que está associado a este canal autenticado.
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3ebf54530a4ae029a52632eb5bb5afc51b5f152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761165"
---
# <a name="d3dauthenticatedquery_devicehandle"></a>D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE

Retorna um identificador para o dispositivo que está associado a este canal autenticado. Você pode usar esse identificador para verificar se dois canais autenticados estão se comunicando com o mesmo dispositivo.



| Requisito | Valor |
|-------------|----------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**                                                                        |
| Dados de entrada  | [**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)                           |
| Retornar dados | [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYDEVICEHANDLE \_**](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a>Comentários

Esta consulta é válida para todos os tipos de canal.

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

 

 




