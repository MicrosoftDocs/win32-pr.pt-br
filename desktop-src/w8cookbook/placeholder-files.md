---
title: Arquivos de espaço reservado
description: Arquivos de espaço reservado
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "105770312"
---
# <a name="placeholder-files"></a><span data-ttu-id="a6d36-103">Arquivos de espaço reservado</span><span class="sxs-lookup"><span data-stu-id="a6d36-103">Placeholder files</span></span>

## <a name="platform"></a><span data-ttu-id="a6d36-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="a6d36-104">Platform</span></span>

<span data-ttu-id="a6d36-105">**Clientes-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a6d36-105">**Clients -** Windows 8.1</span></span>  
<span data-ttu-id="a6d36-106">**Servidores-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a6d36-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="a6d36-107">Description</span><span class="sxs-lookup"><span data-stu-id="a6d36-107">Description</span></span>

<span data-ttu-id="a6d36-108">Os arquivos de espaço reservado permitem que os usuários exibam e gerenciem arquivos do Microsoft OneDrive independentemente da conectividade.</span><span class="sxs-lookup"><span data-stu-id="a6d36-108">Placeholder files enable users to view and manage Microsoft OneDrive files regardless of connectivity.</span></span> <span data-ttu-id="a6d36-109">Os arquivos de espaço reservado representam o namespace do OneDrive, mesmo quando os arquivos não são armazenados em cache localmente.</span><span class="sxs-lookup"><span data-stu-id="a6d36-109">Placeholder files represent the OneDrive namespace, even when files are not cached locally.</span></span> <span data-ttu-id="a6d36-110">Eles contêm metadados de arquivo e imagens em miniatura de fotos.</span><span class="sxs-lookup"><span data-stu-id="a6d36-110">They contain file metadata and thumbnail images of photos.</span></span>

## <a name="manifestation"></a><span data-ttu-id="a6d36-111">Manifestação</span><span class="sxs-lookup"><span data-stu-id="a6d36-111">Manifestation</span></span>

<span data-ttu-id="a6d36-112">Para usuários finais e desenvolvedores, os arquivos de espaço reservado parecem e se comportam quase iguais aos arquivos locais.</span><span class="sxs-lookup"><span data-stu-id="a6d36-112">To end users and developers, placeholder files look and behave almost the same as the local files.</span></span>

<span data-ttu-id="a6d36-113">Se seu aplicativo usar a caixa de diálogo arquivo comum para enumerar o sistema de arquivos, seu aplicativo não será afetado.</span><span class="sxs-lookup"><span data-stu-id="a6d36-113">If your app uses the Common File Dialog to enumerate the file system, your app will not be impacted.</span></span> <span data-ttu-id="a6d36-114">Quando o usuário tenta abrir o arquivo da caixa de diálogo do/File comum, o conteúdo do arquivo será baixado e será passado para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6d36-114">When the user tries to open the file from the common /file Dialog, the file content will be downloaded and will be passed to your app.</span></span>

<span data-ttu-id="a6d36-115">Se seu aplicativo acessa o sistema de arquivos diretamente, seu aplicativo pode tirar proveito dos arquivos de espaço reservado usando as diretrizes abaixo.</span><span class="sxs-lookup"><span data-stu-id="a6d36-115">If your app accesses the file system directly, then your app may take advantage of the placeholder files by using the guidelines below.</span></span>

## <a name="solution"></a><span data-ttu-id="a6d36-116">Solução</span><span class="sxs-lookup"><span data-stu-id="a6d36-116">Solution</span></span>

-   <span data-ttu-id="a6d36-117">Espaços reservados são ocultos por convenção com base em atributos</span><span class="sxs-lookup"><span data-stu-id="a6d36-117">Placeholders are hidden by convention based on attributes</span></span>
-   <span data-ttu-id="a6d36-118">Identificar espaços reservados usando a ID da marca de nova análise e o \_ \_ \_ \_ espaço reservado para arquivo de marca de nova análise</span><span class="sxs-lookup"><span data-stu-id="a6d36-118">Identify placeholders using reparse tag ID IO\_REPARSE\_TAG\_FILE\_PLACEHOLDER</span></span>

<span data-ttu-id="a6d36-119">Use o modelo de dados do Shell para um comportamento contínuo:</span><span class="sxs-lookup"><span data-stu-id="a6d36-119">Use the shell data model for seamless behavior:</span></span>

-   <span data-ttu-id="a6d36-120">Usar SHCreateItemFromParsingName () para criar um item de Shell</span><span class="sxs-lookup"><span data-stu-id="a6d36-120">Use SHCreateItemFromParsingName() to create a shell item</span></span>
-   <span data-ttu-id="a6d36-121">Associar ao fluxo usando IShellItem:: BindToHandler (fluxo de BHID \_ )</span><span class="sxs-lookup"><span data-stu-id="a6d36-121">Bind to the stream using IShellItem::BindToHandler(BHID\_Stream)</span></span>
-   <span data-ttu-id="a6d36-122">Manipulador de propriedades de usuário para acesso à propriedade (IShellItem2:: GetPropertyHandler)</span><span class="sxs-lookup"><span data-stu-id="a6d36-122">User property handler for property access (IShellItem2::GetPropertyHandler)</span></span>
-   <span data-ttu-id="a6d36-123">Shell do usuário thumbnailhandler para obter imagens em miniatura para espaços reservados</span><span class="sxs-lookup"><span data-stu-id="a6d36-123">User shell thumbnailhandler to get thumbnail images for placeholders</span></span>
-   <span data-ttu-id="a6d36-124">Especifique SupportedProtocols = \* na sua implementação de verbo se o verbo for associado ao fluxo por meio de BindToHandler</span><span class="sxs-lookup"><span data-stu-id="a6d36-124">Specify SupportedProtocols=\* on your verb implementation if the verb binds to the stream via BindToHandler</span></span>


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




