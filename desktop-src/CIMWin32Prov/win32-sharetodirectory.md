---
description: A \_ classe WMI de associação ShareToDirectory do Win32 relaciona um recurso compartilhado no sistema de computador e o diretório no qual ele está mapeado.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Classe Win32_ShareToDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646230"
---
# <a name="win32_sharetodirectory-class"></a>\_Classe Win32 ShareToDirectory

A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ ShareToDirectory do Win32** relaciona um recurso compartilhado no sistema de computador e o diretório no qual ele está mapeado.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ ShareToDirectory** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ ShareToDirectory** tem essas propriedades.

<dl> <dt>

**Compartilhe**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ compartilhamento do Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| compartilhamento WMI Win32 \_ ")
</dt> </dl>

Referência à instância que representa as propriedades de um recurso compartilhado disponível por meio do diretório.

</dd> <dt>

**Sharedelement**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ diretório CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("diretório CIM CIM \| \_ ")
</dt> </dl>

Referência à instância que representa as propriedades do diretório que foi mapeado para um recurso compartilhado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
