---
title: Guia de programação do sistema de arquivos projetado
description: Informações conceituais sobre como implementar um aplicativo de provedor ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: a6b2d186ac3e674c3fa68e17ecd523b2c94f2401
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007865"
---
# <a name="projected-file-system-projfs-programming-guide"></a>Guia de programação do sistema de arquivos projetado (ProjFS)

O sistema de arquivos projetado do Windows (ProjFS) permite que um aplicativo de modo de usuário chamado "provedor" faça o projeto de dados hierárquicos no sistema de arquivos, fazendo com que ele apareça como arquivos e diretórios no sistema de arquivos.

## <a name="in-this-section"></a>Nesta seção

| Tópico                                                                                                       | Descrição |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Visão geral do provedor](provider-overview.md)                                                                   | Visão geral conceitual de um aplicativo de provedor.
| [Estado do cache na raiz de virtualização](cache-state.md)                                                    | Descreve os diferentes Estados de cache que um arquivo ou diretório gerenciado pelo provedor pode ter. 
| [Habilitando o sistema de arquivos projetado pelo Windows](enabling-windows-projected-file-system.md)                         | Descreve como habilitar o componente opcional ProjFS.
| [Ciclo de vida da instância de virtualização](virtualization-instance-lifecycle.md)                                   | Visão geral do ciclo de vida de uma instância de virtualização ProjFS.
| [Enumerar arquivos e diretórios](enumerating-files-and-directories.md)                                   | Descreve como um provedor ProjFS participa da enumeração de diretório.
| [Fornecer dados de arquivo](providing-file-data.md)                                                               | Descreve como um provedor fornece informações de espaço reservado e dados de arquivo.
| [Notificações de operação do sistema de arquivos](file-system-operation-notifications.md)                               | Descreve como um provedor pode receber notificações de operações do sistema de arquivos.
| [Manipulando alterações de exibição](handling-view-changes.md)                                                           | Descreve como atualizar a exibição de cliente do armazenamento de backup de um provedor.
| [Manipulação de retorno de chamada assíncrono](asynchronous-callback-handling.md)                                         | Descreve como o provedor pode atender a retornos de chamada de serviço de forma assíncrona.
| [Referência da API do sistema de arquivos projetadas do Windows](/windows/desktop/api/_projfs) | Informações de referência para a interface de programação ProjFS.

## <a name="additional-resources"></a>Recursos adicionais

|                                                                                                              |                                                                                   |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Exemplo de RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Um provedor de ProjFS de exemplo que projeta o registro do Windows no sistema de arquivos. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->