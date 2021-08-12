---
title: Propriedade RedirectionState de IMsRdpDevice
description: Indica o estado de redirecionamento do dispositivo.
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- Propriedade RedirectionState Serviços de Área de Trabalho Remota
- A propriedade RedirectionState Serviços de Área de Trabalho Remota , interface IMsRdpDevice
- Interface IMsRdpDevice Serviços de Área de Trabalho Remota , propriedade RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDevice.RedirectionState
- IMsRdpDevice.get_RedirectionState
- IMsRdpDevice.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8609c682a7a31d293e6e8a9606c8ae445b0487da0d95399fb4e00d779914bfd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606678"
---
# <a name="imsrdpdeviceredirectionstate-property"></a>Propriedade IMsRdpDevice::RedirectionState

Indica o estado de redirecionamento do dispositivo.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a>Valor da propriedade

De definir esse parâmetro como **VARIANT \_ FALSE** para desabilitar o redirecionamento **ou VARIANT \_ TRUE** para habilitar o redirecionamento.

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem-sucedido, **S \_ OK** será retornado. Qualquer outro **valor HRESULT** indica que a chamada falhou.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice é definido como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

 





