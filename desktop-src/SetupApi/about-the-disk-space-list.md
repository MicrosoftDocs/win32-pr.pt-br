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
# <a name="about-the-disk-space-list"></a><span data-ttu-id="56b76-103">Sobre a lista de Disk-Space</span><span class="sxs-lookup"><span data-stu-id="56b76-103">About the Disk-Space List</span></span>

<span data-ttu-id="56b76-104">A lista de espaço em disco permite que você calcule o espaço em disco necessário para concluir as operações de instalação.</span><span class="sxs-lookup"><span data-stu-id="56b76-104">The disk-space list enables you to calculate the disk space required to complete the installation operations.</span></span> <span data-ttu-id="56b76-105">Depois de criar uma lista de espaço em disco e adicionar operações de arquivo a ela, você pode consultar a lista para determinar as unidades de destino especificadas pelas operações de arquivo e o espaço em disco necessário em cada unidade.</span><span class="sxs-lookup"><span data-stu-id="56b76-105">After you create a disk-space list and add file operations to it, you can query the list to determine the target drives specified by the file operations, and the disk space required on each drive.</span></span>

<span data-ttu-id="56b76-106">Ao comparar o espaço necessário para o espaço disponível nos discos de destino, você pode determinar de forma programática se há espaço suficiente disponível para a instalação atual.</span><span class="sxs-lookup"><span data-stu-id="56b76-106">By comparing the space required to the space available on the target disks, you can programmatically determine whether sufficient space is available for the current installation.</span></span>

<span data-ttu-id="56b76-107">Você pode adicionar ou remover operações de arquivo na lista de espaço em disco e recalcular o espaço em disco necessário.</span><span class="sxs-lookup"><span data-stu-id="56b76-107">You can add or remove file operations to the disk-space list and recalculate the disk space required.</span></span> <span data-ttu-id="56b76-108">Essa funcionalidade permite, por exemplo, escrever um programa que interaja com o usuário, permitindo que ele escolha quais componentes eles desejam instalar com base no espaço em disco necessário.</span><span class="sxs-lookup"><span data-stu-id="56b76-108">This functionality enables you to, for example, write a program that interacts with the user, allowing him or her to choose what components they want to install based on the disk space required.</span></span>

<span data-ttu-id="56b76-109">As funções de lista de espaço em disco verificam automaticamente se há cópias preexistentes de arquivos no disco de destino.</span><span class="sxs-lookup"><span data-stu-id="56b76-109">The disk-space list functions automatically check for preexisting copies of files on the target disk.</span></span> <span data-ttu-id="56b76-110">Se uma versão anterior do arquivo for encontrada, as funções de lista de espaço em disco calcularão o espaço adicional necessário para concluir as operações de arquivo.</span><span class="sxs-lookup"><span data-stu-id="56b76-110">If a previous version of the file is found, the disk-space list functions calculate the additional space required to complete the file operations.</span></span>

<span data-ttu-id="56b76-111">Por exemplo, se uma operação de cópia especificar que um arquivo de 6000 bytes deve ser copiado para a unidade C, e uma versão de 2000 bytes desse arquivo já existir na unidade C, as funções de espaço em disco retornariam um espaço necessário de 4000 bytes.</span><span class="sxs-lookup"><span data-stu-id="56b76-111">For example, if a copy operation specifies that a 6000-byte file be copied to drive C, and a 2000-byte version of that file already exists on the drive C, the disk space functions would return a required space of 4000 bytes.</span></span> <span data-ttu-id="56b76-112">O espaço adicional é usado para substituir a versão mais antiga do arquivo pela versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="56b76-112">The additional space is used to replace the older version of the file with the newer version.</span></span>

<span data-ttu-id="56b76-113">A lista de espaço em disco funciona para os tamanhos de arquivo redondos para os limites de cluster de disco.</span><span class="sxs-lookup"><span data-stu-id="56b76-113">The disk-space list functions round file sizes to the disk cluster boundaries.</span></span>

 

 



