---
title: Implementando o objeto COM do menu de contexto
description: Uma extensão de menu de contexto é um objeto COM implementado como um servidor em processo.
ms.assetid: 362dd8e5-1518-4bf4-ac53-115263cd6c62
ms.tgt_platform: multiple
keywords:
- menu de contexto do objeto COM AD
- menu de contexto COM o AD Object, implementando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34d6b487d130327b379ed845f2d0157f2b28056
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105752989"
---
# <a name="implementing-the-context-menu-com-object"></a>Implementando o objeto COM do menu de contexto

Uma extensão de menu de contexto é um objeto COM implementado como um servidor em processo. A extensão do menu de contexto deve implementar as interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Uma extensão de menu de contexto é instanciada quando o usuário exibe o menu de contexto de um objeto de uma classe para a qual a extensão do menu de contexto foi registrada.

## <a name="implementing-ishellextinit"></a>Implementando IShellExtInit

Depois que o objeto COM da extensão do menu de contexto é instanciado, o método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) é chamado. **IShellExtInit:: Initialize** fornece a extensão do menu de contexto com um objeto [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) que contém dados pertinentes ao objeto de diretório ao qual o menu de contexto se aplica.

O [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contém dados no formato [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) . O formato de dados **CFSTR \_ DSOBJECTNAMES** é um **HGLOBAL** que contém uma estrutura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) . A estrutura **DSOBJECTNAMES** contém dados sobre o objeto de diretório ao qual a extensão de folha de propriedades se aplica.

O [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) também contém dados no formato [**de \_ \_ Opções de \_ especificação \_ de exibição CFSTR DS**](cfstr-ds-display-spec-options.md) . O formato de dados de **Opções de especificação de \_ \_ exibição CFSTR \_ \_ DS** é um **HGLOBAL** que contém uma estrutura [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) . O **DSDISPLAYSPECOPTIONS** contém dados de configuração para uso pela extensão.

Se qualquer valor diferente de **S \_ OK** for retornado de [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), a extensão do menu de contexto não será usada.

Os parâmetros *pidlFolder* e *HkeyProgID* do método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) não são usados.

## <a name="implementing-icontextmenu"></a>Implementando IContextMenu

Após [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) retornar, o método [**IContextMenu:: QueryContextMenu**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) será chamado para obter o item de menu ou os itens que a extensão do menu de contexto adicionará. A implementação de **QueryContextMenu** é razoavelmente simples. A extensão do menu de contexto adiciona seus itens de menu usando o [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) ou a função semelhante. Os identificadores de comando de menu devem ser maiores ou iguais a *idCmdFirst* e devem ser menores que *idCmdLast*. **QueryContextMenu** deve retornar o maior identificador numérico adicionado ao menu mais um. A melhor maneira de atribuir identificadores de comando de menu é iniciar em zero e trabalhar em sequência. Se a extensão do menu de contexto não precisar de nenhum item de menu, ela deverá simplesmente não adicionar nenhum item ao menu e retornar zero de **QueryContextMenu**.

[**IContextMenu:: GetCommandString**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) é chamado para recuperar dados textuais para o item de menu, como texto de ajuda a ser exibido para o item de menu. É possível que o host do menu de contexto use cadeias de caracteres Unicode enquanto a extensão usa cadeias de caracteres ANSI. Por isso, os casos **de \_ GCS helptexta**, **GCS \_ HELPTEXTW**, **GCS \_ verba** e **GCS \_ VERBW** devem ser tratados individualmente. A implementação desse método é opcional.

[**IContextMenu:: InvokeCommand**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) é chamado quando um dos itens de menu instalados pela extensão do menu de contexto é selecionado. O menu de contexto executa ou inicia as ações desejadas em resposta a esse método.

 

 