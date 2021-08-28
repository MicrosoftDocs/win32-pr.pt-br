---
description: A propriedade ComponentCosts do objeto Session retorna um objeto RecordList enumerando o espaço em disco por unidade necessário para instalar um componente.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Propriedade Session.ComponentCosts
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
ms.openlocfilehash: 643996bccd352695651fb55f2ddcb33c0888773f4d99283f646a7fcb498c4074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629516"
---
# <a name="sessioncomponentcosts-property"></a>Propriedade Session.ComponentCosts

A propriedade ComponentCosts do objeto [**Session**](session-object.md) retorna um objeto [**RecordList**](recordlist-object.md) enumerando o espaço em disco por unidade necessário para instalar um componente. Essas informações são usadas pela interface do usuário para exibir o espaço em disco necessário para todas as unidades. Os custos de espaço em disco retornados estão em múltiplos de 512 bytes.

A propriedade ComponentCosts só deve ser usada [](file-costing.md) depois que o instalador tiver concluído o custo do arquivo e após a [ação CostFinalize](costfinalize-action.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Para obter o custo total, adicione os custos de todos os componentes mais o custo do mecanismo do instalador (Componente = "").

ComponentCosts retorna um [**objeto RecordList**](recordlist-object.md). Cada registro no objeto RecordList retornado tem os seguintes campos:



| Campo | Descrição                                          |
|-------|------------------------------------------------------|
| 1     | Nome do volume/unidade                                    |
| 2     | Custo final de espaço em disco em múltiplos de 512 bytes.     |
| 3     | Custo temporário de espaço em disco em múltiplos de 512 bytes. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession é definido como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




