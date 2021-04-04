---
title: Serviços personalizados
description: Serviços personalizados
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- e/s de arquivo multimídia, serviços personalizados
- e/s de arquivo, serviços personalizados
- entrada e saída (e/s), serviços personalizados
- E/s (entrada e saída), serviços personalizados
- e/s personalizada
- função mmioInstallIOProc
- função mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007501"
---
# <a name="custom-services"></a><span data-ttu-id="f8c89-110">Serviços personalizados</span><span class="sxs-lookup"><span data-stu-id="f8c89-110">Custom Services</span></span>

<span data-ttu-id="f8c89-111">Os serviços de e/s de arquivo de multimídia usam os procedimentos de e/s para lidar com a entrada física e a saída associada à leitura e gravação em diferentes tipos de sistemas de armazenamento, como sistemas de arquivamento de arquivos e de armazenamento de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f8c89-111">Multimedia file I/O services use I/O procedures to handle the physical input and output associated with reading and writing to different types of storage systems, such as file-archival systems and database-storage systems.</span></span> <span data-ttu-id="f8c89-112">Os procedimentos de e/s predefinidos existem para os sistemas de arquivos padrão e para os arquivos de memória, mas você pode fornecer um procedimento de e/s personalizado para acessar um sistema de armazenamento exclusivo usando a função [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) .</span><span class="sxs-lookup"><span data-stu-id="f8c89-112">Predefined I/O procedures exist for the standard file systems and for memory files, but you can supply a custom I/O procedure for accessing a unique storage system by using the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function.</span></span>

<span data-ttu-id="f8c89-113">Para abrir um arquivo usando um procedimento de e/s personalizado, use a função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="f8c89-113">To open a file by using a custom I/O procedure, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="f8c89-114">Inclua um sinal de adição (+) ou a constante CFSEPCHAR no nome de arquivo para separar o nome do arquivo físico do nome do elemento do arquivo que você deseja abrir.</span><span class="sxs-lookup"><span data-stu-id="f8c89-114">Include a plus sign (+) or the CFSEPCHAR constant in the filename to separate the name of the physical file from the name of the element of the file you want to open.</span></span> <span data-ttu-id="f8c89-115">O exemplo a seguir abre um elemento file chamado "element" de um arquivo chamado FILENAME. ARCO</span><span class="sxs-lookup"><span data-stu-id="f8c89-115">The following example opens a file element named "element" from a file named FILENAME.ARC:</span></span>


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



<span data-ttu-id="f8c89-116">Quando o Gerenciador de e/s de arquivos encontra um sinal de adição em um nome de arquivo, ele examina a extensão de nome de arquivo para determinar qual procedimento de e/s associar ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="f8c89-116">When the file I/O manager encounters a plus sign in a filename, it examines the filename extension to determine which I/O procedure to associate with the file.</span></span> <span data-ttu-id="f8c89-117">No exemplo anterior, o Gerenciador de e/s de arquivo tentaria usar o procedimento de e/s associado ao. Extensão de nome de arquivo ARC; Esse procedimento de e/s teria sido instalado usando [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span><span class="sxs-lookup"><span data-stu-id="f8c89-117">In the previous example, the file I/O manager would attempt to use the I/O procedure associated with the .ARC filename extension; this I/O procedure would have been installed by using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span></span> <span data-ttu-id="f8c89-118">Se nenhum procedimento de e/s for instalado, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f8c89-118">If no I/O procedure is installed, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) returns an error.</span></span>

<span data-ttu-id="f8c89-119">Os procedimentos de e/s devem responder às seguintes mensagens:</span><span class="sxs-lookup"><span data-stu-id="f8c89-119">I/O procedures must respond to the following messages:</span></span>

-   [<span data-ttu-id="f8c89-120">**MMIOM \_ fechar**</span><span class="sxs-lookup"><span data-stu-id="f8c89-120">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="f8c89-121">**MMIOM \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="f8c89-121">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="f8c89-122">**MMIOM \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="f8c89-122">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="f8c89-123">**MMIOM \_ gravação**</span><span class="sxs-lookup"><span data-stu-id="f8c89-123">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="f8c89-124">**MMIOM \_ Seek**</span><span class="sxs-lookup"><span data-stu-id="f8c89-124">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="f8c89-125">**\_renomear MMIOM**</span><span class="sxs-lookup"><span data-stu-id="f8c89-125">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="f8c89-126">**MMIOM \_ WRITEFLUSH**</span><span class="sxs-lookup"><span data-stu-id="f8c89-126">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)

<span data-ttu-id="f8c89-127">Você também pode criar mensagens personalizadas e enviá-las para o procedimento de e/s usando a função [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) .</span><span class="sxs-lookup"><span data-stu-id="f8c89-127">You can also create custom messages and send them to your I/O procedure by using the [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) function.</span></span> <span data-ttu-id="f8c89-128">Se você definir suas próprias mensagens, verifique se elas estão definidas no valor definido pela constante de usuário do MMIOM ou acima dele \_ .</span><span class="sxs-lookup"><span data-stu-id="f8c89-128">If you define your own messages, make sure they are defined at or above the value defined by the MMIOM\_USER constant.</span></span>

<span data-ttu-id="f8c89-129">Além de processar mensagens, um procedimento de e/s deve manter o membro **lDiskOffset** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) (apontado pelo parâmetro *lpmmioinfo* da função **mmioOpen** ).</span><span class="sxs-lookup"><span data-stu-id="f8c89-129">In addition to processing messages, an I/O procedure must maintain the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure (pointed to by the *lpmmioinfo* parameter of the **mmioOpen** function).</span></span> <span data-ttu-id="f8c89-130">O membro **lDiskOffset** sempre deve conter o deslocamento do arquivo para o local que a próxima MMIOM \_ leitura ou a mensagem de gravação de MMIOM \_ será acessada.</span><span class="sxs-lookup"><span data-stu-id="f8c89-130">The **lDiskOffset** member must always contain the file offset to the location that the next MMIOM\_READ or MMIOM\_WRITE message will access.</span></span> <span data-ttu-id="f8c89-131">O deslocamento é especificado em bytes e é relativo ao início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f8c89-131">The offset is specified in bytes and is relative to the beginning of the file.</span></span> <span data-ttu-id="f8c89-132">O procedimento de e/s pode usar o membro **adwInfo** para manter qualquer informação de estado necessária.</span><span class="sxs-lookup"><span data-stu-id="f8c89-132">The I/O procedure can use the **adwInfo** member to maintain any required state information.</span></span> <span data-ttu-id="f8c89-133">O procedimento de e/s não deve modificar nenhum outro membro na estrutura **MMIOINFO** .</span><span class="sxs-lookup"><span data-stu-id="f8c89-133">The I/O procedure should not modify any other members in the **MMIOINFO** structure.</span></span>

 

 