---
description: A propriedade CostingComplete indica se o instalador concluiu o custo de espaço em disco.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Propriedade CostingComplete
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752858"
---
# <a name="costingcomplete-property"></a>Propriedade CostingComplete

A propriedade **CostingComplete** indica se o instalador concluiu o custo de espaço em disco. Essa propriedade pode ser usada para criar uma caixa de diálogo disparada se o custo não tiver sido concluído. A propriedade é definida dinamicamente durante o custo do espaço em disco e é definida como 1 assim que o custo é concluído. Essa propriedade é inicializada como 0 pela [ação CostFinalize](costfinalize-action.md).

## <a name="remarks"></a>Comentários

Para obter um exemplo de como criar um "Aguarde. . . "caixa de diálogo que aparece durante o custo de espaço em disco, consulte a seção [criação de uma condicional" Aguarde... " Caixa de mensagem](authoring-a-conditional-please-wait-------message-box.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




