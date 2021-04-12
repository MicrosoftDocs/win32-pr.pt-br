---
title: Interface IWMDRMLicense
description: A interface IWMDRMLicense representa uma lista de uma ou mais licenças.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Formato de mídia do Windows da interface IWMDRMLicense
- Formato de mídia do Windows da interface IWMDRMLicense, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918154b180ed95dce51224e6340a3ab18f432d18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454180"
---
# <a name="iwmdrmlicense-interface"></a><span data-ttu-id="2de31-105">Interface IWMDRMLicense</span><span class="sxs-lookup"><span data-stu-id="2de31-105">IWMDRMLicense interface</span></span>

<span data-ttu-id="2de31-106">A interface **IWMDRMLicense** representa uma lista de uma ou mais licenças.</span><span class="sxs-lookup"><span data-stu-id="2de31-106">The **IWMDRMLicense** interface represents a list of one or more licenses.</span></span>

## <a name="members"></a><span data-ttu-id="2de31-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2de31-107">Members</span></span>

<span data-ttu-id="2de31-108">A interface **IWMDRMLicense** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2de31-108">The **IWMDRMLicense** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2de31-109">**IWMDRMLicense** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2de31-109">**IWMDRMLicense** also has these types of members:</span></span>

-   [<span data-ttu-id="2de31-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2de31-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2de31-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2de31-111">Methods</span></span>

<span data-ttu-id="2de31-112">A interface **IWMDRMLicense** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2de31-112">The **IWMDRMLicense** interface has these methods.</span></span>



| <span data-ttu-id="2de31-113">Método</span><span class="sxs-lookup"><span data-stu-id="2de31-113">Method</span></span>                                                                                   | <span data-ttu-id="2de31-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2de31-114">Description</span></span>                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2de31-115">**Persiste**</span><span class="sxs-lookup"><span data-stu-id="2de31-115">**CanPersist**</span></span>](iwmdrmlicense-canpersist.md)                                           | <span data-ttu-id="2de31-116">Consulta se a licença pode persistir em um repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="2de31-116">Queries whether the license can be persisted on in a local license store.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="2de31-117">**Createdescriptografar**</span><span class="sxs-lookup"><span data-stu-id="2de31-117">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)                                 | <span data-ttu-id="2de31-118">Cria um objeto de descriptografador usando as configurações da licença atual.</span><span class="sxs-lookup"><span data-stu-id="2de31-118">Creates a decryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="2de31-119">**Createcriptografer**</span><span class="sxs-lookup"><span data-stu-id="2de31-119">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)                                 | <span data-ttu-id="2de31-120">Cria um objeto de criptografador usando as configurações da licença atual.</span><span class="sxs-lookup"><span data-stu-id="2de31-120">Creates an encryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="2de31-121">**CreateSecureDecryptor**</span><span class="sxs-lookup"><span data-stu-id="2de31-121">**CreateSecureDecryptor**</span></span>](iwmdrmlicense-createsecuredecryptor.md)                     | <span data-ttu-id="2de31-122">Cria um objeto de descriptografia seguro.</span><span class="sxs-lookup"><span data-stu-id="2de31-122">Creates a secure decryptor object.</span></span> <span data-ttu-id="2de31-123">O descriptografador seguro difere do descriptografador normal, pois ele descriptografa o conteúdo e, em seguida, criptografa-o novamente de acordo com as configurações especificadas nos parâmetros desse método.</span><span class="sxs-lookup"><span data-stu-id="2de31-123">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span><br/> |
| [<span data-ttu-id="2de31-124">**GetAnalogVideoRestrictionLevels**</span><span class="sxs-lookup"><span data-stu-id="2de31-124">**GetAnalogVideoRestrictionLevels**</span></span>](iwmdrmlicense-getanalogvideorestrictionlevels.md) | <span data-ttu-id="2de31-125">Recupera todas as restrições de vídeo analógicas definidas na licença atual.</span><span class="sxs-lookup"><span data-stu-id="2de31-125">Retrieves all analog video restrictions set on the current license.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="2de31-126">**Getinclusõeslist**</span><span class="sxs-lookup"><span data-stu-id="2de31-126">**GetInclusionList**</span></span>](iwmdrmlicense-getinclusionlist.md)                               | <span data-ttu-id="2de31-127">Recupera a lista de inclusão inteira da licença atual ou da cadeia de licença.</span><span class="sxs-lookup"><span data-stu-id="2de31-127">Retrieves the entire inclusion list for the current license or license chain.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="2de31-128">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="2de31-128">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)                                           | <span data-ttu-id="2de31-129">Recupera a licença como dados de linguagem XML (XML) ou XMR (direitos de mídia extensível).</span><span class="sxs-lookup"><span data-stu-id="2de31-129">Retrieves the license as Extensible Markup Language (XML) or Extensible Media Rights (XMR) data.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="2de31-130">**Getlicenciadoproperty**</span><span class="sxs-lookup"><span data-stu-id="2de31-130">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)                           | <span data-ttu-id="2de31-131">Recupera uma propriedade da licença atual.</span><span class="sxs-lookup"><span data-stu-id="2de31-131">Retrieves a property from the current license.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="2de31-132">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="2de31-132">**GetNext**</span></span>](iwmdrmlicense-getnext.md)                                                 | <span data-ttu-id="2de31-133">Carrega as informações sobre a próxima licença na lista.</span><span class="sxs-lookup"><span data-stu-id="2de31-133">Loads the information about the next license in the list.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="2de31-134">**GetOutputProtectionLevels**</span><span class="sxs-lookup"><span data-stu-id="2de31-134">**GetOutputProtectionLevels**</span></span>](iwmdrmlicense-getoutputprotectionlevels.md)             | <span data-ttu-id="2de31-135">Recupera informações sobre todos os níveis de proteção de saída (OPLs) atribuídos à licença.</span><span class="sxs-lookup"><span data-stu-id="2de31-135">Retrieves information about all output protection levels (OPLs) assigned to the license.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="2de31-136">**PersistLicense**</span><span class="sxs-lookup"><span data-stu-id="2de31-136">**PersistLicense**</span></span>](iwmdrmlicense-persistlicense.md)                                   | <span data-ttu-id="2de31-137">Salva a licença atual do repositório temporário no armazenamento de licença local permanente.</span><span class="sxs-lookup"><span data-stu-id="2de31-137">Saves the current license from the temporary store into the permanent local license store.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="2de31-138">**ResetEnumeration**</span><span class="sxs-lookup"><span data-stu-id="2de31-138">**ResetEnumeration**</span></span>](iwmdrmlicense-resetenumeration.md)                               | <span data-ttu-id="2de31-139">Redefine a lista de licenças para seu estado original.</span><span class="sxs-lookup"><span data-stu-id="2de31-139">Resets the license list to its original state.</span></span><br/>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="2de31-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="2de31-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de31-141">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="2de31-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

