---
title: Propriedade TargetName ITsSbSession
description: Recupera o nome do destino no qual essa sessão foi criada.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Propriedade TargetName Serviços de Área de Trabalho Remota
- A propriedade TargetName Serviços de Área de Trabalho Remota interface , ITsSbSession
- Interface ITsSbSession Serviços de Área de Trabalho Remota propriedade , TargetName
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbc1e26aa4bf55a59b6405921d49e6b1aafa14e63a1e487caca9a7c036b1524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138309"
---
# <a name="itssbsessiontargetname-property"></a>Propriedade ITsSbSession::TargetName

Recupera o nome do destino no qual essa sessão foi criada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para uma **variável BSTR** que recebe o nome do destino no qual essa sessão foi criada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





