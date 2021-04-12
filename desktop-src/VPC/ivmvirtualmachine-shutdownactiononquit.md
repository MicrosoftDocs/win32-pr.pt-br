---
title: Propriedade IVMVirtualMachine ShutdownActionOnQuit (VPCCOMInterfaces. h)
description: Ação a ser executada nesta máquina virtual se estiver em execução quando o Windows Virtual PC for encerrado.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- Propriedade ShutdownActionOnQuit Virtual PC
- Propriedade ShutdownActionOnQuit Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade ShutdownActionOnQuit
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01469e48e767777c6ea3daa4d0f3a923dce67726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455684"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a>Propriedade IVMVirtualMachine:: ShutdownActionOnQuit

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define a ação a ser executada nessa VM (máquina virtual) se ela estiver em execução quando o Windows Virtual PC for encerrado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica como desligar essa VM se ela estiver em execução quando o Windows Virtual PC for encerrado. Para obter uma lista de valores, consulte [**VMShutdownAction**](vmshutdownaction.md).

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                                       |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **nulo** ou não é um valor válido.<br/>                     |
| <dl> <dt>E \_ ACCESSDENIED</dt> <dt>0x80070005</dt> </dl>    | O usuário atual não tem acesso suficiente ao arquivo de configuração.<br/> |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl> | A configuração é desconhecida.<br/>                                       |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                                   |



## <a name="remarks"></a>Comentários

Por padrão, as VMs em execução são salvas quando o Windows Virtual PC é encerrado. A ação de desligamento **vmShutdownAction \_ Save** (0) irá salvar o estado da VM. A ação de desativação de **vmShutdownAction \_** (1) desligará a VM. A ação de **\_ desligamento vmShutdownAction** (2) desligará o sistema operacional convidado se os componentes de integração estiverem disponíveis e salvará a VM de outra forma.

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
</dt> <dt>

[**VMShutdownAction**](vmshutdownaction.md)
</dt> </dl>

 

