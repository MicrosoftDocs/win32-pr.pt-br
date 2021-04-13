---
title: Propriedade IVMHostInfo ProcessorSpeedString (VPCCOMInterfaces. h)
description: Velocidade do processador do host, em megahertz (MHz) ou gigahertz (GHz), como uma cadeia de caracteres.
ms.assetid: 1a4a42bf-b7aa-4eec-8df5-1820aac82de3
keywords:
- Propriedade ProcessorSpeedString Virtual PC
- Propriedade ProcessorSpeedString Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade ProcessorSpeedString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorSpeedString
- IVMHostInfo.get_ProcessorSpeedString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b8cb19baef62275954f0c1d9f6475c5b4817f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455841"
---
# <a name="ivmhostinfoprocessorspeedstring-property"></a>IVMHostInfo: Propriedade rocessorSpeedString de:P

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a velocidade do processador do host, em megahertz (MHz) ou gigahertz (GHz), como uma cadeia de caracteres.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ProcessorSpeedString(
  [out, retval] BSTR *processorSpeedString
);
```



## <a name="property-value"></a>Valor da propriedade

A velocidade do processador, em megahertz ou gigahertz.

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

 

