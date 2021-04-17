---
description: Se o \_ sinalizador de cópia \_ mais recente do SP for especificado durante uma operação de cópia de arquivo, as funções de instalação verificarão se há uma cópia existente do arquivo no diretório de destino.
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: Comparações de versão de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9601dcef07afca81a3ffc64148b0c4f2492f935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749446"
---
# <a name="file-version-comparisons"></a><span data-ttu-id="1d1cb-103">Comparações de versão de arquivo</span><span class="sxs-lookup"><span data-stu-id="1d1cb-103">File Version Comparisons</span></span>

<span data-ttu-id="1d1cb-104">Se o \_ sinalizador de cópia \_ mais recente do SP for especificado durante uma operação de cópia de arquivo, as funções de instalação verificarão se há uma cópia existente do arquivo no diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="1d1cb-104">If the SP\_COPY\_NEWER flag is specified during a file copy operation, the setup functions check for an existing copy of the file in the target directory.</span></span> <span data-ttu-id="1d1cb-105">Se uma cópia existente for encontrada, as funções comparam as versões do destino e do arquivo de origem para determinar qual é mais recente.</span><span class="sxs-lookup"><span data-stu-id="1d1cb-105">If an existing copy is found, the functions compare the versions of the target and source file to determine which is newer.</span></span>

<span data-ttu-id="1d1cb-106">As informações de versão de arquivo usadas durante as verificações de versão são especificadas nos membros **dwFileVersionMS** e **dwFileVersionLS** de uma estrutura do [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) , usadas pelas funções de versão.</span><span class="sxs-lookup"><span data-stu-id="1d1cb-106">The file version information used during version checks is that specified in the **dwFileVersionMS** and **dwFileVersionLS** members of a [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure, used by the version functions.</span></span> <span data-ttu-id="1d1cb-107">Se um dos arquivos não tiver recursos de versão especificados ou se eles tiverem as mesmas informações de versão, o arquivo de origem será tratado como o arquivo mais recente.</span><span class="sxs-lookup"><span data-stu-id="1d1cb-107">If one of the files does not have version resources specified or if they have the same version information, the source file is treated as the newer file.</span></span>

 

 
