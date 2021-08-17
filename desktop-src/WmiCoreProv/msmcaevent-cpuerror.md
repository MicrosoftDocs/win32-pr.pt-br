---
description: Representa um evento de erro de CPU. Essa classe está disponível somente em sistemas de Windows de 64 bits.
ms.assetid: 4ee4aa51-a965-4569-b53c-0ba21bf42752
title: MSMCAEvent_CPUError classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_CPUError
- MSMCAEvent_CPUError.Active
- MSMCAEvent_CPUError.AdditionalErrors
- MSMCAEvent_CPUError.Cpu
- MSMCAEvent_CPUError.ErrorSeverity
- MSMCAEvent_CPUError.InstanceName
- MSMCAEvent_CPUError.Level
- MSMCAEvent_CPUError.RawRecord
- MSMCAEvent_CPUError.RecordId
- MSMCAEvent_CPUError.Size
- MSMCAEvent_CPUError.Type
- MSMCAEvent_CPUError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 42542f9e32bee31e44df65c0d0ade3d337e3fe395315fe28d6fd8b1c66b3b8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926869"
---
# <a name="msmcaevent_cpuerror-class"></a>Classe CPUError MSMCAEvent \_

A **classe \_ CPUError MSMCAEvent** representa um evento de erro de CPU. Essa classe está disponível somente em sistemas de Windows de 64 bits.

A sintaxe a seguir é simplificada Managed Object Format código (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAEvent_CPUError : WmiEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint32  Level;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Membros

A **classe \_ CPUError MSMCAEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ CPUError MSMCAEvent** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**TRUE**, se esta instância da classe estiver ativa; caso **contrário, FALSE.**

</dd> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de erros adicionais no registro MCA.

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

Identificador exclusivo para esta instância da classe .

</dd> <dt>

**Level**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiMissingData** (-1)
</dt> </dl>

Nível de cache, TLB (buffer de tradução) ou estrutura microtetônica em que o erro ocorreu. Um valor de 0 (zero) indica o primeiro nível.

</dd> <dt>

**LogToEventlog**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se zero, esse evento não será registrado no log de eventos do sistema.

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de bytes que contém o registro de erro bruto. O número de elementos na matriz especificada **pela propriedade** Size.

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

**Tamanho**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tamanho do registro de erro bruto em bytes.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de mensagem de log de eventos. Essas mensagens correspondem aos códigos de mensagem do log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do Windows log de eventos quando recebe um dos eventos.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ CPUError MSMCAEvent** é derivada de [**WMIEvent**](wmievent.md).

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

 

