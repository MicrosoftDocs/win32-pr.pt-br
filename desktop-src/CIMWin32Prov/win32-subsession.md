---
description: A \_ Associação de Subsessão do Win32 define as relações entre as sessões em que uma sessão faz parte ou utiliza outra sessão, por exemplo, em que uma sessão de terminal usa uma sessão de logon.
ms.assetid: 2269de22-b086-4f71-8b19-bc53e1c88dc7
ms.tgt_platform: multiple
title: Classe Win32_SubSession
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubSession
- Win32_SubSession.Antecedent
- Win32_SubSession.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: e575fddd5d869d7670aa3e42bf3f948badd7fd1b24befdf8839045c788e59634
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642646"
---
# <a name="win32_subsession-class"></a>\_Classe de Subsessão Win32

A \_ Associação de Subsessão do Win32 define as relações entre as sessões em que uma sessão faz parte ou utiliza outra sessão, por exemplo, em que uma sessão de terminal usa uma sessão de logon.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, AMENDMENT]
class Win32_SubSession : CIM_Dependency
{
  Win32_Session REF Antecedent;
  Win32_Session REF Dependent;
};
```

## <a name="members"></a>Membros

A classe de **\_ subsessão Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ subsessão Win32** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sessão Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) (Antecedent)
</dt> </dl>

Uma [**\_ sessão Win32**](win32-session.md) que descreve a sessão que tem uma subsessão.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sessão Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) (dependente)
</dt> </dl>

Uma [**\_ sessão Win32**](win32-session.md) que descreve a sessão que é a subsessão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

 
