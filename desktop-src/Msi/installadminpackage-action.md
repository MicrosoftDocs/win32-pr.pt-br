---
description: A ação InstallAdminPackage copia o banco de dados do produto para o ponto de instalação administrativa, que é definido pela propriedade TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Ação InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921477"
---
# <a name="installadminpackage-action"></a><span data-ttu-id="0920f-103">Ação InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="0920f-103">InstallAdminPackage Action</span></span>

<span data-ttu-id="0920f-104">A ação InstallAdminPackage copia o banco de dados do produto para o ponto de instalação administrativa, que é definido pela propriedade [**TARGETDIR**](targetdir.md) .</span><span class="sxs-lookup"><span data-stu-id="0920f-104">The InstallAdminPackage action copies the product database to the administrative installation point, which is defined by the [**TARGETDIR**](targetdir.md) property.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0920f-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="0920f-105">Sequence Restrictions</span></span>

<span data-ttu-id="0920f-106">Não há restrições de sequência.</span><span class="sxs-lookup"><span data-stu-id="0920f-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0920f-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="0920f-107">ActionData Messages</span></span>



| <span data-ttu-id="0920f-108">Campo</span><span class="sxs-lookup"><span data-stu-id="0920f-108">Field</span></span> | <span data-ttu-id="0920f-109">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="0920f-109">Description of action data</span></span>                                 |
|-------|------------------------------------------------------------|
| <span data-ttu-id="0920f-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="0920f-110">\[1\]</span></span> | <span data-ttu-id="0920f-111">Nome dos arquivos de instalação.</span><span class="sxs-lookup"><span data-stu-id="0920f-111">Name of install files.</span></span>                                     |
| <span data-ttu-id="0920f-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="0920f-112">\[6\]</span></span> | <span data-ttu-id="0920f-113">Tamanho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0920f-113">Size of database.</span></span>                                          |
| <span data-ttu-id="0920f-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="0920f-114">\[9\]</span></span> | <span data-ttu-id="0920f-115">Identificador de instalação administrativa – diretório de ponto.</span><span class="sxs-lookup"><span data-stu-id="0920f-115">Identifier of administrative installation–point directory.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0920f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0920f-116">Remarks</span></span>

<span data-ttu-id="0920f-117">A ação InstallAdminPackage também atualiza as informações de resumo do banco de dados e remove os arquivos de gabinete localizados em fluxos depois que o banco de dados é copiado.</span><span class="sxs-lookup"><span data-stu-id="0920f-117">The InstallAdminPackage action also updates the summary information of the database and removes any cabinet files located in streams after the database is copied.</span></span>

 

 



