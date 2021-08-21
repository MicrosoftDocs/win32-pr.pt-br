---
description: Representa o header comum que todas as classes MSMCAEvent usam. Essa classe está disponível somente em sistemas de Windows de 64 bits.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: MSMCAEvent_Header classe
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
ms.openlocfilehash: c9b09e745fd3d2a6819a756ff6a012c85330f327739dae28445c2e376189d293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051264"
---
# <a name="msmcaevent_header-class"></a>Classe de header MSMCAEvent \_

A **classe de \_ header MSMCAEvent** representa o header comum que todas as [classes MSMCA](msmca-classes.md) usam. Os arquivos de header são usados para que o código C e C++ possa ter uma estrutura de dados que descreva o header comum para todos os eventos. Essa classe é reservada para uso interno. Essa classe está disponível somente em sistemas de Windows de 64 bits.

A sintaxe a seguir é simplificada Managed Object Format código (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

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

A **classe de \_ header MSMCAEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe de \_ header MSMCAEvent** tem essas propriedades.

<dl> <dt>

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

CPU que relata o erro. Essa propriedade só se aplica a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.

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

**LogToEventlog**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se 0 (zero), esse evento não será registrado no log de eventos do sistema.

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

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de mensagem de log de eventos. Essas mensagens correspondem aos códigos de mensagem do log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do Windows log de eventos quando recebe um dos eventos.

</dd> </dl>

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

[WMI C++ Classes](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

