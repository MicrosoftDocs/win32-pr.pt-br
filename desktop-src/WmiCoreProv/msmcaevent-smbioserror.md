---
description: Indica um erro de BIOS do sistema de arquitetura de verificação de máquina (MCA). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: Classe MSMCAEvent_SMBIOSError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171099"
---
# <a name="msmcaevent_smbioserror-class"></a>\_Classe MSMCAEvent SMBIOSError

A classe **MSMCAEvent \_ SMBIOSError** indica um erro de BIOS do sistema de arquitetura de verificação de máquina (MCA). Essa classe está disponível somente em sistemas Windows de 64 bits.

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Membros

A classe **MSMCAEvent \_ SMBIOSError** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MSMCAEvent \_ SMBIOSError** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True**, se esta instância da classe estiver ativa; caso contrário, **false**.

</dd> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de erros adicionais no registro.

</dd> <dt>

**CPUs**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

CPU que relatou o erro. Essa propriedade se aplica somente a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.

</dd> <dt>

**ErrorSeverity**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nível de severidade do erro relatado.



| Valor                                                                                                | Significado                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Recuperado<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Fatais<br/>       |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Corrigível<br/> |



 

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificador exclusivo desta instância da classe.

</dd> <dt>

**LogToEventlog**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for 0 (zero), esse evento não será registrado no log de eventos do sistema.

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de bytes que contém o registro de erro bruto. O número de elementos na matriz que a propriedade **size** especifica.

</dd> <dt>

**RecordId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador de registro do registro de erro para este erro.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Tamanho**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tamanho do registro de erro bruto.

</dd> <dt>

**\_tipo de evento SMBIOS \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de evento.



| Valor                                                                                                  | Significado                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl>   | Reservado.<br/>                                                                                                        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl>   | Erro de memória ECC de bit único.<br/>                                                                                     |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>   | Erro de memória ECC de vários bits.<br/>                                                                                   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>   | Erro de memória de paridade.<br/>                                                                                             |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl>   | Tempo limite do barramento.<br/>                                                                                                    |
| <span id="5"></span><dl> <dt>**05**</dt> </dl>   | Verificação de canal de e/s.<br/>                                                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl>   | NMI de software.<br/>                                                                                                    |
| <span id="7"></span><dl> <dt>**7**</dt> </dl>   | Redimensionamento da memória de post.<br/>                                                                                              |
| <span id="8"></span><dl> <dt>**8**</dt> </dl>   | Erro de POSTAgem.<br/>                                                                                                      |
| <span id="9"></span><dl> <dt>**9**</dt> </dl>   | Erro de paridade de PCI.<br/>                                                                                                |
| <span id="10"></span><dl> <dt>**10**</dt> </dl> | Erro do sistema PCI.<br/>                                                                                                |
| <span id="11"></span><dl> <dt>**11**</dt> </dl> | Falha de CPU.<br/>                                                                                                     |
| <span id="12"></span><dl> <dt>**12**</dt> </dl> | Tempo limite do temporizador de failsafe de EISA.<br/>                                                                                    |
| <span id="13"></span><dl> <dt>**13**</dt> </dl> | Log de memória corrigível desabilitado.<br/>                                                                                 |
| <span id="14"></span><dl> <dt>**140**</dt> </dl> | Registro em log desabilitado para um tipo de evento específico. Muitos erros do mesmo tipo recebidos em um curto período de tempo.<br/> |
| <span id="15"></span><dl> <dt>**15**</dt> </dl> | Reservado.<br/>                                                                                                        |
| <span id="16"></span><dl> <dt>**16**</dt> </dl> | Limite do sistema excedido (por exemplo, tensão ou limite de temperatura excedido).<br/>                                  |
| <span id="17"></span><dl> <dt>**16**</dt> </dl> | O temporizador de hardware assíncrono expirou e emitiu uma redefinição do sistema.<br/>                                                   |
| <span id="18"></span><dl> <dt>**anos**</dt> </dl> | Informações de configuração do sistema.<br/>                                                                                |
| <span id="19"></span><dl> <dt>**aprimora**</dt> </dl> | Informações de disco rígido.<br/>                                                                                           |
| <span id="20"></span><dl> <dt>**20,00**</dt> </dl> | Sistema reconfigurado.<br/>                                                                                             |
| <span id="21"></span><dl> <dt>**Abril**</dt> </dl> | Erro complexo de CPU incorrigível.<br/>                                                                                 |
| <span id="22"></span><dl> <dt>**22**</dt> </dl> | Redefinição da área de log ou desmarcada.<br/>                                                                                       |
| <span id="23"></span><dl> <dt>**23**</dt> </dl> | Inicialização do sistema. Se implementada, é garantido que essa entrada de log seja a primeira escrita em qualquer inicialização do sistema.<br/>        |



 

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de mensagem de log de eventos. Essas mensagens correspondem aos códigos de mensagem de log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do log de eventos do Windows quando ele recebe um dos eventos.

</dd> <dt>

**BITS de validação \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Bits de validação usados para indicar a validade dos campos subsequentes. Um valor de 1 (0x1) significa que o **\_ evento SMBIOS** é válido.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **MSMCAEvent \_ SMBIOSError** é derivada de [**WmiEvent**](wmievent.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | \\WMI raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes MSMCA](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

