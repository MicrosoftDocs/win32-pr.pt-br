---
title: Propriedade SSE2 IVMHostInfo (VPCCOMInterfaces. h)
description: Determina se o processador dá suporte ao conjunto de instruções SSE2. | Propriedade SSE2 IVMHostInfo (VPCCOMInterfaces. h)
ms.assetid: 1db5583c-fb8e-400e-87d3-3c4309696307
keywords:
- Propriedade SSE2 do Virtual PC
- Propriedade SSE2 Virtual PC, interface IVMHostInfo
- Virtual PC interface IVMHostInfo, Propriedade SSE2
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE2
- IVMHostInfo.get_SSE2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28286262d02512f58df8c3a00e4ba07a67c2916f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837855"
---
# <a name="ivmhostinfosse2-property"></a>Propriedade IVMHostInfo:: SSE2

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se o processador dá suporte ao conjunto de instruções SSE2.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SSE2(
  [out, retval] VARIANT_BOOL *sse2Enabled
);
```



## <a name="property-value"></a>Valor da propriedade

**True** se as instruções SSE2 forem suportadas pelo processador do host; caso contrário, **false** .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>        |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

