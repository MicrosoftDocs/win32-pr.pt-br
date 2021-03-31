---
title: Propriedade IMsTscNonScriptable PortableSalt
description: Esta propriedade não é mais suportada.
ms.assetid: 1f123ec8-27b6-4637-9c57-fe32a224be8a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsTscNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsTscNonScriptable, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, objeto MsTscAx
- Objeto MsTscAx Serviços de Área de Trabalho Remota, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade PortableSalt
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
ms.openlocfilehash: 0162073b8361cc89f7ab2e33f60406c0db935bdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644871"
---
# <a name="imstscnonscriptableportablesalt-property"></a>IMsTscNonScriptable: Propriedade ortableSalt de:P

Esta propriedade não é mais suportada.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_PortableSalt(
  [in]  BSTR newPortableSalt
);

HRESULT get_PortableSalt(
  [out] BSTR *pPortableSalt
);
```



## <a name="property-value"></a>Valor da propriedade

A nova parte de Salt portátil para uma senha codificada portátil.

## <a name="error-codes"></a>Códigos do Erro

Retorna **E \_ NOTIMPL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Fim do suporte do cliente<br/>    | Nenhum compatível<br/>                                                              |
| Fim do suporte do servidor<br/>    | Nenhum compatível<br/>                                                              |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable é definido como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Consulte também

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

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> <dt>

[**PortablePassword**](imstscnonscriptable-portablepassword.md)
</dt> </dl>

 

 





