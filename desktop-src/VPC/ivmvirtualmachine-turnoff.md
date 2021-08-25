---
title: Método TurnOff IVMVirtualMachine (VPCCOMInterfaces.h)
description: Desativa a máquina virtual.
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- Computador Virtual do método TurnOff
- Computador Virtual do método TurnOff, interface IVMVirtualMachine
- INTERFACE IVMVirtualMachine pc virtual , método TurnOff
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5351aacc3e21cd620aa31798314fd7f6728cf98653cb83cbaa2f19439d530c44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864156"
---
# <a name="ivmvirtualmachineturnoff-method"></a>Método IVMVirtualMachine::TurnOff

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Desativa a máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*turnOffTask* \[ out, retval\]
</dt> <dd>

Um [**objeto IVMTask**](ivmtask.md) usado para acompanhar o progresso da conclusão da sequência de turnoff da máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                          | Descrição                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | A operação foi bem-sucedida.<br/>                                                     |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                  | O parâmetro é **NULL.**<br/>                                                        |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ \_ ACCESSNIED)**</dt> <dt>0X80070005</dt> </dl> | O chamador deve ter permissões de acesso de execução para desligar essa máquina virtual.<br/> |
| <dl> <dt>**VM \_ E \_ VM \_ NÃO \_ EXECUTANDO**</dt> <dt>0XA0040206</dt> </dl>                     | A máquina virtual não está em execução.<br/>                                               |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | A configuração é desconhecida.<br/>                                                     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Ocorreu um erro inesperado.<br/>                                                 |



 

## <a name="remarks"></a>Comentários

Esse método desliga a máquina virtual da mesma maneira que desliga a energia em um computador físico.

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

 

