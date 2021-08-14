---
title: Propriedade RedirectionState de IMsRdpDrive
description: Indica o estado de redirecionamento da unidade.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- Propriedade RedirectionState Serviços de Área de Trabalho Remota
- Propriedade RedirectionState Serviços de Área de Trabalho Remota , interface IMsRdpDrive
- Interface IMsRdpDrive Serviços de Área de Trabalho Remota propriedade , RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6069ec911210fac3f4334bdf9e84da080e5536a4f4b6cfc7aca0e54fe0bd2228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351951"
---
# <a name="imsrdpdriveredirectionstate-property"></a>Propriedade IMsRdpDrive::RedirectionState

Indica o estado de redirecionamento da unidade.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a>Valor da propriedade

De definir esse parâmetro como **VARIANT \_ FALSE.** para desabilitar o redirecionamento ou **VARIANT \_ TRUE.** para habilitar o redirecionamento.

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem-sucedido, **S \_ OK** será retornado. Qualquer outro **valor HRESULT** indica que a chamada falhou.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpDrive é definido como \_ d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

 





