---
title: Adicionando ícones e menus de contexto com extensões de Shell
description: você pode melhorar a experiência de seus usuários com o Microsoft Windows Desktop Search (WDS) e o manipulador de protocolo implementando extensões de Shell.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9198fc56b8ca09e61909b1828d7d00b964bb12c0e13308583eb36a4e2211f3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976866"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a>Adicionando ícones e menus de contexto com extensões de Shell

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use [Windows pesquisa](../search/-search-3x-wds-overview.md) em vez disso.

você pode melhorar a experiência de seus usuários com o Microsoft Windows Desktop Search (WDS) e o manipulador de protocolo implementando extensões de Shell. Sem a extensão adicional, o manipulador de protocolo que você criar não incluirá as seguintes experiências de usuário:

-   O WDS não exibirá ícones específicos para seus resultados.
-   Quando os usuários clicam duas vezes em um item, a interface do usuário não responderá ao evento.
-   Quando os usuários clicam com o botão direito do mouse em um item, o menu de contexto não oferece suporte a nenhuma operação para o item.

As implementações mínimas de **IPersist** e **IPersistFolder** são exigidas pelo **IShellFolder** e uma implementação mínima de **IShellFolder** é necessária para **IContextMenu** e **IExtractIcon**, as duas interfaces que fornecem uma experiência de usuário mais direta.

 

## <a name="ipersist"></a>IPersist

A interface **IPersist** define o método único **GetClassID**, que é projetado para fornecer o CLSID de um objeto que pode ser armazenado de forma persistente no sistema.



| Método       | Descrição                                 |
|--------------|---------------------------------------------|
| GetClassID () | Retorna a ClassID do manipulador de protocolo |



 

> [!Note]
>
> O mesmo CLSID deve ser implementado para **IPersist**, **IPersistFolder** e **IShellFolder**.

 

 

## <a name="ipersistfolder"></a>IPersistFolder

A interface **IPersistFolder** é usada para inicializar objetos de pasta do Shell. A implementação dessa interface, que é derivada de **IPersist**, é como a pasta é informada onde está no namespace do Shell.



| Método       | Descrição                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| Initialize () | Instrui um objeto de pasta do Shell para se inicializar com base nas informações passadas e retorna S \_ OK |



 

> [!Note]
>
> O mesmo CLSID deve ser implementado para **IPersist**, **IPersistFolder** e **IShellFolder**.

 

Você não usa essa interface diretamente. Ele é usado pela implementação do sistema de arquivos da interface IShellFolder:: BindToObject quando Inicializa um objeto de pasta do Shell.

 

## <a name="ishellfolder"></a>IShellFolder

a interface **IShellFolder** é usada para gerenciar pastas e uma implementação parcial é necessária para que o ícone e as interfaces de contexto implementadas para um manipulador de protocolo se comportem corretamente na interface do usuário Windows Desktop Search results. A maior parte da funcionalidade necessária é exposta por meio do método **GetUIObjectOf** . Esse método permite que um suplemento consulte as interfaces **IExtractIcon** e **IContextMenu** .

A interface **IShellFolder** usa PIDLs em vez de URLs. Ao contrário dos requisitos de uma extensão de namespace completa, os suplementos podem usar uma estrutura IDL simples que contém apenas a URL.

Os métodos a seguir de **IShellFolder** devem ser implementados. Observe que cinco desses métodos exigem implementação mínima.



| Método             | Descrição                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject()     | Retorna E \_ NOTIMPL                                                                                                                                                                                          |
| BindToStorage()    | Retorna E \_ NOTIMPL                                                                                                                                                                                          |
| CreateViewObject () | Retorna E \_ NOTIMPL                                                                                                                                                                                          |
| SetNameOf()        | Retorna E \_ NOTIMPL                                                                                                                                                                                          |
| ParseDisplayName() | Converte uma URL para a estrutura PIDL                                                                                                                                                                        |
| CompareIDs()       | Compara dois valores de PIDL                                                                                                                                                                                    |
| GetDisplayNameOf() | Retorna a URL para um PIDL                                                                                                                                                                                  |
| GetUIObjectOf()    | Esse método é semelhante ao método OLE COM QueryInterface. Se um ícone for solicitado, o chamador solicitará o \_ IExtractIcon de IID; se um menu de contexto for solicitado, o chamador solicitará o IContextMenu de IID \_ . |



 

> [!Note]
>
> O mesmo CLSID deve ser implementado para **IPersist**, **IPersistFolder** e **IShellFolder**.

 

**IShellFolder** não é usado para enumerar pastas. Isso significa que o nome de exibição de uma pasta será a URL física. Isso pode ser alterado no futuro.

 

## <a name="icontextmenu"></a>IContextMenu

Quando o WDS exibe os resultados para o usuário, o usuário pode clicar com o botão direito do mouse em um item e ver um menu de contexto definido pela sua interface **IContextMenu** .

A ação padrão no menu de contexto é a mesma ação executada quando o item é clicado duas vezes. Sem as interfaces **IShellFolder** ou **IContextMenu** correspondentes para o item, o comportamento padrão de um evento de clique duplo é passar a URL como um argumento para a função ShellExecute.

 

## <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** recupera um ícone para a interface do usuário do WDS com base na URL no PIDL fornecido pelo seu manipulador de protocolo.

 

## <a name="code-sample"></a>Exemplo de código

O [código de exemplo da interface do usuário do manipulador de protocolo personalizado](-search-2x-wds-ph-ui-samplecode.md) demonstra uma implementação de **IShellFolder** e interfaces de suporte e inclui suporte para manipular o PIDLs.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Código de exemplo da interface do usuário do manipulador de protocolo personalizado](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalando e Registrando manipuladores de protocolo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




