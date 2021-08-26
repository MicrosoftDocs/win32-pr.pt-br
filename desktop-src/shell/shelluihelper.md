---
description: implementado pelo Shell para ajudar o script e os desenvolvedores de Visual Basic da Microsoft a usar alguns dos recursos disponíveis no Shell. O objeto ShellUIHelper não tem nenhuma propriedade ou evento. Os métodos são fornecidos para adicionar itens ao shell.
title: Objeto ShellUIHelper (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: f254bd218024b3d1df15a826da701b1f010ae616
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473322"
---
# <a name="shelluihelper-object"></a>Objeto ShellUIHelper

implementado pelo Shell para ajudar o script e os desenvolvedores de Visual Basic da Microsoft a usar alguns dos recursos disponíveis no Shell. O objeto **ShellUIHelper** não tem nenhuma propriedade ou evento. Os métodos são fornecidos para adicionar itens ao shell.

## <a name="members"></a>Membros

O objeto **ShellUIHelper** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **ShellUIHelper** tem esses métodos.




| Método | Descrição | 
|--------|-------------|
| <a href="shelluihelper-addchannel.md"><strong>Addchannel</strong></a> | Adiciona um novo canal à lista de canais no menu <strong>favoritos</strong> do Internet Explorer e à barra de <strong>canais</strong> na área de trabalho.<br /><blockquote>[!Note]<br />não há mais suporte para esse método no Windows Vista. Nesse sistema operacional, ele retorna E_NOTIMPL.</blockquote><br /> | 
| <a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a> | Adiciona um item à área de trabalho ativa.<br /> | 
| <a href="shelluihelper-addfavorite.md"><strong>Addfavorito</strong></a> | Exibe a interface do usuário padrão para criar um item favorito. A interface do usuário é inicializada para os parâmetros especificados.<br /> | 
| <a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a> | Indica se uma URL especificada é assinada.<br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>O textdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 




