---
description: A classe de local do CIM \_ representa a posição e o endereço de um elemento físico.
ms.assetid: c1ec467c-a338-4beb-a8fe-1ebc5b05c754
ms.tgt_platform: multiple
title: Classe CIM_Location
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Location
- CIM_Location.Address
- CIM_Location.Name
- CIM_Location.PhysicalPosition
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd5a1c1c23d07020b45c1c5979a941f01baff0d0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164060"
---
# <a name="cim_location-class"></a>\_Classe de local CIM

A classe de **\_ local do CIM** representa a posição e o endereço de um elemento físico.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B67-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Location
{
  string Address;
  string Name;
  string PhysicalPosition;
};
```

## <a name="members"></a>Membros

A classe de **\_ local do CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ local CIM** tem essas propriedades.

<dl> <dt>

**Endereço**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Cadeia de caracteres de forma livre que indica uma rua ou outro tipo de endereço para o local do elemento físico.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Cadeia de caracteres de forma livre que define um rótulo para o local e que faz parte da chave do objeto.

</dd> <dt>

**PhysicalPosition**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Cadeia de caracteres de forma livre que indica o posicionamento de um elemento físico. Ele pode especificar informações de slot em uma placa de hospedagem, montar um site em um gabinete ou informações de latitude e longitude. Ele faz parte da chave do objeto de **\_ local do CIM** .

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe. Para classes derivadas do **\_ local do CIM**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

