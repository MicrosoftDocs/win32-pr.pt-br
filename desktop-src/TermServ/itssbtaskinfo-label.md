---
title: Propriedade rótulo ITsSbTaskInfo
description: Recupera o rótulo que descreve a finalidade da tarefa.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- Rótulo da propriedade Serviços de Área de Trabalho Remota
- A propriedade label Serviços de Área de Trabalho Remota , interface ITsSbTaskInfo
- Interface ITsSbTaskInfo Serviços de Área de Trabalho Remota , propriedade Label
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2414dd83d44add4084a4176f575817875e933f9770039e49b02364bd8103cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138299"
---
# <a name="itssbtaskinfolabel-property"></a>Propriedade ITsSbTaskInfo::Label

Recupera o rótulo que descreve a finalidade da tarefa.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um **valor BSTR** que contém o rótulo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





