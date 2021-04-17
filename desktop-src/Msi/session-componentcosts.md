---
description: A propriedade ComponentCosts do objeto Session retorna um objeto Recordlist que enumera o espaço em disco por unidade necessário para instalar um componente.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Propriedade Session. ComponentCosts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6ef4e3bfd441f5de61c0f3d69aea93d6cfd2ed8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754346"
---
# <a name="sessioncomponentcosts-property"></a>Propriedade Session. ComponentCosts

A propriedade ComponentCosts do objeto [**Session**](session-object.md) retorna um objeto [**recordlist**](recordlist-object.md) que enumera o espaço em disco por unidade necessário para instalar um componente. Essas informações são usadas pela interface do usuário para exibir o espaço em disco necessário para todas as unidades. Os custos de espaço em disco retornados estão em múltiplos de 512 bytes.

A propriedade ComponentCosts deve ser usada somente depois que o instalador concluir o [custo do arquivo](file-costing.md) e após a [ação CostFinalize](costfinalize-action.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Para obter o custo total, adicione os custos de todos os componentes mais o custo do mecanismo do instalador (componente = "").

ComponentCosts retorna um [**objeto recordlist**](recordlist-object.md). Cada registro no objeto Recordlist retornado tem os seguintes campos:



| Campo | Descrição                                          |
|-------|------------------------------------------------------|
| 1     | Nome da unidade/volume                                    |
| 2     | Custo final do espaço em disco em múltiplos de 512 bytes.     |
| 3     | Custo temporário de espaço em disco em múltiplos de 512 bytes. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




