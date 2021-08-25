---
description: Gerencia links do Shell. Esse objeto disponibiliza grande parte da funcionalidade da interface IShellLink para aplicativos de script.
title: Objeto ShellLinkObject (Shldisp.h)
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
ms.openlocfilehash: 9908fa86b79ff230c2c6320685cd605a97c9b0747db31cc395f8f449ae2fbfa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941486"
---
# <a name="shelllinkobject-object"></a>Objeto ShellLinkObject

Gerencia links do Shell. Esse objeto disponibiliza grande parte da funcionalidade da interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para aplicativos de script.

## <a name="members"></a>Membros

O **objeto ShellLinkObject** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto ShellLinkObject** tem esses métodos.



| Método                                                     | Descrição                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetIconLocation**](shelllinkobject-geticonlocation.md) | Obtém o local do ícone atribuído ao link.<br/>                                 |
| [**Resolver**](shelllinkobject-resolve.md)                 | Procura o destino de um link do Shell, mesmo que o destino tenha sido movido ou renomeado.<br/> |
| [**Salvar**](shelllinkobject-save.md)                       | Salva todas as alterações no link.<br/>                                                      |
| [**SetIconLocation**](shelllinkobject-seticonlocation.md) | Define o local do ícone atribuído ao link.<br/>                                 |



 

### <a name="properties"></a>Propriedades

O **objeto ShellLinkObject** tem essas propriedades.



| Propriedade                                                                | Tipo de acesso           | Descrição                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Argumentos**](shelllinkobject-arguments.md)<br/>               | Leitura/gravação<br/> | Contém os argumentos de um link.<br/>                                                                   |
| [**Descrição**](shelllinkobject-description.md)<br/>           | Leitura/gravação<br/> | Obtém ou define a descrição do link.<br/>                                                      |
| [**Hotkey**](shelllinkobject-hotkey.md)<br/>                     | Leitura/gravação<br/> | Obtém ou define o atalho de teclado para o link.<br/>                                               |
| [**Caminho**](shelllinkobject-path.md)<br/>                         | Leitura/gravação<br/> | Obtém ou define o caminho para o objeto de link.<br/>                                                      |
| [**ShowCommand**](shelllinkobject-showcommand.md)<br/>           | Leitura/gravação<br/> | Obtém ou define o estado de exibição inicial (dimensionado, minimizado ou maximizada) do comando do link.<br/> |
| [**WorkingDirectory**](shelllinkobject-workingdirectory.md)<br/> | Leitura/gravação<br/> | Obtém ou define o diretório de trabalho especificado no link.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Shell Links](./links.md)
</dt> </dl>

 

 
