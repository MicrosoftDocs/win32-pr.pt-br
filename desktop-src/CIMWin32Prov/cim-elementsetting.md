---
description: A \_ classe CIM ElementSetting representa a associação entre os elementos do sistema gerenciado e a classe de configuração definida para eles.
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: Classe CIM_ElementSetting (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749100"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a>Classe CIM_ElementSetting (provedores WMI CIMWin32)

A classe **CIM \_ ElementSetting** representa a associação entre os elementos do sistema gerenciado e a classe de configuração definida para eles.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ElementSetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ElementSetting** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à função do objeto [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) da Associação ElementSetting do **CIM \_** . O elemento de sistema gerenciado associado fornece o elemento que implementa a configuração do elemento.

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ configuração de CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à função do objeto de [**\_ configuração CIM**](cim-setting.md) da Associação **\_ ElementSetting do CIM** . A configuração associada fornece a configuração que implementa a configuração do elemento.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe. Para classes derivadas do **CIM \_ ElementSetting**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




