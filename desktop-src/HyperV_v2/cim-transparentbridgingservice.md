---
description: Representa o aspecto de ponte transparente de um objeto CIM \_ SwitchService.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: CIM_TransparentBridgingService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8744bbac256d0cebc6d340ac83c4e8da746c03b298e2e3cd6c542310b3fc4914
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254976"
---
# <a name="cim_transparentbridgingservice-class"></a>Classe CIM \_ TransparentBridgingService

Representa o aspecto de ponte transparente de um [**objeto CIM \_ SwitchService.**](cim-switchservice.md)

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ TransparentBridgingService** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ TransparentBridgingService** tem essas propriedades.

<dl> <dt>

**AgingTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Segundos"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| BRIDGE-MIB.dot1dTpAgingTime")
</dt> </dl>

O período de tempo de tempo, em segundos, para o desacordo das informações de encaminhamento aprendidas dinamicamente. O padrão 802.1D-1990 recomenda um padrão de 300 segundos.

</dd> <dt>

**Fid**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Filtragem do Identificador de Banco de Dados usado por comutadores com conhecimento de VLAN que têm mais de um banco de dados de filtragem.

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

[**CIM \_ ForwardingService**](cim-forwardingservice.md)
</dt> </dl>

 

