---
title: DRM_KeyID
description: O \_ atributo keyid do DRM contém o identificador de chave.
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007144"
---
# <a name="drm_keyid"></a><span data-ttu-id="8c7af-104">\_Keyid DRM</span><span class="sxs-lookup"><span data-stu-id="8c7af-104">DRM\_KeyID</span></span>

<span data-ttu-id="8c7af-105">O **atributo \_ keyid do DRM** contém o identificador de chave.</span><span class="sxs-lookup"><span data-stu-id="8c7af-105">The **DRM\_KeyID** attribute contains the key identifier.</span></span>

## <a name="global-constant"></a><span data-ttu-id="8c7af-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="8c7af-106">Global Constant</span></span>

<span data-ttu-id="8c7af-107">\_keyid g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="8c7af-107">g\_wszWMDRM\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="8c7af-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="8c7af-108">Data Type</span></span>

<span data-ttu-id="8c7af-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="8c7af-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="8c7af-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c7af-110">Remarks</span></span>

<span data-ttu-id="8c7af-111">Este atributo está presente somente para conteúdo DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="8c7af-111">This attribute is present for DRM Version 7 content only.</span></span> <span data-ttu-id="8c7af-112">Ele pode ser definido usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="8c7af-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="8c7af-113">O mesmo atributo de arquivo pode ser recuperado usando o [**\_ \_ keyid DRMHeader do DRM**](drm-drmheader-keyid.md).</span><span class="sxs-lookup"><span data-stu-id="8c7af-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

<span data-ttu-id="8c7af-114">A ID da chave é usada em conjunto com a semente de chave para criar a chave de conteúdo que é usada para criptografar e descriptografar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="8c7af-114">The key ID is used in conjunction with the key seed to create the content key which is used to encrypt and decrypt the file.</span></span> <span data-ttu-id="8c7af-115">O aplicativo de gravador usa a ID de chave para criptografar o arquivo e, em seguida, armazena a ID da chave no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="8c7af-115">The writer application uses the key ID to encrypt the file and then it stores the key ID in the file header.</span></span> <span data-ttu-id="8c7af-116">Quando um aplicativo de Player solicita uma licença para um arquivo, o componente DRM envia a ID de chave (juntamente com o restante do cabeçalho DRM) para o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="8c7af-116">When a player application requests a license for a file, the DRM component sends the key ID (along with the rest of the DRM header) to the license server.</span></span> <span data-ttu-id="8c7af-117">O servidor de licença, que tem a semente da chave secreta, usa-a e a ID da chave para criar uma chave para o arquivo, que ele insere em uma licença junto com os vários direitos que serão aplicados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="8c7af-117">The license server, which has the secret key seed, uses it and the key ID to create a key for the file, which it then inserts into a license along with the various rights that will be applied to the file.</span></span>

<span data-ttu-id="8c7af-118">Normalmente, uma semente de chave é usada com muitas IDs de chave.</span><span class="sxs-lookup"><span data-stu-id="8c7af-118">Typically, one key seed is used with many key IDs.</span></span> <span data-ttu-id="8c7af-119">A semente de chave é um segredo compartilhado somente pelo criador de conteúdo e pelo distribuidor de licenças.</span><span class="sxs-lookup"><span data-stu-id="8c7af-119">The key seed is a secret shared only by the content creator and the license distributor.</span></span> <span data-ttu-id="8c7af-120">A ID da chave é usada por aplicativos cliente DRM e é armazenada no cabeçalho DRM em claro.</span><span class="sxs-lookup"><span data-stu-id="8c7af-120">The key ID is used by DRM client applications and is stored in the DRM header in the clear.</span></span>

<span data-ttu-id="8c7af-121">Esse atributo é o mesmo que [**o \_ \_ keyid DRMHeader do DRM**](drm-drmheader-keyid.md).</span><span class="sxs-lookup"><span data-stu-id="8c7af-121">This attribute is the same as [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8c7af-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c7af-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c7af-123">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="8c7af-123">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




