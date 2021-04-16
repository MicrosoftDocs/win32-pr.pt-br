---
description: Comece a criar o pacote de atualização copiando o pacote de instalação e a árvore de diretórios de origem do produto original.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Importando banco de dados de instalação original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750237"
---
# <a name="importing-original-installation-database"></a><span data-ttu-id="1972f-103">Importando banco de dados de instalação original</span><span class="sxs-lookup"><span data-stu-id="1972f-103">Importing Original Installation Database</span></span>

<span data-ttu-id="1972f-104">Comece a criar o pacote de atualização copiando o pacote de instalação e a árvore de diretórios de origem do produto original.</span><span class="sxs-lookup"><span data-stu-id="1972f-104">Begin authoring the upgrade package by copying the installation package and source directory tree of the of original product.</span></span> <span data-ttu-id="1972f-105">As instruções para criar o pacote de instalação para MNP2000 são fornecidas em [um exemplo de instalação](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="1972f-105">Instructions for authoring the installation package for MNP2000 are given in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="1972f-106">Você deve copiar o conteúdo das seguintes pastas:</span><span class="sxs-lookup"><span data-stu-id="1972f-106">You should copy the contents of the following folders:</span></span>

<span data-ttu-id="1972f-107">C: \\MNP2000.msi de exemplo \\</span><span class="sxs-lookup"><span data-stu-id="1972f-107">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="1972f-108">C: \\ bloco de notas de exemplo </span><span class="sxs-lookup"><span data-stu-id="1972f-108">C:\\Sample\\Notepad</span></span>\\\\

<span data-ttu-id="1972f-109">C: \\ exemplo de \\ binário</span><span class="sxs-lookup"><span data-stu-id="1972f-109">C:\\Sample\\Binary</span></span>\\

<span data-ttu-id="1972f-110">C: \\ ícone de exemplo </span><span class="sxs-lookup"><span data-stu-id="1972f-110">C:\\Sample\\Icon</span></span>\\\\

<span data-ttu-id="1972f-111">Atualize o conteúdo da pasta do bloco de notas para que corresponda à fonte descrita em [planejando uma atualização principal](planning-a-major-upgrade.md).</span><span class="sxs-lookup"><span data-stu-id="1972f-111">Update the contents of the Notepad folder so that they match the source described in [Planning a Major Upgrade](planning-a-major-upgrade.md).</span></span> <span data-ttu-id="1972f-112">Remova todos os arquivos de origem obsoletos, como Baseball.txt, e substitua pelos arquivos atualizados, como Baseba01.txt.</span><span class="sxs-lookup"><span data-stu-id="1972f-112">Remove all obsolete source files, such as Baseball.txt, and replace with the updated files, such as Baseba01.txt.</span></span> <span data-ttu-id="1972f-113">Adicione os novos arquivos adicionais fornecidos pela atualização, como Opera01.txt.</span><span class="sxs-lookup"><span data-stu-id="1972f-113">Add the additional new files provided by the upgrade, such as Opera01.txt.</span></span>

<span data-ttu-id="1972f-114">Renomear MNP2000.msi para MNP2001.msi.</span><span class="sxs-lookup"><span data-stu-id="1972f-114">Rename MNP2000.msi to MNP2001.msi.</span></span> <span data-ttu-id="1972f-115">Nas etapas subsequentes, você usará um editor de tabela para modificar esse banco de dados no arquivo. msi para a atualização.</span><span class="sxs-lookup"><span data-stu-id="1972f-115">In subsequent steps you will use a table editor to modify this database into the .msi file for the upgrade.</span></span> <span data-ttu-id="1972f-116">As tabelas de banco de dados que não são explicitamente modificadas nas seções subsequentes são idênticas às tabelas no banco de dados do produto original, MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="1972f-116">Database tables that are not explicitly modified in the subsequent sections are identical to the tables in the original product's database, MNP2000.msi.</span></span>

[<span data-ttu-id="1972f-117">Continuar</span><span class="sxs-lookup"><span data-stu-id="1972f-117">Continue</span></span>](updating-directory-structure-for-an-upgrade.md)

 

 



