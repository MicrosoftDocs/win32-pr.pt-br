---
title: Propriedade IVMVirtualMachine BaseBoardSerialNumber (VPCCOMInterfaces. h)
description: Número de série da placa base.
ms.assetid: 374ad471-e0de-4e55-bab6-f7ddf3e5797f
keywords:
- Propriedade BaseBoardSerialNumber Virtual PC
- Propriedade BaseBoardSerialNumber Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade BaseBoardSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BaseBoardSerialNumber
- IVMVirtualMachine.get_BaseBoardSerialNumber
- IVMVirtualMachine.put_BaseBoardSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a6e239216eb5eadd492cb0a021d9f9c69610342
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369192"
---
# <a name="ivmvirtualmachinebaseboardserialnumber-property"></a>Propriedade IVMVirtualMachine:: BaseBoardSerialNumber

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define o número de série da placa base.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BaseBoardSerialNumber(
  [in]          BSTR baseBoardSerialNumber
);

HRESULT get_BaseBoardSerialNumber(
  [out, retval] BSTR *baseBoardSerialNumber
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica o número de série da placa base.

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

 

