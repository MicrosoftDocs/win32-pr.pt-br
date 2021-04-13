---
title: Método IVMVirtualMachine StartCommunicationChannel (VPCCOMInterfaces. h)
description: Configura um canal de comunicação entre o host e o sistema operacional convidado.
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- StartCommunicationChannel do método virtual PC
- Método StartCommunicationChannel Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método StartCommunicationChannel
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455682"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a>Método IVMVirtualMachine:: StartCommunicationChannel

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Configura um canal de comunicação entre o host e o sistema operacional convidado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inHostEndpointType* \[ no\]
</dt> <dd>

Esse parâmetro deve ser **vmEndpoint \_ NamedPipe** (0).

</dd> <dt>

*inHostEndPointName* \[ no\]
</dt> <dd>

O nome exclusivo do pipe. Essa cadeia de caracteres deve ter o seguinte formato: " \\ \\ . \\ pipe \\ *pipeName*". A parte de *pipeName* do nome pode incluir qualquer caractere diferente de uma barra invertida, incluindo números e caracteres especiais. A cadeia de caracteres do nome do pipe inteiro pode ter até 256 caracteres. Os nomes dos pipes não diferenciam maiúsculas de minúsculas.

</dd> <dt>

*inGuestEndpointType* \[ no\]
</dt> <dd>

Esse parâmetro deve ser **vmEndpoint \_ tcpip** (1).

</dd> <dt>

*inGuestEndpointName* \[ no\]
</dt> <dd>

O número da porta na qual o servidor TCP no convidado está escutando.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                                  | Descrição                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                        | A operação foi bem-sucedida.<br/>                                                                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                       | O parâmetro *inHostEndpointType* não é **vmEndpoint \_ NamedPipe** (0) ou o parâmetro *inGuestEndpointType* não é **vmEndpoint \_ tcpip** (1).<br/> |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                          | O parâmetro *inHostEndPointName* ou *inGuestEndpointName* é **nulo** ou não é um valor válido.<br/>                                                    |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                                  | Ocorreu um erro inesperado.<br/>                                                                                                                |
| <dl> <dt>**HRESULT \_ DO \_ Win32 ( \_ \_ identificador inválido do erro)**</dt> <dt>0x80070006</dt> </dl>        | Um identificador não é válido.<br/>                                                                                                                           |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (erro \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt> </dl>            | Não há memória suficiente disponível para concluir esta solicitação.<br/>                                                                                   |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (erro \_ não \_ pronto)**</dt> <dt>0x80070015</dt> </dl>             | O sistema subjacente que ele usa para fornecer serviços de rede está sendo inicializado no momento.<br/>                                                        |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt> </dl>        | O nome do pipe já está em uso.<br/>                                                                                                                 |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (pipe de erro \_ \_ ocupado)**</dt> <dt>0x800700e7</dt> </dl>             | Um ou mais canais estão em execução e podem ser disponibilizados em breve.<br/>                                                                          |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (máximo de sessões de erro \_ \_ \_ atingido)**</dt> <dt>0x80070161</dt> </dl> | Os números máximos de canais de comunicação disponíveis estão em uso. Outro canal não pode ser iniciado neste momento.<br/>                              |
| <dl> <dt>**HRESULT \_ DO \_ Win32 ( \_ \_ incompatibilidade de revisão de erro)**</dt> <dt>0x8007051a</dt> </dl>     | Há uma incompatibilidade entre a versão do host e os subsistemas convidados. Consulte o log de eventos do Windows para obter mais detalhes.<br/>                             |
| <dl> <dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt> </dl>                             | A VM não está em execução.<br/>                                                                                                                           |



 

## <a name="remarks"></a>Comentários

A implementação atual dá suporte apenas à interface de pipe nomeado no host e na interface TCP/IP no sistema operacional convidado.

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

[**VMEndpointType**](vmendpointtype.md)
</dt> </dl>

 

