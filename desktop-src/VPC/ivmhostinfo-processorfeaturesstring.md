---
title: Propriedade IVMHostInfo ProcessorFeaturesString (VPCCOMInterfaces. h)
description: Recupera os recursos da lista com suporte pelo processador do host.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- Propriedade ProcessorFeaturesString Virtual PC
- Propriedade ProcessorFeaturesString Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade ProcessorFeaturesString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118aaa2eabe7ddb2fd608892775a17eac6a77d16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760797"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a>IVMHostInfo: Propriedade rocessorFeaturesString de:P

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera os recursos da lista com suporte pelo processador do host.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a>Valor da propriedade

Uma lista delimitada por vírgulas de recursos. Um exemplo seria "MMX, SSE, SSE2, x86-64".



| Valor                                                                                 | Significado                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>"AMD-V"</dt> </dl>    | Dá suporte às extensões de virtualização AMD.<br/>              |
| <dl> <dt>"Intel VT"</dt> </dl> | Dá suporte às extensões de tecnologia de virtualização da Intel.<br/> |
| <dl> <dt>"HAVD"</dt> </dl>     | A virtualização assistida por hardware está desabilitada.<br/>            |
| <dl> <dt>TER</dt> </dl>     | A virtualização assistida por hardware está habilitada.<br/>             |
| <dl> <dt>TECNOLOGIA</dt> </dl>      | Dá suporte às extensões de MMX.<br/>                             |
| <dl> <dt>SSE</dt> </dl>      | Dá suporte às extensões SIMD de streaming.<br/>                  |
| <dl> <dt>EXTENSÕES</dt> </dl>     | Dá suporte às extensões SIMD de streaming 2.<br/>                |
| <dl> <dt>SSE3</dt> </dl>     | Dá suporte às extensões SIMD de streaming 3.<br/>                |
| <dl> <dt>"TXTE"</dt> </dl>     | Dá suporte às extensões de tecnologia de execução confiável.<br/>    |
| <dl> <dt>"x86-64"</dt> </dl>   | Dá suporte a extensões x86-64.<br/>                              |



 

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

 

