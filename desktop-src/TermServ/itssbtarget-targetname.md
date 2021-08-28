---
title: Propriedade TargetName ITsSbTarget
description: Especifica ou recupera o nome do destino.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Propriedade TargetName Serviços de Área de Trabalho Remota
- A propriedade TargetName Serviços de Área de Trabalho Remota interface , ITsSbTarget
- Interface ITsSbTarget Serviços de Área de Trabalho Remota propriedade , TargetName
- A propriedade TargetName Serviços de Área de Trabalho Remota interface , ITsSbTargetEx
- Interface ITsSbTargetEx Serviços de Área de Trabalho Remota , propriedade TargetName
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
ms.openlocfilehash: 7da653b581c512e0397bb4c486d7c21d6844d41b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982589"
---
# <a name="itssbtargettargetname-property"></a>Propriedade ITsSbTarget::TargetName

Especifica ou recupera o nome do destino.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

Uma **variável BSTR** que especifica o nome de destino.

## <a name="remarks"></a>Comentários

Essa propriedade era somente leitura antes Windows Server 2012.

## <a name="requirements"></a>Requisitos




| Requisito | Valor |
|--------|-------|
| Cliente mínimo com suporte<br /> | Nenhum compatível<br /> | 
| Servidor mínimo com suporte<br /> | Windows Server 2012<br /> | 
| IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget é definido como:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 no Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Consulte também

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





