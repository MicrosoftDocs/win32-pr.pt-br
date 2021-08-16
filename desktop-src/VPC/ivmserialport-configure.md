---
title: Método IVMSerialPort Configure (VPCCOMInterfaces.h)
description: Configura a porta serial.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Configurar o computador virtual do método
- Configurar o método Virtual PC, interface IVMSerialPort
- COMPUTADOR Virtual da interface IVMSerialPort, método Configure
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
ms.openlocfilehash: e6e67d84239f7b672b5b8c47346d1dde73de6a35c1e99a3ba231b8425fe8b7d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136619"
---
# <a name="ivmserialportconfigure-method"></a>Método IVMSerialPort::Configure

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*portType* \[ Em\]
</dt> <dd>

O tipo de porta serial. Para ver uma lista de valores, [**consulte VMSerialPortType**](vmserialporttype.md).

</dd> <dt>

*portName* \[ Em\]
</dt> <dd>

O nome da porta serial. Por exemplo, "COM1" para **vmSerialPort \_ HostPort**, "C:SerialPort.txt" para \\ **vmSerialPort \_ TextFile** ou " \\ \\ *servername* \\ \\ *pipename pipename*" para **vmSerialPort \_ NamedPipe**.

</dd> <dt>

*vmConnectImmediately* \[ Em\]
</dt> <dd>

**TRUE** se a porta serial do host deve ser aberta imediatamente quando a máquina virtual é iniciada e **FALSE** caso contrário. Ignorado se *portType* não for **vmSerialPort \_ HostPort.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                            | Descrição                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | O *parâmetro portType* não é válido.<br/>                                                                                 |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                      |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                    | O *parâmetro portName* é **NULL.**<br/>                                                                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>      | Não há memória suficiente disponível para concluir essa solicitação.<br/>                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0X8007006F</dt> </dl> | O caminho especificado pelo parâmetro *portName* é muito longo. O caminho deve ter menos de **MAX \_ PATH** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0X8007007B</dt> </dl>    | O *parâmetro portName* contém um caractere inválido (um de " \* ?<>/ \| ":").<br/>                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | O *parâmetro portName* especifica um caminho vazio ou relativo. Um caminho absoluto é necessário.<br/>                            |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                            | A configuração dessa máquina virtual não é válida.<br/>                                                               |
| <dl> <dt>**VM \_ E \_ PREF \_ ILLEGAL VALUE \_ 0XA0040301**</dt> <dt></dt> </dl>                   | A porta especificada já está em uso.<br/>                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMSerialPort é definido como \_ 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

