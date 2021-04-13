---
title: Propriedade IVMHostInfo MemoryTotalString (VPCCOMInterfaces. h)
description: Recupera a quantidade total de memória física no computador host, em megabytes, como uma cadeia de caracteres.
ms.assetid: 732c62e5-2776-4551-909f-7ddab74e067d
keywords:
- Propriedade MemoryTotalString Virtual PC
- Propriedade MemoryTotalString Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade MemoryTotalString
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryTotalString
- IVMHostInfo.get_MemoryTotalString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e6c16a4215aba141ff1803d340c63dc9faa868
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369690"
---
# <a name="ivmhostinfomemorytotalstring-property"></a>Propriedade IVMHostInfo:: MemoryTotalString

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a quantidade total de memória física no computador host, em megabytes, como uma cadeia de caracteres.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MemoryTotalString(
  [out, retval] BSTR *megabytesOfMemory
);
```



## <a name="property-value"></a>Valor da propriedade

A quantidade total de memória física, em megabytes.

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

 

