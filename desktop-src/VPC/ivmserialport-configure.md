---
title: Método de configuração de IVMSerialPort (VPCCOMInterfaces. h)
description: Configura a porta serial.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Configurar o método virtual PC
- Configurar o método virtual PC, interface IVMSerialPort
- IVMSerialPort interface virtual PC, método configure
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009438"
---
# <a name="ivmserialportconfigure-method"></a>Método IVMSerialPort:: Configure

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Configura a porta serial.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PortType* \[ no\]
</dt> <dd>

O tipo de porta serial. Para obter uma lista de valores, consulte [**VMSerialPortType**](vmserialporttype.md).

</dd> <dt>

*portaname* \[ no\]
</dt> <dd>

O nome da porta serial. Por exemplo, "COM1" para **vmSerialPort \_ HostPort**, "C: \\SerialPort.txt" para **vmSerialPort \_ textfile** ou " \\ \\ *nome_do_servidor* \\ pipe pipeName \\ " para **vmSerialPort \_ NamedPipe**.

</dd> <dt>

*vmConnectImmediately* \[ no\]
</dt> <dd>

**True** se a porta serial do host precisar ser aberta imediatamente quando a máquina virtual for iniciada; caso contrário, **false** . Ignorado se *PortType* não for **vmSerialPort \_ HostPort**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                            | Descrição                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | O parâmetro *PortType* não é válido.<br/>                                                                                 |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                      |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro *PortName* é **nulo**.<br/>                                                                                  |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (erro \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt> </dl>      | Não há memória suficiente disponível para concluir esta solicitação.<br/>                                                         |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | O caminho especificado pelo parâmetro *PortName* é muito longo. O caminho deve ser menor que **o \_ caminho máximo** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt> </dl>    | O parâmetro *PortName* contém um caractere inválido (um de " \* ? <>/ \| ": ").<br/>                                    |
| <dl> <dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt> </dl>    | O parâmetro *PortName* especifica um caminho relativo ou vazio. Um caminho absoluto é necessário.<br/>                            |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>                            | A configuração desta máquina virtual não é válida.<br/>                                                               |
| <dl> <dt>**VM \_ E \_ pref \_ \_ valor ilegal**</dt> <dt>0xA0040301</dt> </dl>                   | A porta especificada já está em uso.<br/>                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort é definido como 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

