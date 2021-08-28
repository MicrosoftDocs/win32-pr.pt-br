---
title: Propriedade Farmname de ITsSbTarget
description: Recupera ou especifica o nome do farm ao qual esse destino está associado.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- Propriedade farmname Serviços de Área de Trabalho Remota
- Propriedade farmname Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Serviços de Área de Trabalho Remota de interface ITsSbTarget, Propriedade Farmname
- Propriedade farmname Serviços de Área de Trabalho Remota, interface ITsSbTargetEx
- Serviços de Área de Trabalho Remota de interface ITsSbTargetEx, Propriedade Farmname
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b1c36a1a44f38dac11a7e474d7fefb80a09948
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988289"
---
# <a name="itssbtargetfarmname-property"></a>Propriedade ITsSbTarget:: Farmname

Recupera ou especifica o nome do farm ao qual esse destino está associado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

Uma variável **BSTR** que contém o nome do farm.

## <a name="requirements"></a>Requisitos




| Requisito | Valor |
|--------|-------|
| Cliente mínimo com suporte<br /> | Nenhum compatível<br /> | 
| Servidor mínimo com suporte<br /> | Windows Server 2012<br /> | 
| INSERI<br /> | <dl><dt>Sbtsv. idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget é definido como:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 no servidor Windows 2008 R2</li></ul> | 




## <a name="see-also"></a>Consulte também

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





