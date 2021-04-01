---
title: Propriedade do identificador ITsSbTaskInfo
description: Recupera um GUID que é usado como um identificador exclusivo pelo agente de tarefa.
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de Propriedade do identificador
- Serviços de Área de Trabalho Remota de Propriedade do identificador, interface ITsSbTaskInfo
- Serviços de Área de Trabalho Remota de interface ITsSbTaskInfo, Propriedade do identificador
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 241ed2966e9ec92aa420af20ce142bcb724ad222
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645184"
---
# <a name="itssbtaskinfoidentifier-property"></a>Propriedade ITsSbTaskInfo:: Identifier

Recupera um GUID que é usado como um identificador exclusivo pelo agente de tarefa.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um valor **BSTR** que recebe o GUID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| INSERI<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





