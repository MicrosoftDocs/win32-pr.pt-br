---
description: a \_ classe WMI SerialPortConfiguration do Win32 representa as configurações de transmissão de dados em uma porta serial baseada em Windows. Isso inclui configurações para estabelecer uma conexão e verificação de erro.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Classe Win32_SerialPortConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 07052c0366b32904ef6bf6f52b15f3ea98022ba8385120ec60cdefe5714e2c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079690"
---
# <a name="win32_serialportconfiguration-class"></a>\_Classe Win32 SerialPortConfiguration

a [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPortConfiguration do Win32** representa as configurações de transmissão de dados em uma porta serial baseada em Windows. Isso inclui configurações para estabelecer uma conexão e verificação de erro.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ SerialPortConfiguration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ SerialPortConfiguration** tem essas propriedades.

<dl> <dt>

**AbortReadWriteOnError**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError")
</dt> </dl>

Se **for true**, as operações de leitura e gravação serão encerradas se ocorrer um erro. Se **for true**, o driver encerrará todas as operações de leitura e gravação com um status de erro se ocorrer um erro. O driver não aceitará nenhuma outra operação de comunicação até que o aplicativo confirme o erro.

</dd> <dt>

**Taxa**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("estruturas de comunicação do win32api \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| baudrate")
</dt> </dl>

Taxa de bauds (bits por segundo) na qual o dispositivo de comunicação Opera.

Exemplo: 9600

</dd> <dt>

**BinaryModeEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")
</dt> </dl>

Se **for true**, as transferências de dados no modo binário serão habilitadas para a porta serial. os sistemas de computador que executam Windows só permitem transferências binárias por meio de portas seriais, portanto, esse valor é sempre **verdadeiro**.

</dd> <dt>

**BitsPerByte**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("estruturas de comunicação do win32api \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| bytes")
</dt> </dl>

número de bits transmitidos e recebidos para cada byte de dados para a porta serial Windows. O número pode variar com bits de correção de erro e controle, como bits de paridade.

Exemplo: 8

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**ContinueXMitOnXOff**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff")
</dt> </dl>

Se **for true**, as transmissões de dados continuarão quando o buffer de entrada entrar em **XOffXMitThreshold** bytes de estar cheio e o driver tiver transmitido o valor de **XOffChararcter** para parar de receber bytes. Se **for false**, a transmissão não continuará até que o buffer de entrada esteja dentro do **XOnXMitThreshold** bytes de estar vazio e o driver tenha transmitido o valor de **XOnCharacter** para retomar a recepção.

</dd> <dt>

**CTSOutflowControl**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow")
</dt> </dl>

Se for **true**, o sinal Clear to send (CTS) será verificado antes de transmitir os dados. O CTS sinaliza que ambos os dispositivos na conexão serial estão prontos para transferir dados. A transmissão de dados é suspensa até que o sinal CTS seja fornecido.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**DiscardNULLBytes**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull")
</dt> </dl>

Se **for true**, bytes **nulos** (caracteres) serão descartados quando forem recebidos.

</dd> <dt>

**DSROutflowControl**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow")
</dt> </dl>

Se for **true**, o controle de saída de dados será habilitado quando houver uma condição de Data Set Ready (DSR). O DSR sinaliza que a conexão foi estabelecida pelos dispositivos na conexão serial. A transmissão de dados DSR é suspensa até que o sinal de DSR seja fornecido.

</dd> <dt>

**DSRSensitivity**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity")
</dt> </dl>

Se for **true**, o driver de comunicação será sensível ao estado do sinal DSR. O driver ignora todos os bytes recebidos, a menos que a linha de entrada do modem DSR esteja alta.

</dd> <dt>

**DTRFlowControlType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl")
</dt> </dl>

Uso do controle de fluxo de Data Terminal Ready (DTR) depois que uma conexão é estabelecida.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Habilitar** ("habilitar")


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Desabilitar** ("Desabilitar")


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

**Handshake** ("handshake")


</dt> <dd></dd> </dl>

</dd> <dt>

**EOFCharacter**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar")
</dt> </dl>

Valor do caractere usado para sinalizar o fim dos dados.

Exemplo: ^ Z

</dd> <dt>

**ErrorReplaceCharacter**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")
</dt> </dl>

Valor do caractere usado para substituir bytes recebidos por um erro de paridade.

Exemplo: ^C

</dd> <dt>

**ErrorReplacementEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar")
</dt> </dl>

Se **TRUE**, os bytes recebidos com erros de paridade serão substituídos pelo **valor ErrorReplaceCharacter.** Caracteres com erros de paridade só serão substituídos se essa propriedade for **TRUE** e a paridade estiver habilitada.

</dd> <dt>

**EventCharacter**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar")
</dt> </dl>

Valor do caractere de controle usado para sinalizar um evento, como o fim do arquivo.

Exemplo: ^e

</dd> <dt>

**Isbusy**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Functions \| CreateFile")
</dt> </dl>

Se **TRUE**, a porta serial está ocupada.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ DeviceMap \\ \\ SerialComm")
</dt> </dl>

Nome da porta Windows serial.

Exemplo: "COM1"

</dd> <dt>

**Parity**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Paridade de DCB de estruturas de comunicação Win32API") \| \| [](/windows/win32/api/winbase/ns-winbase-dcb) \|
</dt> </dl>

Método de verificação de paridade a ser usado. A paridade é usada como uma técnica de verificação de erro em que um bit de paridade extra é incluído em cada unidade de dados. Em seguida, o receptor pode verificar a validade dos dados contando os bits definidos.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** ("Nenhum")


</dt> <dd>

Verificação de paridade não usada.

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Ímpar** ("Ímpar")


</dt> <dd>

Define o bit de paridade de modo que a contagem de bits definida seja um número ímpar.

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Até** mesmo ("Even")


</dt> <dd>

Define o bit de paridade de modo que a contagem de bits definida seja um número par.

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Marcar** ("Marca")


</dt> <dd>

Deixa o bit de paridade definido como 1.

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Espaço** ("Espaço")


</dt> <dd>

Deixa o bit de paridade definido como 0 (zero).

</dd> </dl>

</dd> <dt>

**ParityCheckEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity")
</dt> </dl>

Se **TRUE**, a verificação de paridade será habilitada.

</dd> <dt>

**RTSFlowControlType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Solicitação para enviar controle de fluxo (RTS). O RTS é usado para sinalizar que os dados estão disponíveis para transmissão.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Habilitar** ("Habilitar")


</dt> <dd>

O RTS é deixado para a sessão de transferência de dados.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Desabilitar** ("Desabilitar")


</dt> <dd>

O RTS é ignorado depois que o primeiro sinal RTS é recebido.

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")


</dt> <dd>

O RTS será desligado se o buffer de transmissão estiver mais de três trimestres cheio e o RTS estiver ligado quando o buffer for menor que meio cheio.

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Alternar** ("Alternar")


</dt> <dd>

O RTS será ligado se houver algum buffer de dados para transmissão.

</dd> </dl>

</dd> <dt>

**Settingid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**Stopbits**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| StopBits")
</dt> </dl>

Número de bits de parada a serem usados. Os bits de parada separam cada unidade de dados em uma conexão serial assíncrona. Eles também são enviados continuamente quando nenhum dado está disponível para transmissão.

<dt>

<span id="1"></span>

**1** ("1")


</dt> <dd></dd> <dt>

<span id="1.5"></span>

**1.5** ("1.5")


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** ("2")


</dt> <dd></dd> </dl>

</dd> <dt>

**XOffCharacter**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")
</dt> </dl>

Valor do caractere XOFF para transmissão e recepção. XOFF é um controle de software para interromper a transmissão de dados (enquanto RTS e CTS são controles de hardware). O VERTICAL retoma a transmissão.

</dd> <dt>

**XOffXMitThreshold**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim")
</dt> </dl>

Número máximo de bytes permitidos no buffer de entrada antes que o caractere XOFF seja enviado.

</dd> <dt>

**XOnCharacter**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| CharChar")
</dt> </dl>

Valor do caractere LTDA para transmissão e recepção. O VERTICAL é um controle de software para retomar a transmissão de dados (enquanto RTS e CTS são controles de hardware). XOFF interrompe a transmissão.

</dd> <dt>

**XOnXMitThreshold**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| LimLim")
</dt> </dl>

Número mínimo de bytes permitidos no buffer de entrada antes que o caractere DATA seja enviado. Essa propriedade funciona em conjunto com **XOffXMitThreshold** para regular a taxa na qual os dados são transferidos.

</dd> <dt>

**XOnXOffInFlowControl**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX")
</dt> </dl>

Se **TRUE,** o controle de fluxo TRUE/XOFF será usado durante a recepção. Se **TRUE**, o valor **XOffCharacter** é enviado quando o buffer de entrada vem dentro de bytes **XOffXMitThreshold** de estar cheio e o valor **XOnCharacter** é enviado quando o buffer de entrada vem dentro de **bytes XOnXMitThreshold** de estar vazio.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

FALSE

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

TRUE

</dd> </dl>

</dd> <dt>

**XOnXOffOutFlowControl**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX")
</dt> </dl>

O **XOnXOffOutFlowControl especifica** se o controle de fluxo NIX ou XOFF é usado durante a transmissão. Se **TRUE**, a transmissão será interrompida quando o **valor XOffCharacter** for recebido e iniciado novamente quando **o valor XOnCharacter** for recebido.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ SerialPortConfiguration do Win32** é derivada da [**configuração cim \_**](cim-setting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração cim \_**](cim-setting.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
