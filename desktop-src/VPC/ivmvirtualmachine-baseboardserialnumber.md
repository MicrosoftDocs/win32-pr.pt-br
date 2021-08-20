---
title: Propriedade BaseBoardSerialNumber de IVMVirtualMachine (VPCCOMInterfaces.h)
description: Número de série da placa base.
ms.assetid: 374ad471-e0de-4e55-bab6-f7ddf3e5797f
keywords:
- Propriedade BaseBoardSerialNumber pc virtual
- Propriedade BaseBoardSerialNumber pc virtual, interface IVMVirtualMachine
- INTERFACE IVMVirtualMachine pc virtual , propriedade BaseBoardSerialNumber
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
ms.openlocfilehash: e2aaf205874eb7b8aaaead44a4d1a4b2775be4e01e076f1cc716058f8f9e45a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653076"
---
# <a name="ivmvirtualmachinebaseboardserialnumber-property"></a>Propriedade IVMVirtualMachine::BaseBoardSerialNumber

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define o número de série da placa base.

Essa propriedade é leitura/gravação.

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
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                    | O parâmetro é **NULL.**<br/>                                                  |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                 | O parâmetro é maior que 32 caracteres, uma cadeia de caracteres vazia ou não é válido.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>            | A configuração é desconhecida.<br/>                                               |
| <dl> <dt>VM \_ VM \_ E EM EXECUÇÃO OU SALVA \_ \_ \_ 0XA004020B</dt> <dt></dt> </dl> | A máquina virtual está em um estado de execução ou salvo.<br/>                         |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>            | Ocorreu um erro inesperado.<br/>                                           |



## <a name="remarks"></a>Comentários

Essa propriedade não conterá informações válidas até que a máquina virtual tenha sido iniciada pela primeira vez. Uma cadeia de caracteres vazia será retornada se for lida antes da inicialização inicial.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

