---
description: Representa um evento de erro de memória MCA (Arquitetura de Verificação de Máquina). Essa classe está disponível somente em sistemas de Windows de 64 bits.
ms.assetid: 0db1d526-e2c3-4e48-90c8-cbcd9121040e
title: MSMCAEvent_MemoryError classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryError
- MSMCAEvent_MemoryError.Active
- MSMCAEvent_MemoryError.AdditionalErrors
- MSMCAEvent_MemoryError.BUS_SPECIFIC_DATA
- MSMCAEvent_MemoryError.Cpu
- MSMCAEvent_MemoryError.ErrorSeverity
- MSMCAEvent_MemoryError.InstanceName
- MSMCAEvent_MemoryError.MEM_BANK
- MSMCAEvent_MemoryError.MEM_BIT_POSITION
- MSMCAEvent_MemoryError.MEM_CARD
- MSMCAEvent_MemoryError.MEM_COLUMN
- MSMCAEvent_MemoryError.MEM_ERROR_STATUS
- MSMCAEvent_MemoryError.MEM_MODULE
- MSMCAEvent_MemoryError.MEM_NODE
- MSMCAEvent_MemoryError.MEM_PHYSICAL_ADDR
- MSMCAEvent_MemoryError.MEM_PHYSICAL_MASK
- MSMCAEvent_MemoryError.MEM_ROW
- MSMCAEvent_MemoryError.RawRecord
- MSMCAEvent_MemoryError.RecordId
- MSMCAEvent_MemoryError.REQUESTOR_ID
- MSMCAEvent_MemoryError.RESPONDER_ID
- MSMCAEvent_MemoryError.Size
- MSMCAEvent_MemoryError.TARGET_ID
- MSMCAEvent_MemoryError.Type
- MSMCAEvent_MemoryError.VALIDATION_BITS
- MSMCAEvent_MemoryError.MEM_DEVICE
- MSMCAEvent_MemoryError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f93ac9ddda978a56ceb0e258766c2e60703acc94e92c551e673a9294e2cb984c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120976"
---
# <a name="msmcaevent_memoryerror-class"></a>Classe MSMCAEvent \_ MemoryError

A **classe \_ MemoryError MSMCAEvent** representa um evento de erro de memória MCA (Arquitetura de Verificação de Máquina). Essa classe está disponível somente em sistemas de Windows de 64 bits.

A sintaxe a seguir é simplificada Managed Object Format código (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAEvent_MemoryError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint64  BUS_SPECIFIC_DATA;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint16  MEM_BANK;
  uint16  MEM_BIT_POSITION;
  uint16  MEM_CARD;
  uint16  MEM_COLUMN;
  uint64  MEM_ERROR_STATUS;
  uint16  MEM_MODULE;
  uint16  MEM_NODE;
  uint64  MEM_PHYSICAL_ADDR;
  uint64  MEM_PHYSICAL_MASK;
  uint16  MEM_ROW;
  uint8   RawRecord[];
  uint64  RecordId;
  uint64  REQUESTOR_ID;
  uint64  RESPONDER_ID;
  uint32  Size;
  uint64  TARGET_ID;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint16  MEM_DEVICE;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Membros

A **classe \_ MemoryError MSMCAEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ MemoryError MSMCAEvent** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**TRUE**, se esta instância da classe estiver ativa; caso contrário, **FALSE.**

</dd> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de erros adicionais no registro MCA.

</dd> <dt>

**DADOS \_ ESPECÍFICOS DO \_ BARRAMENTO**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Dados dependentes de barramento específicos do OEM.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Cpu**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

CPU que relatou o erro. Essa propriedade só se aplica a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.

</dd> <dt>

**Errorseverity**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nível de severidade do erro relatado.



| Valor                                                                                                | Significado                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Recuperável<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Fatal<br/>       |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Corrigível<br/> |



 

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **Chave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificador exclusivo dessa instância da classe .

</dd> <dt>

**LogToEventlog**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se zero, esse evento não será registrado no log de eventos do sistema.

</dd> <dt>

**MEM \_ BANK**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número de Módulo ou RANK do local do erro de memória.

</dd> <dt>

**POSIÇÃO DO BIT MEM \_ \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Posição do bit na palavra de memória que contém o erro.

</dd> <dt>

**CARTÃO \_ MEM**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número do cartão do local do erro de memória.

</dd> <dt>

**COLUNA \_ MEM**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número da coluna do local do erro de memória.

</dd> <dt>

**DISPOSITIVO \_ MEM**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número do dispositivo do local do erro de memória.

</dd> <dt>

**STATUS DO ERRO DO MEM \_ \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Status do erro de memória.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**MÓDULO \_ MEM**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de classificação ou módulo do local do erro de memória.

</dd> <dt>

**NÓ \_ DO MEM**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nó que contém o erro de memória. Essa propriedade se aplica somente a um sistema de vários nós. Essa propriedade é específica do fornecedor.

</dd> <dt>

**MEM \_ PHYSICAL \_ ADDR**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço físico do erro de memória.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**MÁSCARA FÍSICA DO MEM \_ \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Bits de endereço válidos no endereço físico de 64 bits do erro de memória.

> [!Note]  
> A máscara física especifica a granularidade do endereço físico. O endereço físico do erro de memória depende dos fatores de implementação de hardware.

 

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**MEM \_ ROW**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de linha do local do erro de memória.

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de bytes que contém o registro de erro bruto conforme apresentado Windows pela SAL (camada de abstração do sistema). O número de elementos na matriz é especificado pela **propriedade** Size.

</dd> <dt>

**Recordid**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador de registro do registro de erro para esse erro.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**ID DO \_ SOLICITANTE**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço de hardware do dispositivo ou componente que inicia a transação.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_ID DO RESPONDENTE**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço de hardware do respondente para a transação.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Tamanho**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tamanho do registro de erro bruto em bytes.

</dd> <dt>

**\_ID DE DESTINO**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço de hardware do destino pretendido da transação.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de mensagem de log de eventos. Essas mensagens correspondem aos códigos de mensagem do log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do Windows log de eventos quando recebe um dos eventos.

</dd> <dt>

**BITS DE \_ VALIDAÇÃO**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Bits de validação usados para indicar a validade dos campos subsequentes.



| Valores                                                                                     | Significado                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>         | O STATUS DO ERRO DO MEM \_ \_ é válido.<br/>                 |
| <dl> <dt>2 (0x2)</dt> </dl>         | MEM \_ PHYSICAL \_ ADDR é válido.<br/>                |
| <dl> <dt>4 (0x4)</dt> </dl>         | MEM \_ ADDR \_ MASK é válido.<br/>                    |
| <dl> <dt>8 (0x8)</dt> </dl>         | MEM \_ NODE é válido.<br/>                          |
| <dl> <dt>16 (0x10)</dt> </dl>       | O MEM \_ CARD é válido.<br/>                          |
| <dl> <dt>32 (0x20)</dt> </dl>       | MEM \_ MODULE é válido.<br/>                        |
| <dl> <dt>64 (0x40)</dt> </dl>       | MEM \_ BANK é válido.<br/>                          |
| <dl> <dt>128 (0x80)</dt> </dl>      | MEM \_ DEVICE é válido.<br/>                        |
| <dl> <dt>256 (0x100)</dt> </dl>     | MEM \_ ROW é válido.<br/>                           |
| <dl> <dt>512 (0x200)</dt> </dl>     | MEM \_ COLUMN é válido.<br/>                        |
| <dl> <dt>1024 (0x400)</dt> </dl>    | MEM \_ BIT POSITION é \_ válido.<br/>                 |
| <dl> <dt>2048 (0x800)</dt> </dl>    | A \_ \_ ID DO SOLICITANTE \_ DA PLATAFORMA MEM é válida.<br/>       |
| <dl> <dt>4096 (0x1000)</dt> </dl>   | A \_ ID DO RESPONDENTE DO MEM PLATFORM \_ é \_ válida.<br/>       |
| <dl> <dt>8192 (0x2000)</dt> </dl>   | MEM \_ PLATFORM TARGET é \_ válido.<br/>              |
| <dl> <dt>16384 (0x4000)</dt> </dl>  | DADOS \_ ESPECÍFICOS DO BARRAMENTO DE PLATAFORMA MEM \_ são \_ \_ válidos.<br/> |
| <dl> <dt>32768 (0x8000)</dt> </dl>  | A ID do OEM DO MEM \_ PLATFORM \_ é \_ válida.<br/>             |
| <dl> <dt>65536 (0x10000)</dt> </dl> | O \_ STRUCT DE DADOS OEM DA PLATAFORMA MEM \_ \_ é \_ válido.<br/>   |



 

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ MemoryError MSMCAEvent** é derivada de [**WMIEvent.**](wmievent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | WMI \\ raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MSMCA Classes](msmca-classes.md)
</dt> <dt>

[**Wmievent**](wmievent.md)
</dt> </dl>

 

