---
description: A \_ associação CIM PackageAlarm representa a relação na qual um dispositivo de alarme é instalado como parte de um pacote. A instalação indica problemas com o ambiente do pacote&\# 8212; seu estado de segurança ou sua integridade geral.
ms.assetid: 4911502a-de9c-46b4-91f6-a042c69fd052
ms.tgt_platform: multiple
title: Classe CIM_PackageAlarm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageAlarm
- CIM_PackageAlarm.Dependent
- CIM_PackageAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 29aae3a2c1093e026356ea7a096f8b673673f67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088986"
---
# <a name="cim_packagealarm-class"></a>\_Classe CIM PackageAlarm

A associação [**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) representa a relação na qual um dispositivo de alarme é instalado como parte de um pacote. A instalação indica problemas com o ambiente do pacote seu estado de segurança ou sua integridade geral.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Aggregation, UUID("{FAF76B90-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageAlarm : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_AlarmDevice     REF Antecedent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ PackageAlarm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ PackageAlarm** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ AlarmDevice**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um [**\_ AlarmDevice CIM**](cim-alarmdevice.md) que descreve o dispositivo de alarme para o pacote.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ PhysicalPackage**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que descreve o pacote físico cuja integridade, segurança, ambiente etc. é alarmante.

</dd> </dl>

## <a name="remarks"></a>Comentários

**CIM \_ PackageAlarm** é derivado da [**\_ dependência CIM**](cim-dependency.md).

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

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

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

