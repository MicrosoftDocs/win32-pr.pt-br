---
description: Explica como usar SignTool para verificar uma assinatura de arquivo.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Usando SignTool para verificar uma assinatura de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e91df7a64a8db48d04ceba9df5fbc3fd358058
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "107954919"
---
# <a name="using-signtool-to-verify-a-file-signature"></a><span data-ttu-id="e9da1-103">Usando SignTool para verificar uma assinatura de arquivo</span><span class="sxs-lookup"><span data-stu-id="e9da1-103">Using SignTool to Verify a File Signature</span></span>

<span data-ttu-id="e9da1-104">O comando a seguir verifica a assinatura de um arquivo chamado *MyControl.exe*:</span><span class="sxs-lookup"><span data-stu-id="e9da1-104">The following command verifies the signature of a file named *MyControl.exe*:</span></span>

<span data-ttu-id="e9da1-105">**Verificação de SignTool** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="e9da1-105">**SignTool verify** *MyControl.exe*</span></span>

<span data-ttu-id="e9da1-106">Se o exemplo anterior falhar, pode ser que a assinatura usou um certificado de assinatura de código.</span><span class="sxs-lookup"><span data-stu-id="e9da1-106">If the preceding example fails, it could be that the signature used a code-signing certificate.</span></span> <span data-ttu-id="e9da1-107">O padrão de [SignTool](signtool.md) é a política de driver do Windows para verificação.</span><span class="sxs-lookup"><span data-stu-id="e9da1-107">[SignTool](signtool.md) defaults to the Windows driver policy for verification.</span></span>

<span data-ttu-id="e9da1-108">O comando a seguir verifica a assinatura, usando a política de verificação de autenticação padrão:</span><span class="sxs-lookup"><span data-stu-id="e9da1-108">The following command verifies the signature, using the Default Authentication Verification Policy:</span></span>

<span data-ttu-id="e9da1-109">**Verificação de SignTool/pa** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="e9da1-109">**SignTool verify /pa** *MyControl.exe*</span></span>

<span data-ttu-id="e9da1-110">O comando a seguir verifica um arquivo do sistema que pode ser assinado em um catálogo:</span><span class="sxs-lookup"><span data-stu-id="e9da1-110">The following command verifies a system file that may be signed in a catalog:</span></span>

<span data-ttu-id="e9da1-111">**SignTool Verify/a** *SysFile.dll*</span><span class="sxs-lookup"><span data-stu-id="e9da1-111">**SignTool verify /a** *SysFile.dll*</span></span>

<span data-ttu-id="e9da1-112">O comando a seguir verifica um arquivo de sistema que está assinado em um catálogo chamado *MyCat.Cat*:</span><span class="sxs-lookup"><span data-stu-id="e9da1-112">The following command verifies a system file that is signed in a catalog named *MyCat.cat*:</span></span>

<span data-ttu-id="e9da1-113">**SignTool Verify/c** *MyCat.Cat* *MyFile.ini*</span><span class="sxs-lookup"><span data-stu-id="e9da1-113">**SignTool verify /c** *MyCat.cat* *MyFile.ini*</span></span>

<span data-ttu-id="e9da1-114">Para qualquer verificação de [SignTool](signtool.md) , você pode recuperar o signatário do certificado.</span><span class="sxs-lookup"><span data-stu-id="e9da1-114">For any [SignTool](signtool.md) verification, you can retrieve the signer of the certificate.</span></span> <span data-ttu-id="e9da1-115">O comando a seguir verifica um arquivo do sistema e exibe o certificado do signatário:</span><span class="sxs-lookup"><span data-stu-id="e9da1-115">The following command verifies a system file and displays the signer certificate:</span></span>

<span data-ttu-id="e9da1-116">**Verificação de SignTool/v** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="e9da1-116">**SignTool verify /v** *MyControl.exe*</span></span>

<span data-ttu-id="e9da1-117">[SignTool](signtool.md) retorna um texto de linha de comando que declara o resultado da verificação de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e9da1-117">[SignTool](signtool.md) returns command-line text that states the result of the signature check.</span></span> <span data-ttu-id="e9da1-118">Além disso, SignTool retorna um código de saída zero para execução bem-sucedida, uma para execução com falha e duas para execução concluída com avisos.</span><span class="sxs-lookup"><span data-stu-id="e9da1-118">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="e9da1-119">Para obter mais informações sobre [SignTool](signtool.md), consulte [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="e9da1-119">For more information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 



