---
description: Contém um evento de verificação de máquina corrigida (CMC). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: e12efbf7-7d53-415a-bc48-90d33e4ce16d
title: Classe MSMCAInfo_RawCMCEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCMCEvent
- MSMCAInfo_RawCMCEvent.Active
- MSMCAInfo_RawCMCEvent.Count
- MSMCAInfo_RawCMCEvent.InstanceName
- MSMCAInfo_RawCMCEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 1bb60d5fbcf004b924a91e640d8cd8a8c5ad3c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790382"
---
# <a name="msmcainfo_rawcmcevent-class"></a>\_Classe MSMCAInfo RawCMCEvent

A classe **MSMCAInfo \_ RawCMCEvent** contém um evento de verificação de máquina corrigido (CMC). Essa classe está disponível somente em sistemas Windows de 64 bits.

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAInfo_RawCMCEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Membros

A classe **MSMCAInfo \_ RawCMCEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MSMCAInfo \_ RawCMCEvent** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

TRUE, se esta instância da classe estiver ativa; caso contrário, **false**.

</dd> <dt>

**Count**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de registros de erro.

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

**Registros**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **\_ entrada MSMCAInfo**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de registros de erros da arquitetura de verificação de máquina (MCA). O número de registros de erro MCA na matriz é especificado pela propriedade **Count** .

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **MSMCAInfo \_ RawCMCEvent** é derivada de [**WmiEvent**](wmievent.md).

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

 

