---
description: A API de Filtro de Nuvem fornece funcionalidade no limite entre o modo de usuário e o sistema de arquivos.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Mecanismos de sincronização de nuvem
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: d40b195a442859441138ae4e61cb0eb946411623
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549591"
---
# <a name="cloud-sync-engines"></a>Mecanismos de sincronização de nuvem

Consulte também [Exemplo de Espelhamento de Nuvem.](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample)

A partir do Windows 10, versão 1709, o Windows fornece a *API de arquivos de nuvem*. Essa API consiste em várias APIs win32 e WinRT nativas que formalizam o suporte para mecanismos de sincronização de nuvem e lidam com tarefas como criar e gerenciar arquivos e diretórios de espaço reservado. Os usuários dessa API normalmente são provedores de sincronização e, até certo ponto, aplicativos do Windows.

## <a name="in-this-section"></a>Nesta seção

| Tópico                                                                | Descrição                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Criar um Mecanismo de Sincronização de Nuvem que dá suporte a arquivos de espaço reservado](build-a-cloud-file-sync-engine.md)<br/> | Saiba como usar a API de arquivos de nuvem para criar um mecanismo de sincronização de arquivos de nuvem que inclui arquivos de espaço reservado e Explorador de Arquivos integração. <br/> |
| [Referência de filtro de nuvem](cloud-filter-reference.md)<br/> | A API de filtro de nuvem é uma API nativa do Win32 que faz parte da API de arquivos de nuvem mais ampla. A API de filtro de nuvem fornece funcionalidade no limite entre o modo de usuário e o sistema de arquivos. Essa API lida com a criação e o gerenciamento de arquivos e diretórios de espaço reservado. <br/> |