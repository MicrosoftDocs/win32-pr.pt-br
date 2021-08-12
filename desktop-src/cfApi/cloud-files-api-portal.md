---
description: A API de Filtro de Nuvem fornece funcionalidade no limite entre o modo de usuário e o sistema de arquivos.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Mecanismos de sincronização de nuvem
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: 39dd28779c07dfd6e44fde0e53f583e72971d5883205f42581e3b5ac4102c0eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551370"
---
# <a name="cloud-sync-engines"></a>Mecanismos de sincronização de nuvem

Consulte também [Exemplo de Espelhamento de Nuvem.](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample)

A partir do Windows 10, versão 1709, o Windows fornece a *API de arquivos de nuvem*. Essa API consiste em várias APIs win32 e WinRT nativas que formalizam o suporte para mecanismos de sincronização de nuvem e lidam com tarefas como criar e gerenciar arquivos e diretórios de espaço reservado. Os usuários dessa API normalmente são provedores de sincronização e, até certo ponto, Windows aplicativos.

## <a name="in-this-section"></a>Nesta seção

| Tópico                                                                | Descrição                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Criar um Mecanismo de Sincronização de Nuvem que dá suporte a arquivos de espaço reservado](build-a-cloud-file-sync-engine.md)<br/> | Saiba como usar a API de arquivos de nuvem para criar um mecanismo de sincronização de arquivos de nuvem que inclui arquivos de espaço reservado e Explorador de Arquivos integração. <br/> |
| [Referência de filtro de nuvem](cloud-filter-reference.md)<br/> | A API de filtro de nuvem é uma API nativa do Win32 que faz parte da API de arquivos de nuvem mais ampla. A API de filtro de nuvem fornece funcionalidade no limite entre o modo de usuário e o sistema de arquivos. Essa API lida com a criação e o gerenciamento de arquivos e diretórios de espaço reservado. <br/> |