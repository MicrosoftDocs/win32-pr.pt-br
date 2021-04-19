---
description: A propriedade UILevel do objeto instalador é uma propriedade de leitura/gravação que indica o tipo de interface do usuário a ser usado ao abrir e processar pacotes subsequentes no espaço do processo atual.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Propriedade Installer. UILevel
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
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747329"
---
# <a name="installeruilevel-property"></a>Propriedade Installer. UILevel

A propriedade **UILevel** do objeto [**instalador**](installer-object.md) é uma propriedade de leitura/gravação que indica o tipo de interface do usuário a ser usado ao abrir e processar pacotes subsequentes no espaço do processo atual.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários



| Nível da interface do usuário   | Valor | Descrição                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msiUILevelNoChange     | 0     | Não altera o nível da interface do usuário.                                                                                                                                                                          |
| msiUILevelDefault      | 1     | Usa o nível de interface do usuário padrão.                                                                                                                                                                             |
| msiUILevelNone         | 2     | Instalação silenciosa.                                                                                                                                                                               |
| msiUILevelBasic        | 3     | Progresso simples e tratamento de erros.                                                                                                                                                                |
| msiUILevelReduced      | 4     | Caixas de diálogo de interface do usuário e assistente criadas suprimidas.                                                                                                                                                    |
| msiUILevelFull         | 5     | IU criada com assistentes, progresso e erros.                                                                                                                                                    |
| msiUILevelHideCancel   | 32    | Se combinado com o valor msiUILevelBasic, o instalador mostrará as caixas de diálogo de progresso, mas não exibirá um botão **Cancelar** na caixa de diálogo para impedir que os usuários cancelem a instalação. |
| msiUILevelProgressOnly | 64    | Se combinado com o valor msiUILevelBasic, o instalador exibirá as caixas de diálogo de progresso, mas não exibirá caixas de diálogo modais ou caixas de diálogo de erro.                                        |
| msiUILevelEndDialog    | 128   | Se combinado com qualquer valor acima, o instalador exibirá uma caixa de diálogo modal no final de uma instalação bem-sucedida ou se houver um erro. Nenhuma caixa de diálogo será exibida se o usuário cancelar. |



 

Consulte também, [determinando o nível da interface do usuário de uma ação personalizada](determining-ui-level-from-a-custom-action.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




