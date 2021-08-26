---
description: Associa um serviço de ponte transparente a uma entrada de seu banco de dados de encaminhamento.
ms.assetid: 6db93e71-c9b7-4710-a9ee-99a1055cfd82
title: CIM_TransparentBridgingDynamicForwarding classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingDynamicForwarding
- CIM_TransparentBridgingDynamicForwarding.Antecedent
- CIM_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 931b556cad32a7e83f82798c277e65995aa4318156a3f423a9fe2d7e057c252f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980786"
---
# <a name="cim_transparentbridgingdynamicforwarding-class"></a>Classe CIM \_ TransparentBridgingDynamicForwarding

Associa um serviço de ponte transparente a uma entrada de seu banco de dados de encaminhamento.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingDynamicForwarding : CIM_Dependency
{
  CIM_TransparentBridgingService REF Antecedent;
  CIM_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ TransparentBridgingDynamicForwarding** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ TransparentBridgingDynamicForwarding** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ TransparentBridgingService**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Uma [**referência cim \_ TransparentBridgingService**](cim-transparentbridgingservice.md) ao serviço de ponte transparente.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ DynamicForwardingEntry**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente"), [**Fraco**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Uma [**referência cim \_ DynamicForwardingEntry**](cim-dynamicforwardingentry.md) à entrada de banco de dados de encaminhamento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Dependência cim \_**](cim-dependency.md)
</dt> </dl>

 

