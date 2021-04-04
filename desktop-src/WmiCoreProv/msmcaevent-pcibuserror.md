---
description: Representa um erro de barramento PCI de MCA (arquitetura de verificação de máquina). Essa classe está disponível somente para computadores que executam o em um sistema operacional Windows de 64 bits.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: Classe MSMCAEvent_PCIBusError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647120"
---
# <a name="msmcaevent_pcibuserror-class"></a>\_Classe MSMCAEvent PCIBusError

A classe **MSMCAEvent \_ PCIBusError** representa um erro de barramento PCI MCA (arquitetura de verificação de máquina). Essa classe está disponível somente para computadores que executam o em um sistema operacional Windows de 64 bits.

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Membros

A classe **MSMCAEvent \_ PCIBusError** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MSMCAEvent \_ PCIBusError** tem essas propriedades.

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

**\_endereço de barramento PCI \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Memória ou endereço de e/s no barramento PCI no momento do evento.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_cmd de barramento PCI \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Comando ou operação de barramento no momento do evento.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_dados de barramento PCI \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Dados no barramento PCI no momento do evento.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_status de \_ erro do barramento PCI \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Status do barramento no momento do erro.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_tipo de \_ erro do barramento PCI \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de erro de barramento PCI.



| Valor                                                                                                | Significado                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Erro desconhecido ou específico do sistema OEM.<br/>            |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Erro de paridade de dados.<br/>                               |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Erro do sistema.<br/>                                    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Anulação mestre.<br/>                                    |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | Tempo limite de barramento ou nenhum dispositivo presente (sem DEVSEL \# ).<br/> |
| <span id="5"></span><dl> <dt>**05**</dt> </dl> | Erro de paridade de dados mestre.<br/>                        |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Erro de paridade de endereço.<br/>                            |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Erro de paridade de comando.<br/>                            |



 

</dd> <dt>

**\_ID do barramento PCI \_ \_ BusNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador designado para o barramento PCI que encontrou o erro.

</dd> <dt>

**\_ID do barramento PCI \_ \_ SegmentNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador de segmento designado para o barramento PCI que encontrou o erro.

</dd> <dt>

**\_ID do \_ solicitante do barramento PCI \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador do solicitante de barramento PCI no momento do evento.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_ID do \_ respondente do barramento PCI \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador de respondente do barramento PCI no momento do evento.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de bytes que contém o registro de erro bruto conforme apresentado ao Windows pela camada de abstração do sistema (SAL). O número de elementos na matriz é especificado pela propriedade **size** .

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

Bits de validação usados para indicar a validade dos campos subsequentes.



| Valores                                                                                  | Significado                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>      | O \_ status de erro do barramento PCI \_ \_ é válido.<br/>     |
| <dl> <dt>2 (0x2)</dt> </dl>      | O \_ tipo de erro do barramento PCI \_ \_ é válido.<br/>       |
| <dl> <dt>4 (0x4)</dt> </dl>      | A \_ ID do barramento PCI \_ é válida.<br/>                |
| <dl> <dt>8 (0x8)</dt> </dl>      | O \_ endereço de barramento PCI \_ é válido.<br/>           |
| <dl> <dt>16 (0x10)</dt> </dl>    | \_Os dados do barramento PCI \_ são válidos.<br/>              |
| <dl> <dt>32 (0x20)</dt> </dl>    | O \_ cmd de barramento PCI \_ é válido.<br/>               |
| <dl> <dt>64 (0x40)</dt> </dl>    | A \_ ID do solicitante do barramento PCI \_ \_ é válida.<br/>     |
| <dl> <dt>128 (0x80)</dt> </dl>   | A \_ ID do respondente do barramento PCI \_ \_ é válida.<br/>     |
| <dl> <dt>256 (0x100)</dt> </dl>  | A \_ ID de destino do barramento PCI \_ \_ é válida.<br/>        |
| <dl> <dt>512 (0x200)</dt> </dl>  | A \_ ID OEM do barramento PCI \_ \_ é válida.<br/>           |
| <dl> <dt>1024 (0x400)</dt> </dl> | O \_ struct de dados OEM do barramento PCI \_ \_ \_ é válido.<br/> |



 

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **MSMCAEvent \_ PCIBusError** é derivada de [**WmiEvent**](wmievent.md).

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

 

