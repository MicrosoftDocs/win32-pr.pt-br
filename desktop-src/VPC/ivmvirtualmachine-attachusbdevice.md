---
title: Método IVMVirtualMachine AttachUSBDevice (VPCCOMInterfaces.h)
description: Anexa um dispositivo USB a uma VM.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- Computador Virtual attachUSBDevice
- AttachUSBDevice method Virtual PC , IVMVirtualMachine interface
- INTERFACE IVMVirtualMachine Pc Virtual, método AttachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c62f3e6862e14a7faa70719d1238500ab5dfe1de10801e7aea390e24a07210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006896"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a>Método IVMVirtualMachine::AttachUSBDevice

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Anexa um dispositivo USB a uma VM (máquina virtual).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inUSBDevice* \[ Em\]
</dt> <dd>

Um [**ponteiro IVMUSBDevice**](ivmusbdevice.md) que representa o dispositivo USB conectado ao host.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                             | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                   | A operação foi bem-sucedida.<br/>                                           |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                     | O parâmetro é **NULL.**<br/>                                              |
| <dl> <dt>**VM \_ E \_ VM \_ NÃO \_ EXECUTANDO**</dt> <dt>0XA0040206</dt> </dl>                        | A VM não está em execução.<br/>                                                  |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                             | A configuração é desconhecida.<br/>                                           |
| <dl> <dt>**VM \_ E \_ ADIÇÕES \_ NÃO SÃO \_ 0XA0040504**</dt> <dt></dt> </dl>                   | Os Componentes de Integração não estão disponíveis no sistema operacional convidado.<br/> |
| <dl> <dt>**VM \_ O \_ RECURSO DE \_ ADIÇÕES E NÃO \_ \_ ESTÁ**</dt> <dt>0XA0040505</dt> </dl>          | O recurso USB não está disponível.<br/>                                       |
| <dl> <dt>**VM \_ ERRO \_ DE DRIVER DO \_ \_ CONECTOR \_ USB E**</dt> <dt>0XA00400925</dt> </dl>          | Ocorreu um erro de driver do Conector USB.<br/>                                 |
| <dl> <dt>**VM \_ FALHA NA ANEXAÇÃO USB E \_ \_ MAIS \_ \_ \_ DISPOSITIVOS**</dt> <dt>0XA00400931</dt> </dl>     | Não é possível anexar mais dispositivos à VM.<br/>                                   |
| <dl> <dt>**VM \_ FALHA \_ NA CONEXÃO USB DO GP \_ \_ \_ \_ E**</dt> 0XA00400932 <dt></dt> </dl>         | Uma configuração de política de grupo está impedindo o redirecionamento de USB.<br/>               |
| <dl> <dt>**VM \_ FALHA \_ NA ANEXAÇÃO USB \_ E JÁ ATRIBUÍDA \_ \_ \_ 0XA00400933**</dt> <dt></dt> </dl> | Um dispositivo USB já foi anexado por algum outro cliente.<br/>            |
| <dl> <dt>**VM \_ FALHA \_ NA \_ ANEXAÇÃO \_ USB**</dt> E <dt>0XA00400926</dt> </dl>                    | Falha na operação de anexação.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                             | Ocorreu um erro inesperado.<br/>                                       |



 

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

 

