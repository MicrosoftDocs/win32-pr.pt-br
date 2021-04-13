---
title: Propriedade de estado ITsSbSession
description: Recupera ou especifica o estado da sessão.
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de estado
- Serviços de Área de Trabalho Remota de propriedade de estado, interface ITsSbSession
- Serviços de Área de Trabalho Remota de interface ITsSbSession, propriedade State
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb939a518ab1050d932349cd70c85bcd22edf3d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455941"
---
# <a name="itssbsessionstate-property"></a>Propriedade ITsSbSession:: State

Recupera ou especifica o estado da sessão.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a>Valor da propriedade

Um valor da enumeração [**de \_ estado TSSESSION**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) que indica o estado de uma sessão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| INSERI<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[**\_estado TSSESSION**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





