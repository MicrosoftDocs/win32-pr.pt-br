---
description: A propriedade DVDDirectory define ou recupera o diretório atual do volume de DVD atual.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Propriedade DVDDirectory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36515c931fb8669db814886dfff12a4bf85bde28
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825794"
---
# <a name="dvddirectory-property"></a><span data-ttu-id="8cdf8-103">Propriedade DVDDirectory</span><span class="sxs-lookup"><span data-stu-id="8cdf8-103">DVDDirectory Property</span></span>

> [!Note]  
> <span data-ttu-id="8cdf8-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8cdf8-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8cdf8-106">A `DVDDirectory` propriedade define ou recupera o diretório atual do volume de DVD atual.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-106">The `DVDDirectory` property sets or retrieves the current directory of the current DVD volume.</span></span>

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a><span data-ttu-id="8cdf8-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8cdf8-107">Return Value</span></span>

<span data-ttu-id="8cdf8-108">Retorna um valor de cadeia de caracteres que indica o caminho para o diretório raiz do DVD.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-108">Returns a string value indicating the path to the DVD root directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cdf8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cdf8-109">Remarks</span></span>

<span data-ttu-id="8cdf8-110">Esta propriedade é de leitura/gravação sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-110">This property is read/write with no default value.</span></span> <span data-ttu-id="8cdf8-111">Use esse método para definir o caminho raiz quando houver mais de uma unidade de DVD em um sistema.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-111">Use this method to set the root path when there is more than one DVD drive on a system.</span></span> <span data-ttu-id="8cdf8-112">Quando há apenas uma unidade no sistema e sua letra de unidade é maior que "C", o objeto MSWebDVD a localiza automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-112">When there is only one drive on the system and its drive letter is higher than "C", the MSWebDVD object finds it automatically.</span></span> <span data-ttu-id="8cdf8-113">Para um disco DVD-Video padrão, o caminho raiz deve incluir o \_ diretório de vídeo TS:</span><span class="sxs-lookup"><span data-stu-id="8cdf8-113">For a standard DVD-Video disc, the root path should include the ts\_video directory:</span></span>


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



<span data-ttu-id="8cdf8-114">Alguns volumes de DVD podem ter seus vídeos em um diretório chamado algo diferente de "vídeo \_ TS".</span><span class="sxs-lookup"><span data-stu-id="8cdf8-114">Some DVD volumes may have their video in a directory named something other than "video\_ts."</span></span> <span data-ttu-id="8cdf8-115">A ideia geral é que um "volume de DVD" adicional (o conjunto de. IFO.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-115">The general idea is that an additional "DVD volume" (the set of .IFO.</span></span> <span data-ttu-id="8cdf8-116">VOB e. Arquivos BUP que normalmente seriam armazenados no \_ diretório TS de vídeo) podem ser colocados em um subdiretório no disco. Ao alterar a raiz para apontar para esse diretório, o MSWebDVD funcionará nesse volume de DVD separado.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-116">VOB, and .BUP files that would normally be stored in the VIDEO\_TS directory) can be placed in a subdirectory on the disc. By changing the root to point to this directory, MSWebDVD will operate on this separate DVD volume.</span></span> <span data-ttu-id="8cdf8-117">Um novo conjunto de menus, títulos e assim por diante estará disponível, independentemente dos títulos na raiz TS de vídeo \_ , que não estará mais acessível.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-117">A new set of menus, titles, and so on will be available, independent of the titles in the VIDEO\_TS root, which will no longer be accessible.</span></span> <span data-ttu-id="8cdf8-118">Esses diretórios são chamados de "diretórios ocultos".</span><span class="sxs-lookup"><span data-stu-id="8cdf8-118">Such directories are called "hidden directories."</span></span> <span data-ttu-id="8cdf8-119">O exemplo a seguir mostra como definir um diretório oculto como a raiz, onde "Hidden" é um espaço reservado para qualquer nome que o disco autorizou para o diretório.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-119">The following example shows how to set a hidden directory as the root, where "hidden" is a placeholder for whatever name the disc authors have given to the directory.</span></span>


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



