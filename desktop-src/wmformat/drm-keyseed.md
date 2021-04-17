---
title: DRM_KeySeed
description: A \_ Propriedade Keysemente de DRM contém a semente de chave que será usada em conjunto com o keyid para criar a chave.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105754226"
---
# <a name="drm_keyseed"></a><span data-ttu-id="ceccc-104">Keysemente DRM \_</span><span class="sxs-lookup"><span data-stu-id="ceccc-104">DRM\_KeySeed</span></span>

<span data-ttu-id="ceccc-105">A **propriedade \_ Keysemente de DRM** contém a semente de chave que será usada em conjunto com o keyid para criar a chave.</span><span class="sxs-lookup"><span data-stu-id="ceccc-105">The **DRM\_KeySeed** property contains the key seed that will be used in conjunction with the KeyID to create the key.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ceccc-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="ceccc-106">Global Constant</span></span>

<span data-ttu-id="ceccc-107">\_wszWMDRM \_ keysemente</span><span class="sxs-lookup"><span data-stu-id="ceccc-107">g\_wszWMDRM\_KeySeed</span></span>

## <a name="data-type"></a><span data-ttu-id="ceccc-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="ceccc-108">Data Type</span></span>

<span data-ttu-id="ceccc-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ceccc-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="ceccc-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ceccc-110">Remarks</span></span>

<span data-ttu-id="ceccc-111">Essa propriedade pode ser definida usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="ceccc-111">This property can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span> <span data-ttu-id="ceccc-112">Ele não pode ser acessado pelo objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="ceccc-112">It is not accessible by the reader object.</span></span>

<span data-ttu-id="ceccc-113">Uma semente-chave normalmente é usada para proteger vários arquivos ou conjuntos de arquivos, por exemplo, todos os arquivos emitidos por um servidor de licença ou talvez todos os arquivos por um determinado artista.</span><span class="sxs-lookup"><span data-stu-id="ceccc-113">A key seed is typically used to protect multiple files or sets of files, for example all the files issued by a license server, or perhaps all the files by a particular artist.</span></span> <span data-ttu-id="ceccc-114">O KeyID, no entanto, é exclusivo para cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="ceccc-114">The KeyID, however, is unique for each file.</span></span>

<span data-ttu-id="ceccc-115">A semente de chave deve permanecer como um segredo que é compartilhado somente entre o criador de conteúdo e o distribuidor de licenças.</span><span class="sxs-lookup"><span data-stu-id="ceccc-115">The key seed must remain a secret that is shared only between the content creator and the license distributor.</span></span> <span data-ttu-id="ceccc-116">Esse valor não é armazenado no cabeçalho DRM e não é necessário nem acessível aos aplicativos do Player DRM.</span><span class="sxs-lookup"><span data-stu-id="ceccc-116">This value is not stored in the DRM header and it is neither needed by nor accessible to DRM player applications.</span></span>

<span data-ttu-id="ceccc-117">Uma nova semente de chave pode ser gerada usando o método [**IWMDRMWriter:: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) ou por qualquer outro meio adequado.</span><span class="sxs-lookup"><span data-stu-id="ceccc-117">A new key seed can be generated using the [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) method or by any other suitable means.</span></span>

## <a name="see-also"></a><span data-ttu-id="ceccc-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ceccc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceccc-119">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="ceccc-119">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




