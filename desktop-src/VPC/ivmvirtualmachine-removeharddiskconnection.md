---
title: Método IVMVirtualMachine RemoveHardDiskConnection (VPCCOMInterfaces. h)
description: Remove a conexão de disco rígido especificada da máquina virtual.
ms.assetid: d31f2442-aae4-4987-9188-fd32778604a1
keywords:
- RemoveHardDiskConnection do método virtual PC
- Método RemoveHardDiskConnection Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método RemoveHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62a9bbf8b3aac0dd35c8390343c20a1b67b59101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369658"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a>Método IVMVirtualMachine:: RemoveHardDiskConnection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Remove a conexão de disco rígido especificada da máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hardDiskConnection* \[ no\]
</dt> <dd>

Um objeto [**IVMHardDiskConnection**](ivmharddiskconnection.md) que representa a conexão de disco rígido a ser removida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                            | Descrição                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | A operação foi bem-sucedida.<br/>                              |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                    | O parâmetro é **NULL**.<br/>                                 |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>            | A configuração é desconhecida.<br/>                              |
| <dl> <dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt> </dl> | A máquina virtual está em um estado em execução ou salvo.<br/>        |
| <dl> <dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt> </dl>         | A unidade especificada não está conectada a este local de barramento.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>            | Ocorreu um erro inesperado.<br/>                          |



 

## <a name="remarks"></a>Comentários

Você só pode remover uma conexão de disco rígido existente de uma máquina virtual parada. Uma lista de conexões atualmente anexadas à máquina virtual é obtida pela enumeração da propriedade [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

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

 

