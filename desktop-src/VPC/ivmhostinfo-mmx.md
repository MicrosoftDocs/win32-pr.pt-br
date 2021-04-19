---
title: Propriedade MMX IVMHostInfo (VPCCOMInterfaces. h)
description: Determina se o processador dá suporte ao conjunto de instruções MMX. | Propriedade MMX IVMHostInfo (VPCCOMInterfaces. h)
ms.assetid: 2f556289-c752-4af2-a6d0-abb6e717e609
keywords:
- PC virtual da propriedade MMX
- Propriedade MMX Virtual PC, interface IVMHostInfo
- Virtual PC de interface IVMHostInfo, Propriedade MMX
topic_type:
- apiref
api_name:
- IVMHostInfo.MMX
- IVMHostInfo.get_MMX
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e224ed6a0f15da9143a884dd1c1dfacc1634fce7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105784985"
---
# <a name="ivmhostinfommx-property"></a>Propriedade IVMHostInfo:: MMX

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se o processador dá suporte ao conjunto de instruções MMX.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MMX(
  [out, retval] VARIANT_BOOL *mmxEnabled
);
```



## <a name="property-value"></a>Valor da propriedade

**True** se houver suporte para instruções MMX; caso contrário, **false** .

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

 

