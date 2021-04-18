---
description: Indica uma entrada de informações do MCA, correção de máquina corrigida (CMC) ou erro de plataforma corrigido (CPE). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: Classe MSMCAInfo_Entry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cda6abba06dc4d4f3fec3a4763391eee1fa81274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764260"
---
# <a name="msmcainfo_entry-class"></a>\_Classe de entrada MSMCAInfo

A classe de **\_ entrada MSMCAInfo** indica uma entrada de informações de MCA, verificação de máquina corrigida (CMC) ou erro de plataforma corrigido (CPE). Essa classe está disponível somente em sistemas Windows de 64 bits.

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a>Membros

A classe de **\_ entrada MSMCAInfo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ entrada MSMCAInfo** tem essas propriedades.

<dl> <dt>

**Dados**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de inteiros que contém um registro de erro MCA completo, conforme relatado pela camada de abstração do sistema (SAL). O SAL é o código gravado na ROM que o sistema operacional chama para executar operações dependentes da plataforma. É semelhante ao BIOS em uma plataforma x86.

</dd> <dt>

**Comprimento**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de bytes no registro de erros.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe de **\_ entrada MSMCAInfo** é derivada de [**MSMCAInfo**](msmcainfo.md).

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

[**MSMCAInfo**](msmcainfo.md)
</dt> </dl>

 

 




