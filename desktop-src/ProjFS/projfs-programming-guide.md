---
title: Guia de programação do sistema de arquivos projetado
description: Informações conceituais sobre como implementar um aplicativo de provedor ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: d935c99b73e11a2110e739a4e45fdde0f7a24300a2664a2b25d6217bd2235fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792539"
---
# <a name="projected-file-system-projfs-programming-guide"></a>Guia de programação do sistema de arquivos projetado (ProjFS)

o sistema de arquivos Windows projetado (ProjFS) permite que um aplicativo de modo de usuário chamado de "provedor" faça o projeto de dados hierárquicos no sistema de arquivos, fazendo com que ele apareça como arquivos e diretórios no sistema de arquivos.

## <a name="in-this-section"></a>Nesta seção

| Tópico                                                                                                       | Descrição |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Visão geral do provedor](provider-overview.md)                                                                   | Visão geral conceitual de um aplicativo de provedor.
| [Estado do cache na raiz de virtualização](cache-state.md)                                                    | Descreve os diferentes Estados de cache que um arquivo ou diretório gerenciado pelo provedor pode ter. 
| [habilitando Windows sistema de arquivos projetado](enabling-windows-projected-file-system.md)                         | Descreve como habilitar o componente opcional ProjFS.
| [Ciclo de vida da instância de virtualização](virtualization-instance-lifecycle.md)                                   | Visão geral do ciclo de vida de uma instância de virtualização ProjFS.
| [Enumerar arquivos e diretórios](enumerating-files-and-directories.md)                                   | Descreve como um provedor ProjFS participa da enumeração de diretório.
| [Fornecer dados de arquivo](providing-file-data.md)                                                               | Descreve como um provedor fornece informações de espaço reservado e dados de arquivo.
| [Notificações de operação do sistema de arquivos](file-system-operation-notifications.md)                               | Descreve como um provedor pode receber notificações de operações do sistema de arquivos.
| [Manipulando alterações de exibição](handling-view-changes.md)                                                           | Descreve como atualizar a exibição de cliente do armazenamento de backup de um provedor.
| [Manipulação de retorno de chamada assíncrono](asynchronous-callback-handling.md)                                         | Descreve como o provedor pode atender a retornos de chamada de serviço de forma assíncrona.
| [Windows Referência da API do sistema de arquivos projetada](/windows/desktop/api/_projfs) | Informações de referência para a interface de programação ProjFS.

## <a name="additional-resources"></a>Recursos adicionais

| Tópico                                                                                                             | Descrição                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Exemplo de RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | um provedor de ProjFS de exemplo que projeta o Windows registro no sistema de arquivos. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->