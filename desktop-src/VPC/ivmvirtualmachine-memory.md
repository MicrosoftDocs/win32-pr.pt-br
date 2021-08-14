---
title: Propriedade IVMVirtualMachine Memory (VPCCOMInterfaces.h)
description: Quantidade de memória física na máquina virtual, em megabytes.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Propriedade de memória PC virtual
- Propriedade de memória PC virtual, interface IVMVirtualMachine
- INTERFACE IVMVirtualMachine pc virtual , propriedade de memória
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a828dde1804e546c97fe7cd2c161fc45366d416ba0e44900816c7bbee4b1ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344660"
---
# <a name="ivmvirtualmachinememory-property"></a>Propriedade IVMVirtualMachine::Memory

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define a quantidade de memória física na máquina virtual, em megabytes.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica a quantidade de memória física, em megabytes.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                         | Significado                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>                  |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>              | O parâmetro é **NULL.**<br/>                     |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>           | O parâmetro não é válido ou está fora do intervalo.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>      | A configuração é desconhecida.<br/>                  |
| <dl> <dt>VM \_ E \_ PREF \_ NÃO ENCONTRADO \_ 0XA0040300</dt> <dt></dt> </dl> | A preferência não foi encontrada.<br/>                  |
| <dl> <dt>VM \_ E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl> | A máquina virtual está em execução ou salva.<br/>       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Ocorreu um erro inesperado.<br/>              |



## <a name="remarks"></a>Comentários

A quantidade de memória física em uma máquina virtual deve ser pelo menos 4 MB. O limite superior de memória depende da configuração do host, mas pode ser no máximo 3.712 MB.

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

 

