---
description: Associa uma cabeça de vídeo com o controlador de vídeo que a inclui.
ms.assetid: D072DF7C-D55B-4203-9FE5-B395D1EC1632
title: Classe Msvm_VideoHeadOnController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHeadOnController
- Msvm_VideoHeadOnController.Antecedent
- Msvm_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11065c7b7a9e23b786697c3d4f0dbd63e67d6b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091556"
---
# <a name="msvm_videoheadoncontroller-class"></a>\_Classe Msvm VideoHeadOnController

Associa uma cabeça de vídeo com o controlador de vídeo que a inclui.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHeadOnController : CIM_VideoHeadOnController
{
  CIM_DisplayController REF Antecedent;
  Msvm_VideoHead        REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VideoHeadOnController** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VideoHeadOnController** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

O controlador de vídeo que inclui o cabeçalho.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ VideoHead**](msvm-videohead.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

O cabeçalho no dispositivo de vídeo.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ VideoHeadOnController** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_VIDEOHEADONCONTROLLER CIM**](cim-videoheadoncontroller.md)
</dt> <dt>

[**\_VIDEOHEADONCONTROLLER CIM**](/previous-versions//cc136950(v=vs.85))
</dt> <dt>

[Classes de vídeo](video-classes.md)
</dt> </dl>

 

