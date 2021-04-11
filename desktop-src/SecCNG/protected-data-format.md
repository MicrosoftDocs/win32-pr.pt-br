---
description: Os dados protegidos são armazenados como um BLOB codificado ASN. 1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Formato de dados protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091446"
---
# <a name="protected-data-format"></a><span data-ttu-id="8ee84-103">Formato de dados protegidos</span><span class="sxs-lookup"><span data-stu-id="8ee84-103">Protected Data Format</span></span>

<span data-ttu-id="8ee84-104">Os dados protegidos são armazenados como um BLOB codificado ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="8ee84-104">Protected data is stored as an ASN.1 encoded BLOB.</span></span> <span data-ttu-id="8ee84-105">Os dados são formatados como conteúdo envelopado do CMS (sintaxe de mensagem de certificado).</span><span class="sxs-lookup"><span data-stu-id="8ee84-105">The data is formatted as CMS (certificate message syntax) enveloped content.</span></span> <span data-ttu-id="8ee84-106">O envelope digital contém conteúdo criptografado, informações do destinatário que contêm uma chave de criptografia de conteúdo criptografado (CEK) e um cabeçalho que contém informações sobre o conteúdo, incluindo a cadeia de caracteres da regra de descritor de proteção não criptografada.</span><span class="sxs-lookup"><span data-stu-id="8ee84-106">The digital envelope contains encrypted content, recipient information that contains an encrypted content encryption key (CEK), and a header that contains information about the content, including the unencrypted protection descriptor rule string.</span></span> <span data-ttu-id="8ee84-107">Isso é mostrado pelo diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="8ee84-107">This is shown by the following diagram.</span></span>

![dados de envelope protegidos](images/protecteddatablob.png)

## <a name="related-topics"></a><span data-ttu-id="8ee84-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ee84-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ee84-110">DPAPI CNG</span><span class="sxs-lookup"><span data-stu-id="8ee84-110">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="8ee84-111">Descritores de proteção</span><span class="sxs-lookup"><span data-stu-id="8ee84-111">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> <dt>

[<span data-ttu-id="8ee84-112">Provedores de proteção</span><span class="sxs-lookup"><span data-stu-id="8ee84-112">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



