---
description: A propriedade UILevel do objeto Installer é uma propriedade de leitura/gravação que indica o tipo de interface do usuário a ser usada ao abrir e processar pacotes subsequentes dentro do espaço de processo atual.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Propriedade Installer.UILevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3004675ee8e07c3503ec4442832c00975364066fa4a0c770b0b081fc7b64c3c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043566"
---
# <a name="installeruilevel-property"></a>Propriedade Installer.UILevel

A **propriedade UILevel** do objeto [**Installer**](installer-object.md) é uma propriedade de leitura/gravação que indica o tipo de interface do usuário a ser usada ao abrir e processar pacotes subsequentes dentro do espaço de processo atual.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários



| Nível de interface do usuário   | Valor | Descrição                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msiUILevelNoChange     | 0     | Não altera o nível da interface do usuário.                                                                                                                                                                          |
| msiUILevelDefault      | 1     | Usa o nível de interface do usuário padrão.                                                                                                                                                                             |
| msiUILevelNone         | 2     | Instalação silenciosa.                                                                                                                                                                               |
| msiUILevelBasic        | 3     | Progresso simples e tratamento de erros.                                                                                                                                                                |
| msiUILevelReduced      | 4     | Caixas de diálogo da interface do usuário e do assistente autoradas suprimidas.                                                                                                                                                    |
| msiUILevelFull         | 5     | Interface do usuário com assistentes, progresso e erros.                                                                                                                                                    |
| msiUILevelHideCancel   | 32    | Se combinado com o valor msiUILevelBasic, o instalador mostrará caixas de diálogo de progresso, mas não exibirá um botão Cancelar na caixa de diálogo para impedir que os usuários cancelem **a** instalação. |
| msiUILevelProgressOnly | 64    | Se combinado com o valor msiUILevelBasic, o instalador exibirá caixas de diálogo de progresso, mas não exibirá nenhuma caixa de diálogo modal ou caixas de diálogo de erro.                                        |
| msiUILevelEndDialog    | 128   | Se combinado com qualquer valor acima, o instalador exibirá uma caixa de diálogo modal no final de uma instalação bem-sucedida ou se houver um erro. Nenhuma caixa de diálogo será exibida se o usuário cancelar. |



 

Consulte também [Determinando o nível da interface do usuário de uma ação personalizada.](determining-ui-level-from-a-custom-action.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




