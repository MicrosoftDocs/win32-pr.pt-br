---
title: Propriedade de memória IVMVirtualMachine (VPCCOMInterfaces. h)
description: Quantidade de memória física na máquina virtual, em megabytes.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Propriedade de memória virtual PC
- Propriedade de memória virtual PC, interface IVMVirtualMachine
- Virtual PC interface IVMVirtualMachine, Propriedade Memory
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
ms.openlocfilehash: 3b73251b58639e0311e33120cd4bb0e778a017b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105747501"
---
# <a name="ivmvirtualmachinememory-property"></a>Propriedade IVMVirtualMachine:: Memory

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define a quantidade de memória física na máquina virtual, em megabytes.

Esta propriedade é de leitura/gravação.

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
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>              | O parâmetro é **NULL**.<br/>                     |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>           | O parâmetro não é válido ou está fora do intervalo.<br/> |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>      | A configuração é desconhecida.<br/>                  |
| <dl> <dt>VM \_ E \_ pref \_ não \_ encontrado</dt> <dt>0xA0040300</dt> </dl> | A preferência não foi encontrada.<br/>                  |
| <dl> <dt>VM \_ E \_ pref \_ VM \_ ativa</dt> <dt>0xA0040302</dt> </dl> | A máquina virtual está em execução ou salva.<br/>       |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>      | Ocorreu um erro inesperado.<br/>              |



## <a name="remarks"></a>Comentários

A quantidade de memória física em uma máquina virtual deve ser de pelo menos 4 MB. O limite superior na memória depende da configuração do host, mas pode ter no máximo 3.712 MB.

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

 

