---
description: Retorna um alça para o dispositivo associado a esse canal autenticado.
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types.h)
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
ms.openlocfilehash: fd2af1a889cb4a51ebd278ce7aba0154a96b1f5537ea971ab6ce11828baaa1b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974655"
---
# <a name="d3dauthenticatedquery_devicehandle"></a>D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE

Retorna um alça para o dispositivo associado a esse canal autenticado. Você pode usar esse alça para verificar se dois canais autenticados estão se comunicando com o mesmo dispositivo.



| Requisito | Valor |
|-------------|----------------------------------------------------------------------------------------------------------------|
| GUID de Consulta  | **D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**                                                                        |
| Dados de entrada  | [**ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                           |
| Retornar dados | [**SAÍDA D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_**](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a>Comentários

Essa consulta é válida para todos os tipos de canal.

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

 

 




