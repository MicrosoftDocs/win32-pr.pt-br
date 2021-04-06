---
description: Cada propriedade de controle de registro de certificado é de leitura/gravação e tem um padrão inicializado, bem como um conjunto de valores aceitáveis.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Usando as propriedades do controle de registro de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647633"
---
# <a name="using-the-certificate-enrollment-control-properties"></a><span data-ttu-id="e3f89-103">Usando as propriedades do controle de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="e3f89-103">Using the Certificate Enrollment Control Properties</span></span>

<span data-ttu-id="e3f89-104">Cada propriedade de controle de registro de certificado é de leitura/gravação e tem um padrão inicializado, bem como um conjunto de valores aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="e3f89-104">Each Certificate Enrollment Control property is read/write and has an initialized default as well as a set of acceptable values.</span></span> <span data-ttu-id="e3f89-105">Você pode definir uma propriedade para qualquer valor nesse conjunto a fim de modificar o comportamento dos métodos que usam a propriedade.</span><span class="sxs-lookup"><span data-stu-id="e3f89-105">You can set a property to any value within this set in order to modify the behavior of methods that use the property.</span></span> <span data-ttu-id="e3f89-106">Para obter um comportamento desejado, defina a propriedade antes de chamar o método que usa o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e3f89-106">To get a desired behavior, set the property before you call the method that uses that property's value.</span></span>

<span data-ttu-id="e3f89-107">Observe, no entanto, que depois de chamar os métodos a seguir</span><span class="sxs-lookup"><span data-stu-id="e3f89-107">Note, however, that after calling the following methods</span></span>

-   [<span data-ttu-id="e3f89-108">**acceptPKCS7**</span><span class="sxs-lookup"><span data-stu-id="e3f89-108">**acceptPKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [<span data-ttu-id="e3f89-109">**acceptFilePKCS7**</span><span class="sxs-lookup"><span data-stu-id="e3f89-109">**acceptFilePKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [<span data-ttu-id="e3f89-110">**createPKCS10**</span><span class="sxs-lookup"><span data-stu-id="e3f89-110">**createPKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [<span data-ttu-id="e3f89-111">**createFilePKCS10**</span><span class="sxs-lookup"><span data-stu-id="e3f89-111">**createFilePKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

<span data-ttu-id="e3f89-112">as propriedades a seguir estão impedidas de serem redefinidas</span><span class="sxs-lookup"><span data-stu-id="e3f89-112">the following properties are blocked from being reset</span></span>

-   [<span data-ttu-id="e3f89-113">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="e3f89-113">**ProviderType**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [<span data-ttu-id="e3f89-114">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="e3f89-114">**KeySpec**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [<span data-ttu-id="e3f89-115">**ProviderFlags**</span><span class="sxs-lookup"><span data-stu-id="e3f89-115">**ProviderFlags**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [<span data-ttu-id="e3f89-116">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="e3f89-116">**ContainerName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [<span data-ttu-id="e3f89-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="e3f89-117">**ProviderName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

<span data-ttu-id="e3f89-118">a menos que o método [**ICEnroll4:: Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="e3f89-118">unless the [**ICEnroll4::Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) method is called.</span></span>

<span data-ttu-id="e3f89-119">Para obter informações sobre propriedades e métodos individuais, consulte os tópicos de referência para essas propriedades e métodos na [referência de criptografia](cryptography-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e3f89-119">For information about individual properties and methods, see the reference topics for those properties and methods in the [Cryptography Reference](cryptography-reference.md).</span></span>

<span data-ttu-id="e3f89-120">As seções a seguir contêm informações específicas do idioma para definir e recuperar as propriedades do controle de registro de certificado:</span><span class="sxs-lookup"><span data-stu-id="e3f89-120">The following sections contain language-specific information for setting and retrieving the Certificate Enrollment Control properties:</span></span>

-   [<span data-ttu-id="e3f89-121">Propriedades de controle de registro de certificado em C++</span><span class="sxs-lookup"><span data-stu-id="e3f89-121">Certificate Enrollment Control Properties in C++</span></span>](certificate-enrollment-control-properties-in-c-.md)

 

 
