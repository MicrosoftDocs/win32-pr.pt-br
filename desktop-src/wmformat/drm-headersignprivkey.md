---
title: DRM_HeaderSignPrivKey
description: A \_ Propriedade DRM HeaderSignPrivKey contém a chave privada usada para assinar o cabeçalho ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640143"
---
# <a name="drm_headersignprivkey"></a><span data-ttu-id="6fc8e-104">\_HEADERSIGNPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="6fc8e-104">DRM\_HeaderSignPrivKey</span></span>

<span data-ttu-id="6fc8e-105">A propriedade **DRM \_ HeaderSignPrivKey** contém a chave privada usada para assinar o cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="6fc8e-105">The **DRM\_HeaderSignPrivKey** property contains the private key used to sign the ASF header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="6fc8e-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="6fc8e-106">Global Constant</span></span>

<span data-ttu-id="6fc8e-107">g \_ wszWMDRM \_ HeaderSignPrivKey</span><span class="sxs-lookup"><span data-stu-id="6fc8e-107">g\_wszWMDRM\_HeaderSignPrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="6fc8e-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="6fc8e-108">Data Type</span></span>

<span data-ttu-id="6fc8e-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="6fc8e-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="6fc8e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fc8e-110">Remarks</span></span>

<span data-ttu-id="6fc8e-111">Essa propriedade é gerada usando [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span><span class="sxs-lookup"><span data-stu-id="6fc8e-111">This property is generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span></span> <span data-ttu-id="6fc8e-112">Mantenha esse segredo de chave e compartilhe a chave pública somente com o serviço de licença.</span><span class="sxs-lookup"><span data-stu-id="6fc8e-112">Keep this key secret and share the public key only with the license service.</span></span> <span data-ttu-id="6fc8e-113">Depois de definir essa chave, o componente DRM a usará para assinar o cabeçalho do arquivo ASF (não o cabeçalho DRM que é assinado com os valores do objeto de assinatura digital, como DRM \_ LASignaturePrivKey).</span><span class="sxs-lookup"><span data-stu-id="6fc8e-113">After you set this key, the DRM component will use it to sign the ASF file header (not the DRM header which is signed with the digital signature object values such as DRM\_LASignaturePrivKey).</span></span> <span data-ttu-id="6fc8e-114">Obviamente, o **DRM \_ HeaderSignPrivKey** não está incluído no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fc8e-114">Obviously, **DRM\_HeaderSignPrivKey** is not included in the file headert.</span></span>

<span data-ttu-id="6fc8e-115">Essa propriedade não pode ser acessada do objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="6fc8e-115">This property is not accessible from the reader object.</span></span> <span data-ttu-id="6fc8e-116">Ele pode ser definido a partir do objeto Writer usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="6fc8e-116">It can be set from the writer object using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

## <a name="see-also"></a><span data-ttu-id="6fc8e-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fc8e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fc8e-118">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="6fc8e-118">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




