---
title: Propriedade IVMVirtualMachine ChassisSerialNumber (VPCCOMInterfaces. h)
description: Número de série do chassi.
ms.assetid: 03e02e6e-6819-4052-a0e0-9167eb5fdf4b
keywords:
- Propriedade ChassisSerialNumber Virtual PC
- Propriedade ChassisSerialNumber Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade ChassisSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisSerialNumber
- IVMVirtualMachine.get_ChassisSerialNumber
- IVMVirtualMachine.put_ChassisSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00edbac12248f624ac06d1f7b88c3782c3f5a3df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009463"
---
# <a name="ivmvirtualmachinechassisserialnumber-property"></a>Propriedade IVMVirtualMachine:: ChassisSerialNumber

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define o número de série do chassi.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ChassisSerialNumber(
  [in]          BSTR chasisSerialNumber
);

HRESULT get_ChassisSerialNumber(
  [out, retval] BSTR *chassisSerialNumber
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica o número de série do chassi.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                               | Significado                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                  | A operação foi bem-sucedida.<br/>                                               |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                    | O parâmetro é **NULL**.<br/>                                                  |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                 | O parâmetro é maior que 32 caracteres, uma cadeia de caracteres vazia ou não é válido.<br/> |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>            | A configuração é desconhecida.<br/>                                               |
| <dl> <dt>VM \_ E \_ VM \_ em execução \_ ou \_ salvas</dt> <dt>0xA004020B</dt> </dl> | A máquina virtual está em um estado em execução ou salvo.<br/>                         |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>            | Ocorreu um erro inesperado.<br/>                                           |



## <a name="remarks"></a>Comentários

Essa propriedade não conterá informações válidas até que a máquina virtual seja iniciada pela primeira vez. Uma cadeia de caracteres vazia será retornada se for lida antes da inicialização inicial.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

