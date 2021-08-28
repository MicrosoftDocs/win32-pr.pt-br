---
title: Propriedade PortableSalt IMsTscNonScriptable
description: Esta propriedade não é mais suportada.
ms.assetid: 1f123ec8-27b6-4637-9c57-fe32a224be8a
ms.tgt_platform: multiple
keywords:
- Propriedade PortableSalt Serviços de Área de Trabalho Remota
- A propriedade PortableSalt Serviços de Área de Trabalho Remota , interface IMsTscNonScriptable
- Interface IMsTscNonScriptable Serviços de Área de Trabalho Remota , propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota objeto , MsTscAx
- Objeto MsTscAx Serviços de Área de Trabalho Remota , propriedade PortableSalt
- A propriedade PortableSalt Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable
- Interface IMsRdpClientNonScriptable Serviços de Área de Trabalho Remota , propriedade PortableSalt
- A propriedade PortableSalt Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable2
- Interface IMsRdpClientNonScriptable2 Serviços de Área de Trabalho Remota , propriedade PortableSalt
- A propriedade PortableSalt Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable3
- Interface IMsRdpClientNonScriptable3 Serviços de Área de Trabalho Remota , propriedade PortableSalt
- A propriedade PortableSalt Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable4
- Interface IMsRdpClientNonScriptable4 Serviços de Área de Trabalho Remota , propriedade PortableSalt
- A propriedade PortableSalt Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable5
- Interface IMsRdpClientNonScriptable5 Serviços de Área de Trabalho Remota , propriedade PortableSalt
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortableSalt
- IMsTscNonScriptable.get_PortableSalt
- IMsTscNonScriptable.put_PortableSalt
- MsTscAx.PortableSalt
- IMsRdpClientNonScriptable.PortableSalt
- IMsRdpClientNonScriptable.get_PortableSalt
- IMsRdpClientNonScriptable.put_PortableSalt
- IMsRdpClientNonScriptable2.PortableSalt
- IMsRdpClientNonScriptable2.get_PortableSalt
- IMsRdpClientNonScriptable2.put_PortableSalt
- IMsRdpClientNonScriptable3.PortableSalt
- IMsRdpClientNonScriptable3.get_PortableSalt
- IMsRdpClientNonScriptable3.put_PortableSalt
- IMsRdpClientNonScriptable4.PortableSalt
- IMsRdpClientNonScriptable4.get_PortableSalt
- IMsRdpClientNonScriptable4.put_PortableSalt
- IMsRdpClientNonScriptable5.PortableSalt
- IMsRdpClientNonScriptable5.get_PortableSalt
- IMsRdpClientNonScriptable5.put_PortableSalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724f9b394d6e70354b39036df90386a823da2e5874f9ecb0fc0b81f130e3571e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125036"
---
# <a name="imstscnonscriptableportablesalt-property"></a>Propriedade IMsTscNonScriptable::P ortableSalt

Esta propriedade não é mais suportada.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PortableSalt(
  [in]  BSTR newPortableSalt
);

HRESULT get_PortableSalt(
  [out] BSTR *pPortableSalt
);
```



## <a name="property-value"></a>Valor da propriedade

A nova parte de sal portátil para uma senha codificada portátil.

## <a name="error-codes"></a>Códigos do Erro

Retorna **E \_ NOTIMPL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Fim do suporte ao cliente<br/>    | Nenhum compatível<br/>                                                              |
| Fim do suporte ao servidor<br/>    | Nenhum compatível<br/>                                                              |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable é definido como c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**Imstscnonscriptable**](imstscnonscriptable-interface.md)
</dt> <dt>

[**PortablePassword**](imstscnonscriptable-portablepassword.md)
</dt> </dl>

 

 





