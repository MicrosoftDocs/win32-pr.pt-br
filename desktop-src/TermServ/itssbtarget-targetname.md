---
title: Propriedade TargetName ITsSbTarget
description: Especifica ou recupera o nome do destino.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TargetName
- Propriedade TargetName Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Serviços de Área de Trabalho Remota de interface ITsSbTarget, Propriedade TargetName
- Propriedade TargetName Serviços de Área de Trabalho Remota, interface ITsSbTargetEx
- Serviços de Área de Trabalho Remota de interface ITsSbTargetEx, Propriedade TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971ae66d162464c49d7eb4206f1fbddf206707c2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467863"
---
# <a name="itssbtargettargetname-property"></a>Propriedade ITsSbTarget:: TargetName

Especifica ou recupera o nome do destino.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

Uma variável **BSTR** que especifica o nome de destino.

## <a name="remarks"></a>Comentários

Esta propriedade era somente leitura antes de Windows Server 2012.

## <a name="requirements"></a>Requisitos




| | | Mínimo de cliente com suporte<br /> | Nenhum com suporte<br /> | | Mínimo de servidor com suporte<br /> | Windows Server 2012<br /> | | INSERI<br /> | <dl><dt>Sbtsv. idl</dt></dl> | | IID<br /> | IID_ITsSbTarget é definido como:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 no servidor Windows 2008 R2</li></ul> | 




## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





