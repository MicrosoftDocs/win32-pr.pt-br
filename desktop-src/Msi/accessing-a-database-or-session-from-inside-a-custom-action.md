---
description: Não é possível acessar uma sessão de instalador de uma ação personalizada que não seja a sessão de instalação atual.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Acessando um banco de dados ou sessão de dentro de uma ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921538"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a><span data-ttu-id="f5fe6-103">Acessando um banco de dados ou sessão de dentro de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="f5fe6-103">Accessing a Database or Session from Inside a Custom Action</span></span>

<span data-ttu-id="f5fe6-104">Não é possível acessar uma sessão de instalador de uma ação personalizada que não seja a sessão de instalação atual.</span><span class="sxs-lookup"><span data-stu-id="f5fe6-104">You cannot access an installer session from a custom action that is not the current installation session.</span></span> <span data-ttu-id="f5fe6-105">As ações personalizadas são limitadas a trabalhar apenas com o banco de dados ativo da sessão e nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="f5fe6-105">Custom actions are limited to working with only the active database of the session and no other databases.</span></span> <span data-ttu-id="f5fe6-106">As funções de [banco de dados](database-functions.md) a seguir Windows Installer não devem ser chamadas de uma ação personalizada, porque exigem um identificador para um banco de dados que não seja o banco de dados da sessão de instalação atual:</span><span class="sxs-lookup"><span data-stu-id="f5fe6-106">The following Windows Installer [Database Functions](database-functions.md) must not be called from a custom action, because they require a handle to a database that is not the database of the current installation session:</span></span>

[<span data-ttu-id="f5fe6-107">**MsiDatabaseMerge**</span><span class="sxs-lookup"><span data-stu-id="f5fe6-107">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[<span data-ttu-id="f5fe6-108">**MsiCreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="f5fe6-108">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[<span data-ttu-id="f5fe6-109">**MsiDatabaseApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="f5fe6-109">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[<span data-ttu-id="f5fe6-110">**MsiDatabaseCommit**</span><span class="sxs-lookup"><span data-stu-id="f5fe6-110">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[<span data-ttu-id="f5fe6-111">**MsiDatabaseExport**</span><span class="sxs-lookup"><span data-stu-id="f5fe6-111">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[<span data-ttu-id="f5fe6-112">**MsiDatabaseGenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="f5fe6-112">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[<span data-ttu-id="f5fe6-113">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="f5fe6-113">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[<span data-ttu-id="f5fe6-114">**MsiEnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="f5fe6-114">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[<span data-ttu-id="f5fe6-115">**MsiGetDatabaseState**</span><span class="sxs-lookup"><span data-stu-id="f5fe6-115">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a><span data-ttu-id="f5fe6-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5fe6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5fe6-117">Acessando a sessão do instalador atual de dentro de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="f5fe6-117">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



