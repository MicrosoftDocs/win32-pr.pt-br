---
title: DRM_LASignaturePrivKey
description: A \_ Propriedade DRM LASignaturePrivKey contém a chave privada que é usada para criptografar o cabeçalho DRM.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdb22f3abc57fc2331ff87bd05bc05d580d607c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365609"
---
# <a name="drm_lasignatureprivkey"></a><span data-ttu-id="3d74b-104">\_LASIGNATUREPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="3d74b-104">DRM\_LASignaturePrivKey</span></span>

<span data-ttu-id="3d74b-105">A propriedade **DRM \_ LASignaturePrivKey** contém a chave privada que é usada para criptografar o cabeçalho DRM.</span><span class="sxs-lookup"><span data-stu-id="3d74b-105">The **DRM\_LASignaturePrivKey** property contains the private key that is used to encrypt the DRM header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="3d74b-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="3d74b-106">Global Constant</span></span>

<span data-ttu-id="3d74b-107">g \_ wszWMDRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="3d74b-107">g\_wszWMDRM\_LASignaturePrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="3d74b-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="3d74b-108">Data Type</span></span>

<span data-ttu-id="3d74b-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="3d74b-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="3d74b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d74b-110">Remarks</span></span>

<span data-ttu-id="3d74b-111">Essa propriedade pode ser gerada usando o método [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) .</span><span class="sxs-lookup"><span data-stu-id="3d74b-111">This property can be generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) method.</span></span> <span data-ttu-id="3d74b-112">Essa propriedade deve permanecer um segredo conhecido apenas pelo criador de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3d74b-112">This property should remain a secret known only by the content creator.</span></span> <span data-ttu-id="3d74b-113">Essa propriedade pode ser definida com o método [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) .</span><span class="sxs-lookup"><span data-stu-id="3d74b-113">This property can be set with the [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) method.</span></span> <span data-ttu-id="3d74b-114">Ele não está acessível ao objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="3d74b-114">It is not accessible to the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d74b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d74b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d74b-116">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="3d74b-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




