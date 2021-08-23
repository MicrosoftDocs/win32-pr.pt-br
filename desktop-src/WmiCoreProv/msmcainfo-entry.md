---
description: Indica uma entrada de informações de MCA, CMC (verificação de computador corrigida) ou CPE (erro de plataforma) corrigida. Essa classe está disponível somente em sistemas de Windows de 64 bits.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: MSMCAInfo_Entry classe
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
ms.openlocfilehash: 8f6146d629678c1ee209738095fea901f0edb865bccb9aff2d4eeab02d18e773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640896"
---
# <a name="msmcainfo_entry-class"></a>Classe de entrada MSMCAInfo \_

A classe De entrada **MSMCAInfo \_** indica uma entrada MCA, uma CMC (verificação de máquina corrigida) ou uma entrada de informações de erro de plataforma corrigida (CPE). Essa classe está disponível somente em sistemas de Windows de 64 bits.

A sintaxe a seguir é simplificada do Managed Object Format (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a>Membros

A **classe De \_ entrada MSMCAInfo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe MSMCAInfo \_ Entry** tem essas propriedades.

<dl> <dt>

**Dados**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de inteiros que contém um registro de erro MCA completo, conforme relatado pela SAL (camada de abstração do sistema). O SAL é o código gravado em ROM que o sistema operacional chama para executar operações dependentes da plataforma. Ele é semelhante ao BIOS em uma plataforma x86.

</dd> <dt>

**Comprimento**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de bytes no registro de erro.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe De \_ entrada MSMCAInfo** é derivada de [**MSMCAInfo.**](msmcainfo.md)

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

[**MSMCAInfo**](msmcainfo.md)
</dt> </dl>

 

 




