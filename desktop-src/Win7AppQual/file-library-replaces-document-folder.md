---
description: Biblioteca de Arquivos substitui a pasta do documento
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: Biblioteca de Arquivos substitui a pasta do documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e8d08b176ebf4b5801a73695ea03f60a38eeb5a1ca51e1d90d9119dae5fcaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329666"
---
# <a name="file-library-replaces-document-folder"></a>Biblioteca de Arquivos substitui a pasta do documento

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** – Windows 7  
**Servidores** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Gravidade –** Média  
**Frequência** – Alta  











## <a name="description"></a>Descrição

As bibliotecas fornecem uma experiência centralizada como pasta para armazenamento de arquivos, pesquisa e acesso em vários locais, locais e remotos.

Os locais padrão usados por caixas de diálogo de arquivo comuns (por exemplo, Abrir e Salvar) foram alterados da Pasta do Documento para a Biblioteca de Documentos. O Interface do Usuário está inalterado, mas agora o usuário poderá exibir, procurar e pesquisar a Biblioteca usando várias exibições de organização. Os arquivos serão salvos no local de salvar padrão biblioteca, a menos que o usuário mude o local de salvar padrão ou escolha uma pasta diferente.

Os desenvolvedores podem criar suas próprias bibliotecas ou adicionar locais a bibliotecas existentes usando a interface IShellLibrary. Os usuários podem encontrar bibliotecas usando o sistema pasta conhecida (por exemplo, FOLDERID \_ DocumentsLibrary).

## <a name="manifestation-of-impact"></a>Manifestação de impacto

A Biblioteca é um arquivo e não uma pasta. Portanto, as manipulações de caminho podem resultar em erros devido à tentativa do aplicativo de concatenar arquivos em arquivos.

## <a name="solution"></a>Solução

Ao usar IFileDialog, você deve usar o método GetResult em vez da combinação de GetFolder e GetFilename como faria nas versões anteriores do sistema operacional. Use as APIs do Shell sempre que possível para interagir e manipular itens no Namespace do Shell (por exemplo, IShellItem).

## <a name="leveraging-feature-capabilities"></a>Aproveitando as funcionalidades de recursos

Se você quiser criar suas próprias bibliotecas ou adicionar locais a bibliotecas existentes, deverá usar a API IShellLibrary. As bibliotecas são pastas de shell para que você possa enumerá-las como qualquer outra Pasta do Shell.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Teste de compatibilidade, desempenho, confiabilidade e usabilidade

Usar a caixa de diálogo de arquivo comum garantirá que os usuários possam salvar diretamente em suas bibliotecas.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   **Windows bibliotecas:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **Mantendo a sincronização com uma biblioteca:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 



