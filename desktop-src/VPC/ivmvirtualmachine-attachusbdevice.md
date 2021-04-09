---
title: Método IVMVirtualMachine AttachUSBDevice (VPCCOMInterfaces. h)
description: Anexa um dispositivo USB a uma VM.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- AttachUSBDevice do método virtual PC
- Método AttachUSBDevice Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método AttachUSBDevice
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
ms.openlocfilehash: c3c36224823e4bd74b6a1c757816d55608e6d95a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009498"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a>Método IVMVirtualMachine:: AttachUSBDevice

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Anexa um dispositivo USB a uma máquina virtual (VM).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inUSBDevice* \[ no\]
</dt> <dd>

Um ponteiro [**IVMUSBDevice**](ivmusbdevice.md) que representa o dispositivo USB conectado ao host.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                             | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                   | A operação foi bem-sucedida.<br/>                                           |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                     | O parâmetro é **NULL**.<br/>                                              |
| <dl> <dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt> </dl>                        | A VM não está em execução.<br/>                                                  |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>                             | A configuração é desconhecida.<br/>                                           |
| <dl> <dt>**VM \_ E \_ adições \_ não \_**</dt> <dt>0xA0040504</dt> disp. </dl>                   | Os componentes de integração não estão disponíveis no sistema operacional convidado.<br/> |
| <dl> <dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt> </dl>          | O recurso USB não está disponível.<br/>                                       |
| <dl> <dt>**VM \_ \_Erro de \_ \_ Driver do \_ conector USB E**</dt> <dt>0xA00400925</dt> </dl>          | Ocorreu um erro de driver de conector USB.<br/>                                 |
| <dl> <dt>**VM \_ \_ \_ Falha na conexão USB E \_ \_ mais \_ dispositivos**</dt> <dt>0xA00400931</dt> </dl>     | Não é possível anexar mais dispositivos à VM.<br/>                                   |
| <dl> <dt>**VM \_ \_ \_ Falha na conexão de USB E \_ \_ \_ erro de GP**</dt> de <dt>0xA00400932</dt> </dl>         | Uma configuração de política de grupo está impedindo o redirecionamento de USB.<br/>               |
| <dl> <dt>**VM \_ Falha de conexão do E \_ USB \_ \_ \_ já \_ atribuída**</dt> <dt>0xA00400933</dt> </dl> | Um dispositivo USB já foi anexado por outro cliente.<br/>            |
| <dl> <dt>**VM \_ \_Falha de \_ conexão \_ USB E**</dt> <dt>0xA00400926</dt> </dl>                    | Falha na operação de anexação.<br/>                                            |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                             | Ocorreu um erro inesperado.<br/>                                       |



 

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

 

