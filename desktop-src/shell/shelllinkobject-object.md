---
description: Gerencia links do Shell. Esse objeto torna grande parte da funcionalidade da interface IShellLink disponível para scripts de aplicativos.
title: Objeto ShellLinkObject (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968195"
---
# <a name="shelllinkobject-object"></a>Objeto ShellLinkObject

Gerencia links do Shell. Esse objeto torna grande parte da funcionalidade da interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) disponível para scripts de aplicativos.

## <a name="members"></a>Membros

O objeto **ShellLinkObject** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **ShellLinkObject** tem esses métodos.



| Método                                                     | Descrição                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetIconLocation**](shelllinkobject-geticonlocation.md) | Obtém o local do ícone atribuído ao link.<br/>                                 |
| [**Resolver**](shelllinkobject-resolve.md)                 | Procura o destino de um link do Shell, mesmo que o destino tenha sido movido ou renomeado.<br/> |
| [**Salvar**](shelllinkobject-save.md)                       | Salva todas as alterações no link.<br/>                                                      |
| [**SetIconLocation**](shelllinkobject-seticonlocation.md) | Define o local do ícone atribuído ao link.<br/>                                 |



 

### <a name="properties"></a>Propriedades

O objeto **ShellLinkObject** tem essas propriedades.



| Propriedade                                                                | Tipo de acesso           | Description                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Argumentos**](shelllinkobject-arguments.md)<br/>               | Leitura/gravação<br/> | Contém os argumentos de um link.<br/>                                                                   |
| [**Descrição**](shelllinkobject-description.md)<br/>           | Leitura/gravação<br/> | Obtém ou define a descrição do link.<br/>                                                      |
| [**Tecla**](shelllinkobject-hotkey.md)<br/>                     | Leitura/gravação<br/> | Obtém ou define o atalho de teclado para o link.<br/>                                               |
| [**Caminho**](shelllinkobject-path.md)<br/>                         | Leitura/gravação<br/> | Obtém ou define o caminho para o objeto de link.<br/>                                                      |
| [**ShowCommand**](shelllinkobject-showcommand.md)<br/>           | Leitura/gravação<br/> | Obtém ou define o estado de exibição inicial (dimensionado, minimizado ou maximizado) do comando do link.<br/> |
| [**WorkingDirectory**](shelllinkobject-workingdirectory.md)<br/> | Leitura/gravação<br/> | Obtém ou define o diretório de trabalho especificado no link.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Links do Shell](./links.md)
</dt> </dl>

 

 
