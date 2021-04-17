---
title: Instalando procedimentos de e/s personalizados
description: Instalando procedimentos de e/s personalizados
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- e/s de arquivo multimídia, procedimentos personalizados
- e/s de arquivo, procedimentos personalizados
- entrada e saída (e/s), procedimentos personalizados
- E/s (entrada e saída), procedimentos personalizados
- Instalando procedimentos de e/s personalizados
- e/s personalizada
- função mmioInstallIOProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366004"
---
# <a name="installing-custom-io-procedures"></a><span data-ttu-id="7efdf-110">Instalando procedimentos de e/s personalizados</span><span class="sxs-lookup"><span data-stu-id="7efdf-110">Installing Custom I/O Procedures</span></span>

<span data-ttu-id="7efdf-111">Para instalar um procedimento de e/s associado ao. Extensão de nome de arquivo ARC, use a função [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7efdf-111">To install an I/O procedure associated with the .ARC filename extension, use the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function as follows:</span></span>


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



<span data-ttu-id="7efdf-112">Quando você instala um procedimento de e/s usando o [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), o procedimento permanece instalado até você removê-lo.</span><span class="sxs-lookup"><span data-stu-id="7efdf-112">When you install an I/O procedure using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), the procedure remains installed until you remove it.</span></span> <span data-ttu-id="7efdf-113">O procedimento de e/s é usado para qualquer arquivo que você abrir, desde que o arquivo tenha a extensão de nome de arquivo apropriada.</span><span class="sxs-lookup"><span data-stu-id="7efdf-113">The I/O procedure is used for any file you open as long as the file has the appropriate filename extension.</span></span>

<span data-ttu-id="7efdf-114">Você também pode instalar temporariamente um procedimento de e/s usando a função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="7efdf-114">You can also temporarily install an I/O procedure by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="7efdf-115">Nesse caso, o procedimento de e/s é usado apenas com um arquivo aberto usando **mmioOpen** e é removido quando o arquivo é fechado usando a função [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) .</span><span class="sxs-lookup"><span data-stu-id="7efdf-115">In this case, the I/O procedure is used only with a file opened by using **mmioOpen** and is removed when the file is closed by using the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function.</span></span> <span data-ttu-id="7efdf-116">Para especificar um procedimento de e/s ao abrir um arquivo usando **mmioOpen**, use o parâmetro *lpmmioinfo* para fazer referência a uma estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7efdf-116">To specify an I/O procedure when you open a file by using **mmioOpen**, use the *lpmmioinfo* parameter to reference an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure as follows:</span></span>

1.  <span data-ttu-id="7efdf-117">Defina o membro **fccIOProc** como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7efdf-117">Set the **fccIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="7efdf-118">Defina o membro **pIOProc** para o endereço de instância de procedimento do procedimento de e/s.</span><span class="sxs-lookup"><span data-stu-id="7efdf-118">Set the **pIOProc** member to the procedure-instance address of the I/O procedure.</span></span>
3.  <span data-ttu-id="7efdf-119">Defina todos os outros membros como zero (a menos que você esteja abrindo um arquivo de memória ou lendo diretamente ou gravando no buffer de e/s de arquivo).</span><span class="sxs-lookup"><span data-stu-id="7efdf-119">Set all other members to zero (unless you are opening a memory file, or directly reading or writing to the file I/O buffer).</span></span>

<span data-ttu-id="7efdf-120">Certifique-se de remover os procedimentos de e/s que você instalou antes de sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7efdf-120">Be sure to remove any I/O procedures you have installed before you exit your application.</span></span>

 

 