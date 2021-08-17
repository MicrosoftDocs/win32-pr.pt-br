---
title: Propriedade IMsRdpClientNonScriptable5 DisableConnectionBar
description: Especifica se o controle Área de Trabalho Remota ActiveX deve desabilitar a barra de conexão.
ms.assetid: 82c57b93-f976-43e6-97f9-3602bf97e466
ms.tgt_platform: multiple
keywords:
- Propriedade DisableConnectionBar Serviços de Área de Trabalho Remota
- A propriedade DisableConnectionBar Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable5
- Interface IMsRdpClientNonScriptable5 Serviços de Área de Trabalho Remota propriedade DisableConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableConnectionBar
- IMsRdpClientNonScriptable5.put_DisableConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f74fce650eb82514538eed7066b937c29f8618aba1eab7531f3bdb7e1127da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138739"
---
# <a name="imsrdpclientnonscriptable5disableconnectionbar-property"></a>Propriedade IMsRdpClientNonScriptable5::D isableConnectionBar

Especifica se o controle Área de Trabalho Remota ActiveX deve desabilitar a barra de conexão. Se essa propriedade **contiver VARIANT \_ TRUE**, a barra de conexão deverá ser desabilitada. Se essa propriedade **contiver VARIANT \_ FALSE**, a barra de conexão deverá ser habilitada.

Essa propriedade é somente gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DisableConnectionBar(
  [in] VARIANT_BOOL fDisableConnectionBar
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica o novo valor da propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 é definido como 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





