---
description: As funções de integridade da imagem gerenciam o conjunto de certificados em um arquivo de imagem.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Funções de integridade da imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010170"
---
# <a name="image-integrity-functions"></a><span data-ttu-id="15569-103">Funções de integridade da imagem</span><span class="sxs-lookup"><span data-stu-id="15569-103">Image Integrity Functions</span></span>

<span data-ttu-id="15569-104">As funções de integridade da imagem gerenciam o conjunto de certificados em um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="15569-104">The image integrity functions manage the set of certificates in an image file.</span></span> <span data-ttu-id="15569-105">As rotinas são fornecidas para adicionar, remover e consultar certificados.</span><span class="sxs-lookup"><span data-stu-id="15569-105">Routines are provided to add, remove, and query certificates.</span></span> <span data-ttu-id="15569-106">Há também uma função disponível para obter o fluxo de bytes de um arquivo de imagem necessário para calcular um resumo de mensagens do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="15569-106">There is also a function available for obtaining the byte stream of an image file required to calculate a message digest of the image file.</span></span> <span data-ttu-id="15569-107">Isso é necessário para criar certificados de assinatura.</span><span class="sxs-lookup"><span data-stu-id="15569-107">This is needed to create signature certificates.</span></span>

<span data-ttu-id="15569-108">Cada certificado em um arquivo tem um índice que pode ser alterado à medida que os certificados são removidos.</span><span class="sxs-lookup"><span data-stu-id="15569-108">Every certificate in a file has an index which can change as certificates are removed.</span></span> <span data-ttu-id="15569-109">Novos certificados serão sempre adicionados "no final" da lista de certificados existentes.</span><span class="sxs-lookup"><span data-stu-id="15569-109">New certificates will always be added "at the end" of the list of existing certificates.</span></span> <span data-ttu-id="15569-110">Ou seja, eles serão atribuídos a índices maiores que qualquer índice em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="15569-110">That is, they will be assigned indices that are greater than any index currently in use.</span></span> <span data-ttu-id="15569-111">Em geral, um aplicativo não deve supor que um determinado certificado tenha o mesmo índice que tinha na última vez em que foi referenciado.</span><span class="sxs-lookup"><span data-stu-id="15569-111">In general, an application should not assume that a given certificate has the same index it had the last time it was referenced.</span></span>

-   [<span data-ttu-id="15569-112">**DigestFunction**</span><span class="sxs-lookup"><span data-stu-id="15569-112">**DigestFunction**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [<span data-ttu-id="15569-113">**ImageAddCertificate**</span><span class="sxs-lookup"><span data-stu-id="15569-113">**ImageAddCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [<span data-ttu-id="15569-114">**ImageEnumerateCertificates**</span><span class="sxs-lookup"><span data-stu-id="15569-114">**ImageEnumerateCertificates**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [<span data-ttu-id="15569-115">**ImageGetCertificateData**</span><span class="sxs-lookup"><span data-stu-id="15569-115">**ImageGetCertificateData**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [<span data-ttu-id="15569-116">**ImageGetCertificateHeader**</span><span class="sxs-lookup"><span data-stu-id="15569-116">**ImageGetCertificateHeader**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [<span data-ttu-id="15569-117">**ImageGetDigestStream**</span><span class="sxs-lookup"><span data-stu-id="15569-117">**ImageGetDigestStream**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [<span data-ttu-id="15569-118">**ImageRemoveCertificate**</span><span class="sxs-lookup"><span data-stu-id="15569-118">**ImageRemoveCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



