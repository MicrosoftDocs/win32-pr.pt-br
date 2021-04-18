---
description: A API de filtro de nuvem fornece a funcionalidade no limite entre o modo de usuário e o sistema de arquivos.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Mecanismos de sincronização de nuvem
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: debe32a1849a393a067017f90f5405c4b3ba77d1
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105798207"
---
# <a name="cloud-sync-engines"></a>Mecanismos de sincronização de nuvem

Consulte também [exemplo de espelho de nuvem](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).

A partir do Windows 10, versão 1709, o Windows fornece a *API de arquivos de nuvem*. Essa API consiste em várias APIs nativas do Win32 e do WinRT que formalizam o suporte para mecanismos de sincronização de nuvem e manipula tarefas como a criação e o gerenciamento de diretórios e arquivos de espaço reservado. Os usuários dessa API normalmente são provedores de sincronização e, até certo ponto, aplicativos do Windows.

## <a name="in-this-section"></a>Nesta seção

| Tópico                                                                | Descrição                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Criar um mecanismo de sincronização de nuvem que dê suporte a arquivos de espaço reservado](build-a-cloud-file-sync-engine.md)<br/> | Saiba como usar a API de arquivos de nuvem para criar um mecanismo de sincronização de arquivos de nuvem que inclui arquivos de espaço reservado e integração do explorador de arquivos. <br/> |
| [Referência de filtro de nuvem](cloud-filter-reference.md)<br/> | A API de filtro de nuvem é uma API Win32 nativa que faz parte da API de arquivos de nuvem mais ampla. A API de filtro de nuvem fornece a funcionalidade no limite entre o modo de usuário e o sistema de arquivos. Essa API manipula a criação e o gerenciamento de diretórios e arquivos de espaço reservado. <br/> |

