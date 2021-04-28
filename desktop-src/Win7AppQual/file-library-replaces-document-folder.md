---
description: A biblioteca de arquivos substitui a pasta de documentos
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: A biblioteca de arquivos substitui a pasta de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699c645d574012a419f77538bcc58d61a4938120
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088374"
---
# <a name="file-library-replaces-document-folder"></a>A biblioteca de arquivos substitui a pasta de documentos

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -média  
**Frequência** -alta  











## <a name="description"></a>Descrição

As bibliotecas fornecem uma experiência de pasta centralizada para armazenamento de arquivos, pesquisa e acesso em vários locais, tanto locais quanto remotos.

Os locais padrão usados por caixas de diálogo de arquivo comuns (por exemplo, abrir e salvar) foram alterados da pasta de documentos para a biblioteca de documentos. A interface do usuário está inalterada, mas o usuário agora poderá exibir, procurar e pesquisar a biblioteca usando várias exibições de organização. Os arquivos serão salvos no local de salvamento padrão da biblioteca, a menos que o usuário altere o local de salvamento padrão ou escolha uma pasta diferente.

Os desenvolvedores podiam criar suas próprias bibliotecas ou adicionar locais a bibliotecas existentes usando a interface IShellLibrary. Os usuários podem encontrar bibliotecas usando o sistema de pastas conhecido (por exemplo, FOLDERid \_ DocumentsLibrary).

## <a name="manifestation-of-impact"></a>Manifestação do impacto

A biblioteca é, em si, um arquivo, e não uma pasta. Portanto, as manipulações de caminho podem resultar em erros devido à tentativa pelo aplicativo de concatenar arquivos em arquivos.

## <a name="solution"></a>Solução

Ao usar IFileDialog, você deve usar o método GetResult em vez de combinação de GetFolder e GetFilename como faria nas versões anteriores do sistema operacional. Use as APIs do shell sempre que possível para interagir com e manipular itens no namespace do Shell (por exemplo, IShellItem).

## <a name="leveraging-feature-capabilities"></a>Aproveitando os recursos do recurso

Se você quiser criar suas próprias bibliotecas ou adicionar locais a bibliotecas existentes, deverá usar a API IShellLibrary. As bibliotecas são pastas de shell próprias para que você possa enumerá-las assim como qualquer outra pasta do Shell.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilidade, desempenho, confiabilidade e teste de usabilidade

Usar a caixa de diálogo arquivo comum garantirá que os usuários possam salvar diretamente em suas bibliotecas.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   **Bibliotecas do Windows:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **Mantendo a sincronização com uma biblioteca:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 



