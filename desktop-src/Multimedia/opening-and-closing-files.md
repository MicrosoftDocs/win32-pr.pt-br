---
title: Abrindo e fechando arquivos
description: Abrindo e fechando arquivos
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- Função AVIFileOpen
- Função AVIFileRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105761889"
---
# <a name="opening-and-closing-files"></a><span data-ttu-id="3cda7-105">Abrindo e fechando arquivos</span><span class="sxs-lookup"><span data-stu-id="3cda7-105">Opening and Closing Files</span></span>

<span data-ttu-id="3cda7-106">Um aplicativo deve abrir um arquivo AVI antes de ler ou gravar.</span><span class="sxs-lookup"><span data-stu-id="3cda7-106">An application must open an AVI file before reading or writing.</span></span> <span data-ttu-id="3cda7-107">Para abrir um arquivo AVI, use a função [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) .</span><span class="sxs-lookup"><span data-stu-id="3cda7-107">To open an AVI file, use the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) function.</span></span> <span data-ttu-id="3cda7-108">**AVIFileOpen** retorna o endereço de uma interface de arquivo AVI que contém o identificador do arquivo aberto e incrementa a contagem de referência do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3cda7-108">**AVIFileOpen** returns the address of an AVI file interface that contains the handle of the open file and increments the reference count of the file.</span></span>

<span data-ttu-id="3cda7-109">A função **AVIFileOpen** dá suporte ao dos sinalizadores usados com a função [OpenFile](/documentation/) .</span><span class="sxs-lookup"><span data-stu-id="3cda7-109">The **AVIFileOpen** function supports the OF flags used with the [OpenFile](/documentation/) function.</span></span> <span data-ttu-id="3cda7-110">Se um aplicativo gravar em um arquivo existente, ele deverá incluir o \_ sinalizador de gravação em **AVIFileOpen**.</span><span class="sxs-lookup"><span data-stu-id="3cda7-110">If an application writes to an existing file, it must include the OF\_WRITE flag in **AVIFileOpen**.</span></span> <span data-ttu-id="3cda7-111">Da mesma forma, se seu aplicativo cria e grava em um novo arquivo, você deve incluir os \_ sinalizadores de criação e de \_ gravação em **AVIFileOpen**.</span><span class="sxs-lookup"><span data-stu-id="3cda7-111">Similarly, if your application creates and writes to a new file, you must include the OF\_CREATE and OF\_WRITE flags in **AVIFileOpen**.</span></span>

<span data-ttu-id="3cda7-112">Quando você abre um arquivo usando **AVIFileOpen**, pode usar um manipulador de arquivo padrão ou pode especificar um manipulador de arquivo personalizado para ler e gravar no arquivo e seus fluxos de dados.</span><span class="sxs-lookup"><span data-stu-id="3cda7-112">When you open a file using **AVIFileOpen**, you can use a default file handler or you can specify a custom file handler to read and write to the file and its data streams.</span></span> <span data-ttu-id="3cda7-113">Em ambos os casos, AVIFile pesquisa no registro o manipulador de arquivo correto a ser usado.</span><span class="sxs-lookup"><span data-stu-id="3cda7-113">In either case, AVIFile searches the registry for the correct file handler to use.</span></span> <span data-ttu-id="3cda7-114">Você deve garantir que os manipuladores de arquivo personalizados estejam no registro antes que um aplicativo possa acessá-los.</span><span class="sxs-lookup"><span data-stu-id="3cda7-114">You must ensure custom file handlers are in the registry before an application can access them.</span></span>

<span data-ttu-id="3cda7-115">Você pode incrementar a contagem de referência de um arquivo usando a função [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) .</span><span class="sxs-lookup"><span data-stu-id="3cda7-115">You can increment the reference count of a file by using the [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) function.</span></span> <span data-ttu-id="3cda7-116">Por exemplo, talvez você queira fazer isso ao passar um identificador da interface de arquivo para outro aplicativo ou quando desejar manter um arquivo aberto ao usar uma função que normalmente fecharia o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3cda7-116">For example, you might want to do this when passing a handle of the file interface to another application, or when you want to keep a file open while using a function that would normally close the file.</span></span>

<span data-ttu-id="3cda7-117">Você pode fechar um arquivo usando a função [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) .</span><span class="sxs-lookup"><span data-stu-id="3cda7-117">You can close a file by using the [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) function.</span></span> <span data-ttu-id="3cda7-118">A função **AVIFileRelease** decrementa a contagem de referência de um arquivo AVI, salva as alterações feitas no arquivo e, quando a contagem de referência chega a zero, fecha o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3cda7-118">The **AVIFileRelease** function decrements the reference count of an AVI file, saves changes made to the file, and when the reference count reaches zero, closes the file.</span></span> <span data-ttu-id="3cda7-119">Seus aplicativos devem balancear a contagem de referência incluindo uma chamada para **AVIFileRelease** para cada uso de [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) e **AVIFileAddRef**.</span><span class="sxs-lookup"><span data-stu-id="3cda7-119">Your applications should balance the reference count by including a call to **AVIFileRelease** for each use of [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileAddRef**.</span></span>

> [!Note]  
> <span data-ttu-id="3cda7-120">Um aplicativo pode abrir um arquivo com um ou mais threads de programa.</span><span class="sxs-lookup"><span data-stu-id="3cda7-120">An application can open a file with one or more program threads.</span></span> <span data-ttu-id="3cda7-121">No entanto, para o melhor desempenho possível, apenas um thread deve acessar o arquivo a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="3cda7-121">However, for the best possible performance, only one thread should access the file at any one time.</span></span>

 

 

 