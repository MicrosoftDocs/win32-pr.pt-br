---
description: Um aplicativo lê e grava em um arquivo usando as funções ReadFile, ReadFileEx, WriteFile e WriteFileEx.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Lendo e gravando em arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757557"
---
# <a name="reading-from-and-writing-to-files"></a><span data-ttu-id="06c1c-103">Lendo e gravando em arquivos</span><span class="sxs-lookup"><span data-stu-id="06c1c-103">Reading From and Writing to Files</span></span>

<span data-ttu-id="06c1c-104">Um aplicativo lê e grava em um arquivo usando as funções [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) .</span><span class="sxs-lookup"><span data-stu-id="06c1c-104">An application reads from and writes to a file by using the [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) functions.</span></span> <span data-ttu-id="06c1c-105">Essas funções exigem um identificador para um arquivo a ser aberto para leitura e gravação, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="06c1c-105">These functions require a handle to a file to be opened for reading and writing, respectively.</span></span> <span data-ttu-id="06c1c-106">Eles lêem e gravam um número especificado de bytes no local indicado pelo ponteiro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="06c1c-106">They read and write a specified number of bytes at the location indicated by the file pointer.</span></span> <span data-ttu-id="06c1c-107">Os dados são lidos e gravados exatamente como especificado; as funções não formatam Os dados.</span><span class="sxs-lookup"><span data-stu-id="06c1c-107">The data is read and written exactly as specified; the functions do not format the data.</span></span>

<span data-ttu-id="06c1c-108">Quando o ponteiro do arquivo atingir o final de um arquivo e o aplicativo tentar ler o arquivo, nenhum erro ocorrerá, mas nenhum byte será lido.</span><span class="sxs-lookup"><span data-stu-id="06c1c-108">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="06c1c-109">Portanto, a leitura de zero bytes sem um erro significa que o aplicativo atingiu o final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="06c1c-109">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="06c1c-110">Escrever zero bytes não faz nada.</span><span class="sxs-lookup"><span data-stu-id="06c1c-110">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="06c1c-111">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="06c1c-111">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="06c1c-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="06c1c-112">In this section</span></span>



| <span data-ttu-id="06c1c-113">Tópico</span><span class="sxs-lookup"><span data-stu-id="06c1c-113">Topic</span></span>                                                                                                                                           | <span data-ttu-id="06c1c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="06c1c-114">Description</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06c1c-115">Posicionando um ponteiro de arquivo</span><span class="sxs-lookup"><span data-stu-id="06c1c-115">Positioning a File Pointer</span></span>](positioning-a-file-pointer.md)<br/>                                                                         | <span data-ttu-id="06c1c-116">O Windows usa um ponteiro de arquivo para controlar os bytes lidos ou gravados.</span><span class="sxs-lookup"><span data-stu-id="06c1c-116">Windows uses a file pointer to keep track of bytes read or written.</span></span><br/>                                                       |
| [<span data-ttu-id="06c1c-117">Lendo ou gravando em arquivos usando um esquema de Scatter-Gather</span><span class="sxs-lookup"><span data-stu-id="06c1c-117">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | <span data-ttu-id="06c1c-118">Descreve um esquema de dispersão-coleta para leitura ou gravação de partes não contíguas de dados em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="06c1c-118">Describes a scatter-gather scheme for reading or writing noncontiguous chunks of data in one operation.</span></span><br/>                   |
| [<span data-ttu-id="06c1c-119">Liberando dados de e/s de System-Buffered para O disco</span><span class="sxs-lookup"><span data-stu-id="06c1c-119">Flushing System-Buffered I/O Data to Disk</span></span>](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | <span data-ttu-id="06c1c-120">O Windows armazena os dados em operações de leitura e gravação de arquivo em buffers de dados mantidos pelo sistema para otimizar o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="06c1c-120">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span><br/> |
| [<span data-ttu-id="06c1c-121">Truncando ou estendendo arquivos</span><span class="sxs-lookup"><span data-stu-id="06c1c-121">Truncating or Extending Files</span></span>](truncating-or-extending-files.md)<br/>                                                                   | <span data-ttu-id="06c1c-122">Um aplicativo pode truncar ou estender um arquivo chamando [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span><span class="sxs-lookup"><span data-stu-id="06c1c-122">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span><br/>                             |



 

 

 




