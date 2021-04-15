---
description: ICE97 verifica se dois componentes não isolam um componente compartilhado para o mesmo diretório.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c41701ce04c0071d6599f888083dfbea4bfc0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747550"
---
# <a name="ice97"></a><span data-ttu-id="47099-103">ICE97</span><span class="sxs-lookup"><span data-stu-id="47099-103">ICE97</span></span>

<span data-ttu-id="47099-104">ICE97 verifica se dois componentes não isolam um componente compartilhado para o mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="47099-104">ICE97 verifies that two components do not isolate a shared component to the same directory.</span></span>

## <a name="result"></a><span data-ttu-id="47099-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="47099-105">Result</span></span>

<span data-ttu-id="47099-106">ICE97 posta os seguintes avisos.</span><span class="sxs-lookup"><span data-stu-id="47099-106">ICE97 posts the following warnings.</span></span>



| <span data-ttu-id="47099-107">Aviso de ICE97</span><span class="sxs-lookup"><span data-stu-id="47099-107">ICE97 Warning</span></span>                                                                                                                                                                    | <span data-ttu-id="47099-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="47099-108">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="47099-109">Este componente \[ 1 \] instala o componente compartilhado no mesmo diretório 2 que o \[ \] outro, que interrompe as regras de componente se ambos (ou mais) componentes são selecionados para instalação.</span><span class="sxs-lookup"><span data-stu-id="47099-109">This component \[1\] installs the Shared component into the same directory \[2\] as another, which breaks component rules if both (or more) components are selected for install.</span></span> | <span data-ttu-id="47099-110">Dois componentes não devem isolar um componente compartilhado para o mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="47099-110">Two components must not isolate a shared component to the same directory.</span></span> |



 

<span data-ttu-id="47099-111">Por exemplo, Component1 e Component2, que compartilham ComponentShared, são instalados no mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="47099-111">For example, Component1 and Component2, which share ComponentShared, are installed to the same directory.</span></span> <span data-ttu-id="47099-112">Ambos especificam ComponentShared como um componente isolado.</span><span class="sxs-lookup"><span data-stu-id="47099-112">Both specify ComponentShared as an isolated component.</span></span> <span data-ttu-id="47099-113">Devido ao isolamento, os arquivos em ComponentShared são copiados duas vezes para a \_ referência de diretório para Component1 e Component2.</span><span class="sxs-lookup"><span data-stu-id="47099-113">Because of the isolation, the files in ComponentShared are copied twice into the Directory\_ reference for Component1 and Component2.</span></span> <span data-ttu-id="47099-114">Os componentes agora têm uma contagem de referência na cópia dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="47099-114">The components now have one reference count on the copy of files.</span></span> <span data-ttu-id="47099-115">Isso é uma violação das regras do componente do instalador.</span><span class="sxs-lookup"><span data-stu-id="47099-115">This is in violation of the Installer component rules.</span></span> <span data-ttu-id="47099-116">Se o Component1 for desinstalado, os arquivos de componentes isolados serão removidos e Component2 será interrompido.</span><span class="sxs-lookup"><span data-stu-id="47099-116">If Component1 is uninstalled, the isolated components files are removed and Component2 is broken.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47099-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47099-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47099-118">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="47099-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



