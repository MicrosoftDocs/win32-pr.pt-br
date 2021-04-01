---
description: ICE88 valida que o diretório referenciado na coluna DirProperty da tabela IniFile existe no pacote Windows Installer.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829673"
---
# <a name="ice88"></a><span data-ttu-id="e9d33-103">ICE88</span><span class="sxs-lookup"><span data-stu-id="e9d33-103">ICE88</span></span>

<span data-ttu-id="e9d33-104">ICE88 valida que o diretório referenciado na coluna DirProperty da [tabela inifile](inifile-table.md) existe no pacote Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e9d33-104">ICE88 validates that the directory referenced in the DirProperty column of the [IniFile table](inifile-table.md) exists in the Windows Installer package.</span></span> <span data-ttu-id="e9d33-105">ICE88 emitirá um aviso se o valor de DirProperty não representar uma propriedade nas tabelas Directory, AppSearch ou Property, determinadas [Propriedades de pasta do sistema](property-reference.md)ou uma propriedade definida por uma ação personalizada Type 51.</span><span class="sxs-lookup"><span data-stu-id="e9d33-105">ICE88 issues a warning if the DirProperty value does not represent a property in the Directory, AppSearch, or Property tables, certain [system folder properties](property-reference.md), or a property set by a type 51 custom action.</span></span>

<span data-ttu-id="e9d33-106">O ICE88 examina as tabelas e propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="e9d33-106">ICE88 scans the following tables and properties.</span></span>

-   [<span data-ttu-id="e9d33-107">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="e9d33-107">Directory Table</span></span>](directory-table.md)
-   [<span data-ttu-id="e9d33-108">Tabela AppSearch</span><span class="sxs-lookup"><span data-stu-id="e9d33-108">AppSearch Table</span></span>](appsearch-table.md)
-   [<span data-ttu-id="e9d33-109">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="e9d33-109">Property Table</span></span>](property-table.md)
-   <span data-ttu-id="e9d33-110">[Tabela CustomAction](customaction-table.md) , em que a ação personalizada é um [tipo de ação personalizada 51](custom-action-type-51.md)</span><span class="sxs-lookup"><span data-stu-id="e9d33-110">[CustomAction Table](customaction-table.md) , where the custom action is a [Custom Action Type 51](custom-action-type-51.md)</span></span>
-   [<span data-ttu-id="e9d33-111">**Propriedade ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="e9d33-111">**ProgramFilesFolder Property**</span></span>](programfilesfolder.md)
-   [<span data-ttu-id="e9d33-112">**Propriedade CommonFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="e9d33-112">**CommonFilesFolder Property**</span></span>](commonfilesfolder.md)
-   [<span data-ttu-id="e9d33-113">**Propriedade SystemFolder**</span><span class="sxs-lookup"><span data-stu-id="e9d33-113">**SystemFolder Property**</span></span>](systemfolder.md)
-   [<span data-ttu-id="e9d33-114">**Propriedade ProgramFiles64Folder**</span><span class="sxs-lookup"><span data-stu-id="e9d33-114">**ProgramFiles64Folder Property**</span></span>](programfiles64folder.md)
-   [<span data-ttu-id="e9d33-115">**Propriedade CommonFiles64Folder**</span><span class="sxs-lookup"><span data-stu-id="e9d33-115">**CommonFiles64Folder Property**</span></span>](commonfiles64folder.md)
-   [<span data-ttu-id="e9d33-116">**Propriedade System64Folder**</span><span class="sxs-lookup"><span data-stu-id="e9d33-116">**System64Folder Property**</span></span>](system64folder.md)

## <a name="result"></a><span data-ttu-id="e9d33-117">Resultado</span><span class="sxs-lookup"><span data-stu-id="e9d33-117">Result</span></span>

<span data-ttu-id="e9d33-118">ICE88 posta o aviso a seguir.</span><span class="sxs-lookup"><span data-stu-id="e9d33-118">ICE88 posts the following warning.</span></span>



| <span data-ttu-id="e9d33-119">Aviso de ICE88</span><span class="sxs-lookup"><span data-stu-id="e9d33-119">ICE88 Warning</span></span>                                                                                                                                                                  | <span data-ttu-id="e9d33-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9d33-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d33-121">Na entrada da tabela IniFile (IniFile =) \[ 3 \] , DirProperty = \[ 1 \] não é encontrado nas tabelas Directory/Property/AppSearch/CA-Type51 e não é uma das propriedades do instalador.</span><span class="sxs-lookup"><span data-stu-id="e9d33-121">In the IniFile table entry (IniFile=) \[3\] the DirProperty=\[1\] is not found in Directory/Property/AppSearch/CA-Type51 tables and it is not one of the installer properties.</span></span> | <span data-ttu-id="e9d33-122">Para cada registro na tabela IniFile, ICE88 lê o valor na coluna DirProperty.</span><span class="sxs-lookup"><span data-stu-id="e9d33-122">For each record in the IniFile table, ICE88 reads the value in the DirProperty column.</span></span> <span data-ttu-id="e9d33-123">ICE88 verifica o valor na tabela de [diretórios](directory-table.md), na tabela [AppSearch](appsearch-table.md)e na [tabela de propriedades](property-table.md) e também examina a lista de propriedades definidas pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="e9d33-123">ICE88 scans for the value in the [Directory Table](directory-table.md), [AppSearch Table](appsearch-table.md), and [Property Table](property-table.md) and also scans the list of properties set by the installer.</span></span> <span data-ttu-id="e9d33-124">ICE88 lança esse aviso se o valor não puder ser encontrado na verificação.</span><span class="sxs-lookup"><span data-stu-id="e9d33-124">ICE88 posts this warning if the value cannot be found in the scan.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e9d33-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9d33-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9d33-126">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="e9d33-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



