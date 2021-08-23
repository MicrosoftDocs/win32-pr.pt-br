---
title: Propriedade IVMHostInfo ProcessorFeaturesString (VPCCOMInterfaces.h)
description: Recupera os recursos de lista com suporte pelo processador de host.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- Propriedade ProcessorFeaturesString pc virtual
- Propriedade ProcessorFeaturesString pc virtual , interface IVMHostInfo
- Interface IVMHostInfo pc virtual , propriedade ProcessorFeaturesString
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
ms.openlocfilehash: 1040702df250c906bb32af5068a340c37a9ba3faabee3af17d8397bfdc8059e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998886"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a>Propriedade IVMHostInfo::P rocessorFeaturesString

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera os recursos de lista com suporte pelo processador de host.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a>Valor da propriedade

Uma lista de recursos delimitada por vírgulas. Um exemplo seria "MMX,SSE,SSE2,x86-64".



| Valor                                                                                 | Significado                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>"AMD-V"</dt> </dl>    | Dá suporte às extensões de Virtualização amd.<br/>              |
| <dl> <dt>"Intel VT"</dt> </dl> | Dá suporte às extensões da Intel Virtualization Technology.<br/> |
| <dl> <dt>"HAVD"</dt> </dl>     | A Virtualização Assistida por Hardware está desabilitada.<br/>            |
| <dl> <dt>"HAVE"</dt> </dl>     | A Virtualização Assistida por Hardware está habilitada.<br/>             |
| <dl> <dt>"MMX"</dt> </dl>      | Dá suporte às extensões MMX.<br/>                             |
| <dl> <dt>"SSE"</dt> </dl>      | Dá suporte às extensões SIMD de streaming.<br/>                  |
| <dl> <dt>"SSE2"</dt> </dl>     | Dá suporte às Extensões SIMD de Streaming 2.<br/>                |
| <dl> <dt>"SSE3"</dt> </dl>     | Dá suporte às Extensões SIMD de Streaming 3.<br/>                |
| <dl> <dt>"TXTE"</dt> </dl>     | Dá suporte às extensões de Tecnologia de Execução Confiável.<br/>    |
| <dl> <dt>"x86-64"</dt> </dl>   | Dá suporte a extensões x86-64.<br/>                              |



 

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>         | O parâmetro é **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ocorreu um erro inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHostInfo é definido como \_ 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

