---
description: Indica um erro de componente de PCI de arquitetura de verificação de máquina (MCA). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 2b241333-2ea5-42cb-bdd3-27a10df51f3e
title: Classe MSMCAEvent_PCIComponentError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIComponentError
- MSMCAEvent_PCIComponentError.Active
- MSMCAEvent_PCIComponentError.AdditionalErrors
- MSMCAEvent_PCIComponentError.Cpu
- MSMCAEvent_PCIComponentError.ErrorSeverity
- MSMCAEvent_PCIComponentError.InstanceName
- MSMCAEvent_PCIComponentError.PCI_COMP_ERROR_STATUS
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_BusNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeBaseClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeInterface
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeSubClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceId
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_FunctionNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_SegmentNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_VendorId
- MSMCAEvent_PCIComponentError.RawRecord
- MSMCAEvent_PCIComponentError.RecordId
- MSMCAEvent_PCIComponentError.Size
- MSMCAEvent_PCIComponentError.Type
- MSMCAEvent_PCIComponentError.VALIDATION_BITS
- MSMCAEvent_PCIComponentError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cbcf3ee13e822fd59cdcdd30538d5e369d798aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765194"
---
# <a name="msmcaevent_pcicomponenterror-class"></a>\_Classe MSMCAEvent PCIComponentError

A classe **MSMCAEvent \_ PCIComponentError** indica um erro de componente de PCI MCA (arquitetura de verificação de máquina). Essa classe está disponível somente em sistemas Windows de 64 bits.

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAEvent_PCIComponentError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_COMP_ERROR_STATUS;
  uint8   PCI_COMP_INFO_BusNumber;
  uint8   PCI_COMP_INFO_ClassCodeBaseClass;
  uint8   PCI_COMP_INFO_ClassCodeInterface;
  uint8   PCI_COMP_INFO_ClassCodeSubClass;
  uint16  PCI_COMP_INFO_DeviceId;
  uint8   PCI_COMP_INFO_DeviceNumber;
  uint8   PCI_COMP_INFO_FunctionNumber;
  uint8   PCI_COMP_INFO_SegmentNumber;
  uint16  PCI_COMP_INFO_VendorId;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Membros

A classe **MSMCAEvent \_ PCIComponentError** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MSMCAEvent \_ PCIComponentError** tem essas propriedades.

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

**\_status de \_ erro de comp de PCI \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Código de erro interno.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Informações de comp de PCI \_ \_ \_ BusNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de barramento do componente PCI.

</dd> <dt>

**Informações de comp de PCI \_ \_ \_ ClassCodeBaseClass**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Código de classe da classe base do componente PCI.

</dd> <dt>

**Informações de comp de PCI \_ \_ \_ ClassCodeInterface**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Interface de código de classe do componente PCI.

</dd> <dt>

**Informações de comp de PCI \_ \_ \_ ClassCodeSubClass**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Subclasse de código de classe do componente PCI.

</dd> <dt>

**\_Dispositivo de \_ informações de comp de PCI \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador de dispositivo do componente PCI.

</dd> <dt>

**Informações de comp de PCI \_ \_ \_ DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número do dispositivo do componente PCI.

</dd> <dt>

**Informações de comp de PCI \_ \_ \_ FunctionNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número da função do componente PCI.

</dd> <dt>

**Informações de comp de PCI \_ \_ \_ SegmentNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de segmento do componente PCI.

</dd> <dt>

**Informações de comp de PCI do \_ \_ \_ fornecedor**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador de fornecedor do componente PCI.

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



| Valores                                                                               | Significado                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>   | O \_ status de erro de comp de PCI \_ \_ é válido.<br/>    |
| <dl> <dt>2 (0x2)</dt> </dl>   | As \_ informações de comp de PCI \_ são válidas.<br/>             |
| <dl> <dt>4 (0x4)</dt> </dl>   | O \_ número de memória do PCI comp \_ \_ é válido.<br/>         |
| <dl> <dt>8 (0x8)</dt> </dl>   | O \_ número de e/s de comp de PCI \_ \_ é válido.<br/>          |
| <dl> <dt>16 (0x10)</dt> </dl> | O \_ par de dados regs de PCI comp \_ \_ \_ é válido.<br/> |



 

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **MSMCAEvent \_ PCIComponentError** é derivada de [**WmiEvent**](wmievent.md).

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

 

