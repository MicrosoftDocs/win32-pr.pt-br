---
title: arquivos compostos
description: Embora você possa implementar seus próprios objetos de armazenamento estruturado e interfaces, o COM fornece uma implementação padrão chamada Arquivos Compostos.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 302f7587817f07ec18900f537189a2571c883b0fc43a58eddb823a40fe1c0db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867455"
---
# <a name="compound-files"></a>arquivos compostos

Embora você possa implementar seus próprios objetos de armazenamento estruturado e interfaces, o COM fornece uma implementação padrão chamada Arquivos Compostos. O uso de Arquivos Compostos economiza o trabalho de codificar sua própria implementação de armazenamento estruturado e concede vários benefícios adicionais derivados da aderindo a um padrão definido. Esses benefícios incluem o seguinte:

-   **Independência do sistema de arquivos e da plataforma**. Como a implementação de Arquivos Compostos do COM é executado sobre sistemas de arquivos simples existentes, os arquivos compostos armazenados no sistema de arquivos FAT, no sistema de arquivos NTFS ou nos sistemas de arquivos Macintosh podem ser abertos por aplicativos usando qualquer um dos outros sistemas de arquivos.
-   **Pesquisável.** Como os objetos separados em um arquivo composto são salvos em um formato padrão e podem ser acessados usando interfaces COM padrão e APIs, qualquer utilitário do navegador que usa essas interfaces e APIs pode listar os objetos no arquivo, embora os dados dentro de um determinado objeto possam estar em um formato proprietário.
-   **Acesso a determinados dados internos.** Como a implementação de Arquivos Compostos fornece maneiras padrão de escrever determinados tipos de dados ( informações resumidas, por exemplo), os aplicativos podem ler esses dados usando interfaces COM e APIs.

 

 




