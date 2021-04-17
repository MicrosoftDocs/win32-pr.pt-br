---
description: Contém um evento de plataforma corrigido (CPE). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: Classe MSMCAInfo_RawCorrectedPlatformEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762170"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a>\_Classe MSMCAInfo RawCorrectedPlatformEvent

A classe **MSMCAInfo \_ RawCorrectedPlatformEvent** contém um evento de plataforma corrigido (CPE). Essa classe está disponível somente em sistemas Windows de 64 bits.

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Membros

A classe **MSMCAInfo \_ RawCorrectedPlatformEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MSMCAInfo \_ RawCorrectedPlatformEvent** tem essas propriedades.

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

**Registros**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **\_ entrada MSMCAInfo**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de registros de erro de MCA. O número de registros de erro MCA na matriz é especificado pela propriedade **Count** .

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **MSMCAInfo \_ RawCorrectedPlatformEvent** é derivada de [**WmiEvent**](wmievent.md).

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

 

 




