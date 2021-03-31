---
title: Propriedade IVMSerialPort ConnectImmediately (VPCCOMInterfaces. h)
description: Determina se a porta serial deve ser aberta sem aguardar a recepção de um comando de modem.
ms.assetid: 5ac22906-0fe2-477d-98af-7c05ce274cc5
keywords:
- Propriedade ConnectImmediately Virtual PC
- Propriedade ConnectImmediately Virtual PC, interface IVMSerialPort
- IVMSerialPort interface virtual PC, Propriedade ConnectImmediately
topic_type:
- apiref
api_name:
- IVMSerialPort.ConnectImmediately
- IVMSerialPort.get_ConnectImmediately
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7661b9cf3b118427b1ecb2b6f450913e35e35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644710"
---
# <a name="ivmserialportconnectimmediately-property"></a>Propriedade IVMSerialPort:: ConnectImmediately

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se a porta serial deve ser aberta sem aguardar a recepção de um comando de modem.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ConnectImmediately(
  [out, retval] VARIANT_BOOL *vmConnectImmediately
);
```



## <a name="property-value"></a>Valor da propriedade

**Variante \_ TRUE** se a porta serial deve ser aberta sem esperar que um comando de modem seja recebido; **Variante \_** Caso contrário, false.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                            |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>                               |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl> | A configuração desta máquina virtual não é válida.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                        |



## <a name="remarks"></a>Comentários

Essa propriedade só será válida se a propriedade de [**tipo**](ivmserialport-type.md) de porta for **vmSerialPort \_ HostPort**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort é definido como 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

