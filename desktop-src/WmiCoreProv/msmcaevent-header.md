---
description: Representa o cabeçalho comum que todas as classes MSMCAEvent usam. Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: Classe MSMCAEvent_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784956"
---
# <a name="msmcaevent_header-class"></a>\_Classe de cabeçalho MSMCAEvent

A classe de **\_ cabeçalho MSMCAEvent** representa o cabeçalho comum que todas as [classes MSMCA](msmca-classes.md) usam. Os arquivos de cabeçalho são usados para que o código C e C++ possa ter uma estrutura de dados que descreva o cabeçalho comum para todos os eventos. Essa classe é reservada para uso interno. Essa classe está disponível somente em sistemas Windows de 64 bits.

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a>Membros

A classe de **\_ cabeçalho MSMCAEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ cabeçalho MSMCAEvent** tem essas propriedades.

<dl> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de erros adicionais no registro MCA.

</dd> <dt>

**CPUs**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

CPU que relata o erro. Essa propriedade se aplica somente a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.

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

**LogToEventlog**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for 0 (zero), esse evento não será registrado no log de eventos do sistema.

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

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de mensagem de log de eventos. Essas mensagens correspondem aos códigos de mensagem de log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do log de eventos do Windows quando ele recebe um dos eventos.

</dd> </dl>

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

[Classes WMI C++](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

