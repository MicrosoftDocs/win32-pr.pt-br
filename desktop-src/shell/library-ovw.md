---
description: O Windows 7 apresenta bibliotecas, que fornecem aos usuários uma exibição única e coerente de seus arquivos, mesmo quando esses arquivos são armazenados em locais diferentes.
title: Bibliotecas do Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968246"
---
# <a name="windows-libraries"></a>Bibliotecas do Windows

O Windows 7 apresenta bibliotecas, que fornecem aos usuários uma exibição única e coerente de seus arquivos, mesmo quando esses arquivos são armazenados em locais diferentes. As bibliotecas podem ser configuradas e organizadas por um usuário e uma biblioteca pode conter pastas que são encontradas no computador do usuário e também as pastas que foram compartilhadas em uma rede. As bibliotecas apresentam uma visão mais simples do sistema de armazenamento subjacente porque, para o usuário, os arquivos e as pastas em uma biblioteca são exibidos em uma única exibição, independentemente de onde estejam fisicamente armazenados.

Os desenvolvedores que escrevem novos programas no Windows 7 são incentivados a usar bibliotecas como o meio pelo qual os usuários interagem com os arquivos usados pelo programa. O uso de bibliotecas em seu programa fornecerá aos usuários uma experiência mais limpa, mais fácil e consistente no Windows 7.

Os desenvolvedores também devem examinar seus programas existentes e atualizá-los se necessário, para trabalhar com bibliotecas. Como as bibliotecas não fazem parte do sistema de arquivos, as APIs baseadas no sistema de arquivos não terão acesso a bibliotecas que o usuário possa ter configurado.

Os programas que atualmente permitem que os usuários armazenem seu conteúdo em pastas diferentes ou em computadores diferentes irão se beneficiar mais quando adicionam suporte à biblioteca. As bibliotecas simplificam o gerenciamento de conteúdo em diferentes locais de armazenamento para o desenvolvedor e o usuário.

Este guia descreve mais sobre quais bibliotecas do são, como os programas podem ser feitos para trabalhar com bibliotecas e algumas das maneiras como um programa pode usar bibliotecas para melhorar a experiência do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre bibliotecas](library-leverage-to-manage-folders.md)
</dt> <dt>

[Usando bibliotecas em seu programa](library-be-library-aware.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Links do Shell](./links.md)
</dt> <dt>

[Pastas conhecidas](known-folders.md)
</dt> <dt>

[Esquema de descrição da biblioteca](library-schema-entry.md)
</dt> </dl>

 

 
