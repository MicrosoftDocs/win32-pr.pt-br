---
description: Especifica se o IMFTransform deseja receber notificações de conclusão de MEPolicySet.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814608"
---
# <a name="mft_policy_set_aware-attribute"></a><span data-ttu-id="2ea9a-103">\_Atributo de \_ reconhecimento de conjunto de políticas de MFT \_</span><span class="sxs-lookup"><span data-stu-id="2ea9a-103">MFT\_POLICY\_SET\_AWARE attribute</span></span>

<span data-ttu-id="2ea9a-104">Se for diferente de zero, indica que o **IMFTransform** deseja receber notificações de conclusão de [MEPolicySet](./mepolicyset.md) .</span><span class="sxs-lookup"><span data-stu-id="2ea9a-104">If non-zero, indicates that the **IMFTransform** wants to receive [MEPolicySet](./mepolicyset.md) completion notifications.</span></span>

## <a name="data-type"></a><span data-ttu-id="2ea9a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2ea9a-105">Data type</span></span>

<span data-ttu-id="2ea9a-106">**UINT32** (Tratado como **bool**)</span><span class="sxs-lookup"><span data-stu-id="2ea9a-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="2ea9a-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="2ea9a-107">Get/set</span></span>

<span data-ttu-id="2ea9a-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="2ea9a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="2ea9a-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="2ea9a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="2ea9a-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="2ea9a-110">Applies to</span></span>

[<span data-ttu-id="2ea9a-111">**IMFInputTrustAuthority**</span><span class="sxs-lookup"><span data-stu-id="2ea9a-111">**IMFInputTrustAuthority**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a><span data-ttu-id="2ea9a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ea9a-112">Remarks</span></span>

<span data-ttu-id="2ea9a-113">Este atributot pode ser usado por um **IMFInputTrustAuthority** Decrypter.</span><span class="sxs-lookup"><span data-stu-id="2ea9a-113">This attributet can be used by an **IMFInputTrustAuthority** decrypter.</span></span> <span data-ttu-id="2ea9a-114">Uma implementação de um módulo de descriptografia de conteúdo (CDM) pode incluir uma implementação de **IMFInputTrustAuthority**.</span><span class="sxs-lookup"><span data-stu-id="2ea9a-114">An implementation of a Content Decryption Module (CDM) may include an implementation of **IMFInputTrustAuthority**.</span></span> <span data-ttu-id="2ea9a-115">O objeto **IMFInputTrustAuthority** é acessado por meio de [IMFContentDecryptionModule:: CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span><span class="sxs-lookup"><span data-stu-id="2ea9a-115">The **IMFInputTrustAuthority** object is accessed through [IMFContentDecryptionModule::CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span></span>


<span data-ttu-id="2ea9a-116">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2ea9a-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ea9a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ea9a-117">Requirements</span></span>



| <span data-ttu-id="2ea9a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ea9a-118">Requirement</span></span> | <span data-ttu-id="2ea9a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2ea9a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ea9a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ea9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2ea9a-121">Atualização de abril de 2020 do Windows 10</span><span class="sxs-lookup"><span data-stu-id="2ea9a-121">Windows 10 April 2020 Update</span></span>   <br/>                                        |
| <span data-ttu-id="2ea9a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ea9a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ea9a-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ea9a-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ea9a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ea9a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ea9a-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2ea9a-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="2ea9a-126">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="2ea9a-126">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
