---
description: Este tópico descreve como criar um especialista genérico que é fornecido com o SDK do Monitor de Rede.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Criando um especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169380"
---
# <a name="building-an-expert"></a><span data-ttu-id="72d9b-103">Criando um especialista</span><span class="sxs-lookup"><span data-stu-id="72d9b-103">Building an Expert</span></span>

<span data-ttu-id="72d9b-104">Este tópico descreve como criar um especialista genérico que é fornecido com o SDK do Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="72d9b-104">This topic describes how to build a generic expert that ships with the Network Monitor SDK.</span></span>

> [!Note]  
> <span data-ttu-id="72d9b-105">Antes de criar os exemplos de código a seguir, instale o SDK do Monitor de Rede e inicialize o arquivo de MySetEnv.bat.</span><span class="sxs-lookup"><span data-stu-id="72d9b-105">Before creating the following code examples, install the Network Monitor SDK and initialize the MySetEnv.bat file.</span></span>

 

<span data-ttu-id="72d9b-106">**Para criar um especialista genérico**</span><span class="sxs-lookup"><span data-stu-id="72d9b-106">**To build a generic expert**</span></span>

1.  <span data-ttu-id="72d9b-107">Abra um prompt de comando Monitor de Rede e navegue até o \\ subdiretório experts; por exemplo, C: \\ Program Files \\ NetMonSDK2 \\ experts.</span><span class="sxs-lookup"><span data-stu-id="72d9b-107">Open a Network Monitor command prompt and navigate to the \\Experts subdirectory; for example, C:\\Program Files\\NetMonSDK2\\Experts.</span></span>
2.  <span data-ttu-id="72d9b-108">Digite **Xcopy/e/s/V Blrplate MyExpert**; em seguida, quando solicitado, digite **D**.</span><span class="sxs-lookup"><span data-stu-id="72d9b-108">Type **xcopy /e /s /v Blrplate MyExpert**; then, when prompted, type **D**.</span></span>
3.  <span data-ttu-id="72d9b-109">Mova para o \\ subdiretório MyExpert.</span><span class="sxs-lookup"><span data-stu-id="72d9b-109">Move to the \\MyExpert subdirectory.</span></span>
4.  <span data-ttu-id="72d9b-110">Digite **Ren Blrplate \* . \* MyExpert \* . \***.</span><span class="sxs-lookup"><span data-stu-id="72d9b-110">Type **ren Blrplate\*.\* MyExpert\*.\***.</span></span> <span data-ttu-id="72d9b-111">Verifique se todos os arquivos foram renomeados corretamente.</span><span class="sxs-lookup"><span data-stu-id="72d9b-111">Ensure that all files are properly renamed.</span></span> <span data-ttu-id="72d9b-112">Verifique os nomes de arquivo comparando os arquivos \\ no \\ subdiretório experts Blrplate.</span><span class="sxs-lookup"><span data-stu-id="72d9b-112">Verify the file names by comparing the files in the \\Experts\\Blrplate subdirectory.</span></span>
5.  <span data-ttu-id="72d9b-113">Edite o makefile substituindo todas as ocorrências de **Blrplate** por **MyExpert**.</span><span class="sxs-lookup"><span data-stu-id="72d9b-113">Edit the Makefile by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
6.  <span data-ttu-id="72d9b-114">Edite ambos os arquivos. cpp substituindo todas as ocorrências de **Blrplate** por **MyExpert**.</span><span class="sxs-lookup"><span data-stu-id="72d9b-114">Edit both .cpp files by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span> <span data-ttu-id="72d9b-115">Lembre-se de que o identificador da caixa de diálogo em config. cpp deve estar em letras maiúsculas (por exemplo, **MyExpert**).</span><span class="sxs-lookup"><span data-stu-id="72d9b-115">Be aware that the dialog box identifier in Config.cpp must be capitalized (for example, **MYEXPERT**).</span></span>
7.  <span data-ttu-id="72d9b-116">Edite MyExpert. h substituindo todas as ocorrências de **Blrplate** por **MyExpert**.</span><span class="sxs-lookup"><span data-stu-id="72d9b-116">Edit MyExpert.h by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
8.  <span data-ttu-id="72d9b-117">Edite Resrc1. h renomeando **BLRPLATE** para **MyExpert**.</span><span class="sxs-lookup"><span data-stu-id="72d9b-117">Edit Resrc1.h by renaming **BLRPLATE** to **MYEXPERT**.</span></span> <span data-ttu-id="72d9b-118">(Lembre-se de que **MyExpert** deve estar em letras maiúsculas).</span><span class="sxs-lookup"><span data-stu-id="72d9b-118">(Remember, **MYEXPERT** must be capitalized).</span></span>
9.  <span data-ttu-id="72d9b-119">Edite o arquivo MyExpert. rc ao renomear a **\_ caixa de diálogo IDD BLRPLATE \_ config \_** para a **caixa de \_ \_ \_ diálogo configuração do IDD MyExpert**.</span><span class="sxs-lookup"><span data-stu-id="72d9b-119">Edit the MyExpert.rc file by renaming **IDD\_BLRPLATE\_CONFIG\_DIALOG** to **IDD\_MYEXPERT\_CONFIG\_DIALOG**.</span></span>
10. <span data-ttu-id="72d9b-120">Digite **NMAKE** para criar o arquivo dll.</span><span class="sxs-lookup"><span data-stu-id="72d9b-120">Type **nmake** to build the DLL file.</span></span> <span data-ttu-id="72d9b-121">Para verificar a compilação, altere o diretório para o \\ subdiretório obj e verifique se o arquivo existe.</span><span class="sxs-lookup"><span data-stu-id="72d9b-121">To verify the build, change directory to the \\Obj subdirectory and verify that the file exists.</span></span> <span data-ttu-id="72d9b-122">Para obter mais informações, consulte [exibindo Propriedades de DLL de especialistas](viewing-expert-dll-properties.md).</span><span class="sxs-lookup"><span data-stu-id="72d9b-122">For more information, see [Viewing Expert DLL Properties](viewing-expert-dll-properties.md).</span></span>

<span data-ttu-id="72d9b-123">Quando a compilação for concluída, você terá uma DLL de especialista que pode ser testada e implantada com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="72d9b-123">When the build is complete, you will have an expert DLL that you can test and deploy with Network Monitor.</span></span> <span data-ttu-id="72d9b-124">Para obter mais informações sobre como instalar um especialista, consulte [instalando um especialista para Monitor de Rede 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="72d9b-124">For more information about installing an expert, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span> <span data-ttu-id="72d9b-125">Para obter mais informações sobre como depurar um especialista, consulte [Depurando um especialista](debugging-an-expert.md).</span><span class="sxs-lookup"><span data-stu-id="72d9b-125">For more information about debugging an expert, see [Debugging an Expert](debugging-an-expert.md).</span></span>

 

 



