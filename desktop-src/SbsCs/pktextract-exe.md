---
description: Pktextract.exe é uma ferramenta que extrai o atributo publicKeyToken de um arquivo de certificado.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091447"
---
# <a name="pktextractexe"></a><span data-ttu-id="129c1-103">Pktextract.exe</span><span class="sxs-lookup"><span data-stu-id="129c1-103">Pktextract.exe</span></span>

<span data-ttu-id="129c1-104">Pktextract.exe é uma ferramenta que extrai o atributo **PublicKeyToken** de um arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="129c1-104">Pktextract.exe is a tool that extracts the **publicKeyToken** attribute from a certificate file.</span></span> <span data-ttu-id="129c1-105">A saída é o **PublicKeyToken**, que é um identificador exclusivo de 16 caracteres (8 bytes) da chave pública presente no certificado, em um formato que pode ser facilmente colado em uma instrução de identidade do assembly.</span><span class="sxs-lookup"><span data-stu-id="129c1-105">The output is the **publicKeyToken**, which is a unique 16-character (8-byte) identifier of the public key present in the certificate, in a format that can easily be pasted into an assembly identity statement.</span></span> <span data-ttu-id="129c1-106">O arquivo de certificado deve estar presente no mesmo diretório que Pktextract.exe para usar o utilitário.</span><span class="sxs-lookup"><span data-stu-id="129c1-106">The certificate file must be present in the same directory as Pktextract.exe to use the utility.</span></span> <span data-ttu-id="129c1-107">O Pktextract.exe é fornecido no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="129c1-107">Pktextract.exe is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="129c1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="129c1-108">Syntax</span></span>

<span data-ttu-id="129c1-109">**pktextract.exe** *<filename. cer>* **\[ -Quiet \] \[ -nologo \]**</span><span class="sxs-lookup"><span data-stu-id="129c1-109">**pktextract.exe** *<filename.cer>* **\[-quiet\] \[-nologo\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="129c1-110">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="129c1-110">Command Line Options</span></span>

<span data-ttu-id="129c1-111">Pktextract.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="129c1-111">Pktextract.exe uses the following case-insensitive command line options.</span></span>



| <span data-ttu-id="129c1-112">Opção</span><span class="sxs-lookup"><span data-stu-id="129c1-112">Option</span></span>  | <span data-ttu-id="129c1-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="129c1-113">Description</span></span>                                                          |
|---------|----------------------------------------------------------------------|
| <span data-ttu-id="129c1-114">-quiet</span><span class="sxs-lookup"><span data-stu-id="129c1-114">-quiet</span></span>  | <span data-ttu-id="129c1-115">Suprime a exibição completa de informações de certificado.</span><span class="sxs-lookup"><span data-stu-id="129c1-115">Suppresses full display of certificate information.</span></span> <span data-ttu-id="129c1-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="129c1-116">Optional.</span></span>        |
| <span data-ttu-id="129c1-117">-nologo</span><span class="sxs-lookup"><span data-stu-id="129c1-117">-nologo</span></span> | <span data-ttu-id="129c1-118">É executado sem exibir dados padrão de direitos autorais da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="129c1-118">Runs without displaying standard Microsoft copyright data.</span></span> <span data-ttu-id="129c1-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="129c1-119">Optional.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="129c1-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="129c1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="129c1-121">Ferramentas de desenvolvimento lado a lado do assembly</span><span class="sxs-lookup"><span data-stu-id="129c1-121">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



