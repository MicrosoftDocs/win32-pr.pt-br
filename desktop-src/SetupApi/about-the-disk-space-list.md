---
description: A lista de espaço em disco permite que você calcule o espaço em disco necessário para concluir as operações de instalação.
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: Sobre a lista de Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b092d73c00f426fe5c0ab298e4b6a53c19131c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751068"
---
# <a name="about-the-disk-space-list"></a>Sobre a lista de Disk-Space

A lista de espaço em disco permite que você calcule o espaço em disco necessário para concluir as operações de instalação. Depois de criar uma lista de espaço em disco e adicionar operações de arquivo a ela, você pode consultar a lista para determinar as unidades de destino especificadas pelas operações de arquivo e o espaço em disco necessário em cada unidade.

Ao comparar o espaço necessário para o espaço disponível nos discos de destino, você pode determinar de forma programática se há espaço suficiente disponível para a instalação atual.

Você pode adicionar ou remover operações de arquivo na lista de espaço em disco e recalcular o espaço em disco necessário. Essa funcionalidade permite, por exemplo, escrever um programa que interaja com o usuário, permitindo que ele escolha quais componentes eles desejam instalar com base no espaço em disco necessário.

As funções de lista de espaço em disco verificam automaticamente se há cópias preexistentes de arquivos no disco de destino. Se uma versão anterior do arquivo for encontrada, as funções de lista de espaço em disco calcularão o espaço adicional necessário para concluir as operações de arquivo.

Por exemplo, se uma operação de cópia especificar que um arquivo de 6000 bytes deve ser copiado para a unidade C, e uma versão de 2000 bytes desse arquivo já existir na unidade C, as funções de espaço em disco retornariam um espaço necessário de 4000 bytes. O espaço adicional é usado para substituir a versão mais antiga do arquivo pela versão mais recente.

A lista de espaço em disco funciona para os tamanhos de arquivo redondos para os limites de cluster de disco.

 

 



