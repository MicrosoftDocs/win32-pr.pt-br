---
title: Mensagem de CQPM_ENABLE (Cmnquery. h)
description: Enviado para a função de retorno de chamada CQPageProc de uma página de extensão de formulário de consulta para habilitar ou desabilitar a página.
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_ENABLE Active Directory
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0252c5e1ec7fd9633241416fbf01bb4ead52c45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009007"
---
# <a name="cqpm_enable-message"></a>CQPM \_ habilitar mensagem

A mensagem de **\_ habilitação CQPM** é enviada para a função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de uma página de extensão de formulário de consulta para habilitar ou desabilitar a página.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém zero para desabilitar a página ou diferente de zero para habilitar a página.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno para essa mensagem é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





