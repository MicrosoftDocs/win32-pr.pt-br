---
description: As propriedades a seguir são definidas pela interface ICertSrvSetupKeyInformation.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Propriedades de ICertSrvSetupKeyInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828557"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a><span data-ttu-id="d67f4-103">Propriedades de ICertSrvSetupKeyInformation</span><span class="sxs-lookup"><span data-stu-id="d67f4-103">Properties of ICertSrvSetupKeyInformation</span></span>

<span data-ttu-id="d67f4-104">As propriedades a seguir são definidas pela interface [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) .</span><span class="sxs-lookup"><span data-stu-id="d67f4-104">The following properties are defined by the [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) interface.</span></span>



| <span data-ttu-id="d67f4-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d67f4-105">Property</span></span>                                                                           | <span data-ttu-id="d67f4-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d67f4-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d67f4-107">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="d67f4-107">**ContainerName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | <span data-ttu-id="d67f4-108">Obtém ou define o nome usado pelo CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) para gerar, armazenar ou acessar a chave.</span><span class="sxs-lookup"><span data-stu-id="d67f4-108">Gets or sets the name used by the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to generate, store, or access the key.</span></span>                                                                       |
| [<span data-ttu-id="d67f4-109">**Existente**</span><span class="sxs-lookup"><span data-stu-id="d67f4-109">**Existing**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | <span data-ttu-id="d67f4-110">Obtém ou define um valor que indica se a chave privada já existe.</span><span class="sxs-lookup"><span data-stu-id="d67f4-110">Gets or sets a value that indicates whether the private key already exists.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="d67f4-111">**ExistingCACertificate**</span><span class="sxs-lookup"><span data-stu-id="d67f4-111">**ExistingCACertificate**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | <span data-ttu-id="d67f4-112">Obtém ou define o valor binário que foi codificado usando [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) e que é o valor binário do certificado de autoridade de certificação que corresponde a uma chave existente.</span><span class="sxs-lookup"><span data-stu-id="d67f4-112">Gets or sets the binary value that has been encoded by using [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) and that is the binary value of the CA certificate that corresponds to an existing key.</span></span> |
| [<span data-ttu-id="d67f4-113">**HashAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="d67f4-113">**HashAlgorithm**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | <span data-ttu-id="d67f4-114">Obtém ou define o nome do algoritmo de hash usado para assinar ou verificar o certificado de autoridade de certificação para a chave.</span><span class="sxs-lookup"><span data-stu-id="d67f4-114">Gets or sets the name of the hash algorithm used to sign or verify the CA certificate for the key.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="d67f4-115">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="d67f4-115">**Length**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | <span data-ttu-id="d67f4-116">Obtém ou define a intensidade da chave para um dos valores com suporte pelo CSP.</span><span class="sxs-lookup"><span data-stu-id="d67f4-116">Gets or sets the strength of the key to one of the values supported by the CSP.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="d67f4-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="d67f4-117">**ProviderName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | <span data-ttu-id="d67f4-118">Obtém ou define o nome do CSP que é usado para gerar ou armazenar a chave privada.</span><span class="sxs-lookup"><span data-stu-id="d67f4-118">Gets or sets the name of the CSP that is used to generate or store the private key.</span></span>                                                                                                                                                                                                               |



 

 

 
