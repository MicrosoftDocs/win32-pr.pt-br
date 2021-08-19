---
title: Propriedade IVMVirtualMachine ShutdownActionOnQuit (VPCCOMInterfaces.h)
description: Ação a ser executada nessa máquina virtual se ela estiver em execução quando Windows virtual PC for encerrar.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- Computador Virtual da propriedade ShutdownActionOnQuit
- Propriedade ShutdownActionOnQuit pc virtual , interface IVMVirtualMachine
- INTERFACE IVMVirtualMachine Pc Virtual, propriedade ShutdownActionOnQuit
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
ms.openlocfilehash: c859a0f1715685e07ba13d6fb06fc99dc08f712fd20fa56a4672a2cc857b1591
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124696"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a>Propriedade IVMVirtualMachine::ShutdownActionOnQuit

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define a ação a ser executada nessa VM (máquina virtual) se ela estiver em execução quando Windows Virtual PC for encerrar.

Essa propriedade é leitura/gravação.

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

Especifica como desligar essa VM se ela estiver em execução quando Windows Virtual PC for encerrado. Para ver uma lista de valores, [**consulte VMShutdownAction**](vmshutdownaction.md).

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                                       |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>         | O parâmetro é **NULL** ou não é um valor válido.<br/>                     |
| <dl> <dt>E \_ ACESSODENIED</dt> <dt>0x80070005</dt> </dl>    | O usuário atual não tem acesso suficiente ao arquivo de configuração.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | A configuração é desconhecida.<br/>                                       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ocorreu um erro inesperado.<br/>                                   |



## <a name="remarks"></a>Comentários

Por padrão, as VMs em execução são salvas quando Windows computador virtual é parado. A ação de **desligamento vmShutdownAction \_ Save** (0) salvará o estado da VM. A **ação vmShutdownAction \_ TurnOff** (1) desligará a VM. A **ação vmShutdownAction \_ Shutdown** (2) desligará o sistema operacional convidado se os componentes de integração estão disponíveis e salvará a VM caso contrário.

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
</dt> <dt>

[**VMShutdownAction**](vmshutdownaction.md)
</dt> </dl>

 

