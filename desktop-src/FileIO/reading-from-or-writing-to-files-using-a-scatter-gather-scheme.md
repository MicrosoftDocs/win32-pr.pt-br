---
description: Descreve um esquema de dispersão-coleta para leitura ou gravação de partes não contíguas de dados em uma única operação.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Lendo ou gravando em arquivos usando um esquema de Scatter-Gather
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7db31dd73dd0b498436548a867dd92ff248805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778770"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a><span data-ttu-id="ba212-103">Lendo ou gravando em arquivos usando um esquema de Scatter-Gather</span><span class="sxs-lookup"><span data-stu-id="ba212-103">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>

<span data-ttu-id="ba212-104">Um esquema de coleta de dispersão usa o sistema operacional para entregar em uma operação várias partes discretas de dados (como registros de banco de dado) de um arquivo para separar buffers não contíguos na memória.</span><span class="sxs-lookup"><span data-stu-id="ba212-104">A scatter-gather scheme uses the operating system to deliver in one operation multiple discrete chunks of data (such as database records) from a file to separate, noncontiguous buffers in memory.</span></span> <span data-ttu-id="ba212-105">Um esquema de dispersão e coleta também grava os dados de buffers não contíguos em uma operação.</span><span class="sxs-lookup"><span data-stu-id="ba212-105">A scatter-gather scheme also writes the data from noncontiguous buffers in one operation.</span></span>

<span data-ttu-id="ba212-106">Um aplicativo pode implementar um esquema de coleta de dispersão usando as funções [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) .</span><span class="sxs-lookup"><span data-stu-id="ba212-106">An application can implement a scatter-gather scheme by using the [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) functions.</span></span>

 

 



