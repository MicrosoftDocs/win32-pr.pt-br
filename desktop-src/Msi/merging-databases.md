---
description: Você pode usar o instalador para adicionar as informações de um banco de dados em outro banco de dados executando uma mesclagem.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Mesclando bancos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922326"
---
# <a name="merging-databases"></a><span data-ttu-id="a2324-103">Mesclando bancos de dados</span><span class="sxs-lookup"><span data-stu-id="a2324-103">Merging Databases</span></span>

<span data-ttu-id="a2324-104">Você pode usar o instalador para adicionar as informações de um banco de dados em outro banco de dados executando uma mesclagem.</span><span class="sxs-lookup"><span data-stu-id="a2324-104">You can use the installer to add the information in one database into another database by performing a merge.</span></span> <span data-ttu-id="a2324-105">[Mesclagens e transformações](merges-and-transforms.md) funcionam em um banco de dados inteiro e uma mesclagem combina dois bancos de dados em um.</span><span class="sxs-lookup"><span data-stu-id="a2324-105">[Merges and Transforms](merges-and-transforms.md) operate on an entire database, and a merge combines two databases into one.</span></span> <span data-ttu-id="a2324-106">As mesclagens são úteis para as equipes de desenvolvimento porque permitem que o banco de dados de instalação de aplicativo grande seja dividido em partes menores e, em seguida, recombinadas no banco de dados de instalação completo mais tarde.</span><span class="sxs-lookup"><span data-stu-id="a2324-106">Merges are useful to development teams because they allow the installation database of large application to be divided into smaller parts and then recombined into the complete installation database later.</span></span>

<span data-ttu-id="a2324-107">**Para mesclar vários bancos de dados de componentes em um único banco de dados completo**</span><span class="sxs-lookup"><span data-stu-id="a2324-107">**To merge several component databases into a single complete database**</span></span>

1.  <span data-ttu-id="a2324-108">Desenvolva os bancos de dados de componentes parciais separadamente.</span><span class="sxs-lookup"><span data-stu-id="a2324-108">Develop the partial component databases separately.</span></span>
2.  <span data-ttu-id="a2324-109">Mescle cada banco de dados de componente no banco de dados do produto principal chamando a função [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) .</span><span class="sxs-lookup"><span data-stu-id="a2324-109">Merge each component database into the main product database by calling the [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function.</span></span>

 

 



