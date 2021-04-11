---
description: Um ponteiro de arquivo é um valor de deslocamento de 64 bits que especifica o próximo byte a ser lido ou o local para receber o próximo byte gravado.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Ponteiros de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165257"
---
# <a name="file-pointers"></a><span data-ttu-id="cf287-103">Ponteiros de arquivo</span><span class="sxs-lookup"><span data-stu-id="cf287-103">File Pointers</span></span>

<span data-ttu-id="cf287-104">Quando um arquivo é aberto, o Windows associa um *ponteiro de arquivo* ao fluxo padrão.</span><span class="sxs-lookup"><span data-stu-id="cf287-104">When a file is opened, Windows associates a *file pointer* with the default stream.</span></span> <span data-ttu-id="cf287-105">Esse ponteiro de arquivo é um valor de deslocamento de 64 bits que especifica o próximo byte a ser lido ou o local para receber o próximo byte gravado.</span><span class="sxs-lookup"><span data-stu-id="cf287-105">This file pointer is a 64-bit offset value that specifies the next byte to be read or the location to receive the next byte written.</span></span> <span data-ttu-id="cf287-106">Cada vez que um arquivo é aberto, o sistema coloca o ponteiro do arquivo no início do arquivo, que é o deslocamento zero.</span><span class="sxs-lookup"><span data-stu-id="cf287-106">Each time a file is opened, the system places the file pointer at the beginning of the file, which is offset zero.</span></span> <span data-ttu-id="cf287-107">Cada operação de leitura e gravação avança o ponteiro do arquivo pelo número de bytes que estão sendo lidos e gravados.</span><span class="sxs-lookup"><span data-stu-id="cf287-107">Each read and write operation advances the file pointer by the number of bytes being read and written.</span></span> <span data-ttu-id="cf287-108">Por exemplo, se o ponteiro do arquivo estiver no início do arquivo e uma operação de leitura de 5 bytes for solicitada, o ponteiro do arquivo estará localizado no deslocamento 5 imediatamente após a operação de leitura.</span><span class="sxs-lookup"><span data-stu-id="cf287-108">For example, if the file pointer is at the beginning of the file and a read operation of 5 bytes is requested, the file pointer will be located at offset 5 immediately after the read operation.</span></span> <span data-ttu-id="cf287-109">À medida que cada byte é lido ou gravado, o sistema avança o ponteiro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf287-109">As each byte is read or written, the system advances the file pointer.</span></span> <span data-ttu-id="cf287-110">O ponteiro do arquivo também pode ser reposicionado chamando a função [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) .</span><span class="sxs-lookup"><span data-stu-id="cf287-110">The file pointer can also be repositioned by calling the [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function.</span></span>

<span data-ttu-id="cf287-111">Quando o ponteiro do arquivo atingir o final de um arquivo e o aplicativo tentar ler o arquivo, nenhum erro ocorrerá, mas nenhum byte será lido.</span><span class="sxs-lookup"><span data-stu-id="cf287-111">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="cf287-112">Portanto, a leitura de zero bytes sem um erro significa que o aplicativo atingiu o final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf287-112">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="cf287-113">Escrever zero bytes não faz nada.</span><span class="sxs-lookup"><span data-stu-id="cf287-113">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="cf287-114">Um aplicativo pode truncar ou estender um arquivo usando a função [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) .</span><span class="sxs-lookup"><span data-stu-id="cf287-114">An application can truncate or extend a file by using the [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) function.</span></span> <span data-ttu-id="cf287-115">Essa função define o fim do arquivo para a posição atual do ponteiro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf287-115">This function sets the end of file to the current position of the file pointer.</span></span>

 

 



