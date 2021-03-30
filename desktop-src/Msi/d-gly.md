---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e2673f845d85db88d55cbcd53838f7e682dbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647354"
---
# <a name="d-windows-installer"></a><span data-ttu-id="23987-103">D (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="23987-103">D (Windows Installer)</span></span>

<span data-ttu-id="23987-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="23987-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="23987-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**função de banco de dados**</span><span class="sxs-lookup"><span data-stu-id="23987-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**database function**</span></span>
</dt> <dd>

<span data-ttu-id="23987-106">Acessa o banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="23987-106">Accesses the installer database.</span></span> <span data-ttu-id="23987-107">Essas funções são fornecidas principalmente para uso por [*ferramentas de criação de pacote do instalador*](i-gly.md) e não se destinam a serem usadas para chamar os serviços do instalador.</span><span class="sxs-lookup"><span data-stu-id="23987-107">These functions are provided primarily for use by [*installer package authoring tools*](i-gly.md) and they are not intended to be used to call installer services.</span></span> <span data-ttu-id="23987-108">Para obter mais informações, consulte [funções de banco de dados](database-functions.md) e a referência de função do [instalador](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="23987-108">For more information, see [Database Functions](database-functions.md) and the [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="23987-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**identificador de banco de dados**</span><span class="sxs-lookup"><span data-stu-id="23987-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**database handle**</span></span>
</dt> <dd>

<span data-ttu-id="23987-110">Necessário para trabalhar com um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="23987-110">Required for working with a database.</span></span> <span data-ttu-id="23987-111">Para obter mais informações, consulte [obtendo um identificador de banco de dados](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="23987-111">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="23987-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**patch Delta**</span><span class="sxs-lookup"><span data-stu-id="23987-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**delta patch**</span></span>
</dt> <dd>

<span data-ttu-id="23987-113">Um patch Delta é um patch de Windows Installer compactado por Delta criado usando uma ferramenta, como Patchwiz.dll, que dá suporte à compactação Delta.</span><span class="sxs-lookup"><span data-stu-id="23987-113">A delta patch is a delta-compressed Windows Installer patch created using a tool, such as Patchwiz.dll, that supports delta compression.</span></span> <span data-ttu-id="23987-114">Os patches que usam a compactação Delta podem reduzir o tamanho de uma atualização fornecendo apenas as diferenças (deltas) entre os arquivos existentes em um computador de destino e os arquivos novos desejados.</span><span class="sxs-lookup"><span data-stu-id="23987-114">Patches that use delta compression can reduce the size of an update by providing only the differences (deltas) between existing files on a target computer and the desired new files.</span></span> <span data-ttu-id="23987-115">Os arquivos novos desejados são então sintetizados a partir dos arquivos existentes e dos deltas baixados.</span><span class="sxs-lookup"><span data-stu-id="23987-115">The desired new files are then synthesized from the existing files and the downloaded deltas.</span></span> <span data-ttu-id="23987-116">Para obter mais informações sobre a tecnologia de compactação Delta, consulte a [interface de programação de aplicativo de compactação Delta](https://msdn.microsoft.com/library/ms811406.aspx).</span><span class="sxs-lookup"><span data-stu-id="23987-116">For more information about delta compression technology, see the [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).</span></span>

</dd> </dl>

 

 



