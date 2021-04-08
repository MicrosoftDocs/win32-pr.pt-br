---
description: Um componente é uma parte do aplicativo ou produto a ser instalado.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Componentes do Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922012"
---
# <a name="windows-installer-components"></a>Componentes do Windows Installer

Um componente é uma parte do aplicativo ou produto a ser instalado. Exemplos de componentes incluem arquivos únicos, um grupo de arquivos relacionados, objetos COM, registro, chaves do registro, atalhos, recursos, bibliotecas agrupadas em um diretório ou partes compartilhadas de código como MFC ou DAO.

O serviço instalador instala ou remove um componente como uma única parte coerente. Ele controla cada componente pelo respectivo GUID de ID de componente especificado na coluna ComponentID da [tabela de componentes](component-table.md).

> [!Note]  
> Dois componentes que compartilham a mesma ID de componente são tratados como várias instâncias do mesmo componente, independentemente de seu conteúdo real. Apenas uma única instância de qualquer componente é instalada no computador de um usuário. Por isso, vários recursos ou aplicativos podem compartilhar alguns componentes.

 

Como os componentes são normalmente compartilhados, o autor de um pacote de instalação deve seguir regras estritas ao especificar os componentes de um recurso ou aplicativo. Isso é essencial para a operação correta do mecanismo de contagem de referência Windows Installer. Para obter mais informações, consulte [organizando aplicativos em componentes](organizing-applications-into-components.md).

Em resumo, essas regras são:

-   Cada componente deve ser armazenado em uma única pasta.
-   Nenhum arquivo, entrada de registro, atalho ou outros recursos já devem ser enviados como um membro de mais de um componente. Isso se aplica a produtos, versões de produtos e empresas.

Para obter mais informações sobre como usar componentes, consulte

-   [Instalando um componente ausente](installing-a-missing-component.md)
-   [Instalando componentes, arquivos, fontes e chaves do registro permanentes](installing-permanent-components-files-fonts-registry-keys.md)
-   [Usando componentes qualificados](using-qualified-components.md)
-   [Usando componentes transitivos](using-transitive-components.md)
-   [Trabalhando com recursos e componentes](working-with-features-and-components.md)
-   [Criando um pacote grande](authoring-a-large-package.md)
-   [Verificando a instalação de recursos, componentes, arquivos](checking-the-installation-of-features-components-files.md)
-   [Pesquisando um componente ou recurso desfeito](searching-for-a-broken-feature-or-component.md)
-   [Publicando produtos, recursos e componentes](publishing-products-features-and-components.md)

 

 



