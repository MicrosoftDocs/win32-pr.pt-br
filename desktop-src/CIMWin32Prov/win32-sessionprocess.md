---
description: A \_ classe WMI de associação do Win32 SessionProcess representa uma associação entre uma sessão de logon e os processos associados a essa sessão.
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Classe Win32_SessionProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754385"
---
# <a name="win32_sessionprocess-class"></a>\_Classe Win32 SessionProcess

A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ SessionProcess** representa uma associação entre uma sessão de logon e os processos associados a essa sessão.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ SessionProcess** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ SessionProcess** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ LogonSession**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**Key**](../wmisdk/key-qualifier.md)
</dt> </dl>

Um [**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) que representa a sessão que está relacionada ao processo.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ processo Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("dependente"), [**chave**](../wmisdk/key-qualifier.md)
</dt> </dl>

Um [**\_ processo Win32**](win32-processor.md) que representa o processo associado à sessão.

</dd> </dl>

## <a name="remarks"></a>Comentários

**Win32 \_ SessionProcess** retorna todas as sessões para o administrador quando conectado com privilégios elevados ou quando executado remotamente. Essa é uma extensão para o comportamento da classe.

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

[**\_SessionResource Win32**](win32-sessionresource.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
