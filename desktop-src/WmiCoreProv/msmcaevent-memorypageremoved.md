---
description: Indica que uma página de memória foi removida do uso do sistema devido a erros de ECC (Verificação e Correção de Erro) de hardware excessivos. Essa classe está disponível somente em sistemas de Windows de 64 bits.
ms.assetid: 364a2520-8d7c-44f2-95f6-eea9a5531975
title: MSMCAEvent_MemoryPageRemoved classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryPageRemoved
- MSMCAEvent_MemoryPageRemoved.Active
- MSMCAEvent_MemoryPageRemoved.InstanceName
- MSMCAEvent_MemoryPageRemoved.PhysicalAddress
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: d8229848cf1113736e3b9a4e37cd9493b8c724c58c384387536cded4742ca3c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558463"
---
# <a name="msmcaevent_memorypageremoved-class"></a>Classe MSMCAEvent \_ MemoryPageRemoved

A **classe MSMCAEvent \_ MemoryPageRemoved** indica que uma página de memória foi removida do uso do sistema devido a erros de ECC (verificação e correção de erro) de hardware excessivos. Essa classe está disponível somente em sistemas de Windows de 64 bits.

A sintaxe a seguir é simplificada do Managed Object Format (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAEvent_MemoryPageRemoved : WmiEvent
{
  boolean Active;
  string  InstanceName;
  uint64  PhysicalAddress;
};
```

## <a name="members"></a>Membros

A **classe MSMCAEvent \_ MemoryPageRemoved** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe MSMCAEvent \_ MemoryPageRemoved** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**TRUE**, se esta instância da classe estiver ativa; caso **contrário, FALSE.**

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

**Physicaladdress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço da página de memória que foi removida.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe MSMCAEvent \_ MemoryPageRemoved** é derivada de [**WMIEvent.**](wmievent.md)

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

 

