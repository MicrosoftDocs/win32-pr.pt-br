---
title: Propriedade SerialPorts IVMHostInfo (VPCCOMInterfaces. h)
description: Recupera os nomes de porta serial associados às portas seriais do host.
ms.assetid: ef3bc474-19c9-4d91-8aa0-7619c89fec2d
keywords:
- Propriedade SerialPorts Virtual PC
- Propriedade SerialPorts Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade SerialPorts
topic_type:
- apiref
api_name:
- IVMHostInfo.SerialPorts
- IVMHostInfo.get_SerialPorts
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8cb520ee82b53e93f9073b66d4dc4d69a2ef75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008809"
---
# <a name="ivmhostinfoserialports-property"></a>Propriedade IVMHostInfo:: SerialPorts

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera os nomes de porta serial associados às portas seriais do host.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SerialPorts(
  [out, retval] BSTR *serialPorts
);
```



## <a name="property-value"></a>Valor da propriedade

Uma lista delimitada por ponto-e-vírgula de nomes de porta serial.

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

 

