---
title: Registrando o objeto COM do menu de contexto em um especificador de exibição
description: Este tópico mostra as chaves do registro que precisam ser modificadas para registrar um objeto COM do menu de contexto.
ms.assetid: 389bc249-4849-4763-9d1b-b35598a51050
ms.tgt_platform: multiple
keywords:
- Registrando o objeto COM do menu de contexto em um especificador de exibição
- menu de contexto do objeto COM AD, registrando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae30c1a60a1a0bc5a8ec388a3578ab13829c95
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007295"
---
# <a name="registering-the-context-menu-com-object-in-a-display-specifier"></a>Registrando o objeto COM do menu de contexto em um especificador de exibição

Quando você usa COM para criar uma DLL de extensão de menu de contexto para um serviço de diretório Active Directory, a extensão deve ser registrada com o registro do Windows e Active Directory Domain Services para notificar os snap-ins administrativos do MMC do Active Directory e o Shell do Windows da extensão.

## <a name="registering-in-the-windows-registry"></a>Registrando no registro do Windows

Como todos os servidores COM, uma extensão de menu de contexto deve ser registrada no registro. A extensão é registrada sob a chave a seguir.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*<clsid>* é a representação de cadeia de caracteres do CLSID, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . Sob a *<clsid>* chave, há uma chave **InprocServer32** que identifica o objeto como um servidor no processo de 32 bits. Na chave **InprocServer32** , o local da dll é especificado no valor padrão e o modelo de threading é especificado no valor de **ThreadingModel** . Toda extensão de menu de contexto deve usar o modelo de Threading "Apartment".

## <a name="registering-with-active-directory-domain-services"></a>Registrando com Active Directory Domain Services

O registro de extensão do menu de contexto é específico para uma localidade. Se a extensão do menu de contexto se aplicar a todas as localidades, ela deverá ser registrada no objeto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) da classe Object em todos os subcontêineres de localidade no contêiner exibir especificadores. Se a extensão do menu de contexto for localizada para uma determinada localidade, ela deverá ser registrada no objeto **displaySpecifier** no subcontêiner dessa localidade. Para obter mais informações sobre o contêiner e as localidades dos especificadores de exibição, consulte [Exibir especificadores de exibição](display-specifiers.md) e [contêiner DisplaySpecifiers](displayspecifiers-container.md).

Há dois atributos de especificador de exibição para os quais um item de extensão de menu de contexto pode ser registrado. Esses são [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) e [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu).

O atributo [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) identifica os menus de contexto administrativos a serem exibidos em Active Directory snap-ins administrativos. O menu de contexto é exibido quando o usuário exibe o menu de contexto para objetos da classe apropriada em um dos snap-ins administrativos do MMC Active Directory.

O atributo [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) identifica os menus de contexto do usuário final a serem exibidos no Shell do Windows. O menu de contexto é exibido quando o usuário exibe o menu de contexto para objetos da classe apropriada no Windows Explorer. A partir do Windows Server 2003, o Shell do Windows não exibe mais objetos de Active Directory Domain Services.

Todos esses atributos têm valores múltiplos.

Ao registrar uma extensão de menu de contexto, os valores para os atributos [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) e [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) exigem o formato a seguir.


```C++
<order number>,<clsid>
```



O " &lt; número do pedido &gt; " é um número sem sinal que representa a posição do item no menu de contexto. Quando um menu de contexto é exibido, os valores são classificados usando uma comparação de "número de &lt; ordem" de cada valor &gt; . Se mais de um valor tiver o mesmo " &lt; número do pedido &gt; ", essas extensões de menu de contexto serão carregadas na ordem em que são lidas do servidor de Active Directory. Se possível, use um " &lt; número de pedido" não existente &gt; , ou seja, um que não tenha sido usado por outros valores na propriedade. Não há posição e lacunas de início indicadas na sequência " &lt; número do pedido &gt; ".

O " &lt; CLSID &gt; " é a representação de cadeia de caracteres do CLSID, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

No Shell do Windows, há suporte para itens de menu de contexto de seleção múltipla. Nesse caso, a extensão do menu de contexto é invocada para cada objeto selecionado. Em Active Directory snap-ins administrativos, também há suporte para itens de extensão de menu de contexto de seleção múltipla. Nesse caso, a estrutura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) conterá uma estrutura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) para cada objeto de diretório selecionado.

> [!IMPORTANT]
> Para o Shell do Windows, as informações do especificador de exibição são recuperadas no logon do usuário e armazenadas em cache para a sessão do usuário. Para os snap-ins administrativos, os dados do especificador de exibição são recuperados quando o snap-in é carregado e armazenado em cache durante a duração do processo. Para o Shell do Windows, isso significa que as alterações para os especificadores de exibição entram em vigor após o usuário fazer logoff e logon novamente. Para os snap-ins administrativos, as alterações entram em vigor quando o snap-in ou o arquivo de console é recarregado, ou seja, se você iniciar uma nova instância do arquivo de console ou nova instância de Mmc.exe e adicionar o snap-in, os dados do especificador de exibição mais recentes serão recuperados.

 

Para obter mais informações e um exemplo de código de como implementar uma extensão de menu de contexto, consulte [exemplo de código para implementação do objeto com do menu de contexto](example-code-for-implementation-of-the-context-menu-com-object.md).

 

 