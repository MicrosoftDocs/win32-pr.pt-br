---
title: Método IVMVirtualPC UnregisterVirtualMachine (VPCCOMInterfaces. h)
description: Cancela o registro de uma configuração de VM sem excluir o arquivo de configuração.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- UnregisterVirtualMachine do método virtual PC
- Método UnregisterVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método UnregisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6173d6f43d51384af610b850ec654d185f0a8ce31a375b4dd90bd929c6455b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652726"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a>Método IVMVirtualPC:: UnregisterVirtualMachine

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Cancela o registro de uma configuração de VM (máquina virtual) sem excluir o arquivo de configuração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VirtualMachine* \[ no\]
</dt> <dd>

Um ponteiro para um objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa a configuração de VM a ser cancelada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                | O parâmetro *VirtualMachine* era **nulo**.<br/>                                         |
| <dl> <dt>**VM \_ E \_ VM \_ executando**</dt> <dt>0xA0040500</dt> </dl>                        | A VM está em execução.<br/>                                                                   |
| <dl> <dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt> </dl> | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Comentários

Somente VMs interrompidas podem ter o registro cancelado. O estado salvo existente ou os dados da unidade de desfazer para essa configuração serão mantidos quando uma VM tiver o registro cancelado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

