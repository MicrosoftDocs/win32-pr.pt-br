---
description: Um identificador que pode ser definido em um IMFOutputPolicy.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: MF_POLICY_ID (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787195b20980164d7534bccc267781cdbb7510e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011738"
---
# <a name="mf_policy_id-attribute"></a><span data-ttu-id="b9750-103">Atributo de ID da \_ política MF \_</span><span class="sxs-lookup"><span data-stu-id="b9750-103">MF\_POLICY\_ID attribute</span></span>

<span data-ttu-id="b9750-104">Um identificador que pode ser definido em um [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy).</span><span class="sxs-lookup"><span data-stu-id="b9750-104">An identifier that can be set on an [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy).</span></span>

## <a name="data-type"></a><span data-ttu-id="b9750-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b9750-105">Data type</span></span>

<span data-ttu-id="b9750-106">**UINT32** (Tratado como **bool**)</span><span class="sxs-lookup"><span data-stu-id="b9750-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="remarks"></a><span data-ttu-id="b9750-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9750-107">Remarks</span></span>

<span data-ttu-id="b9750-108">O valor pode ser recebido do evento de mídia [MEPolicySet](./mepolicyset.md) .</span><span class="sxs-lookup"><span data-stu-id="b9750-108">The value can be recieved from the [MEPolicySet](./mepolicyset.md) media event.</span></span> <span data-ttu-id="b9750-109">Ele é armazenado como uma carga de tipo **VT_UI4** no evento **MEPolicySet** .</span><span class="sxs-lookup"><span data-stu-id="b9750-109">It is stored as a **VT_UI4** type payload in the **MEPolicySet** event.</span></span>


## <a name="requirements"></a><span data-ttu-id="b9750-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9750-110">Requirements</span></span>



| <span data-ttu-id="b9750-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9750-111">Requirement</span></span> | <span data-ttu-id="b9750-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b9750-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9750-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9750-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b9750-114">Atualização de abril de 2020 do Windows 10</span><span class="sxs-lookup"><span data-stu-id="b9750-114">Windows 10 April 2020 Update</span></span>   <br/>                                      |
| <span data-ttu-id="b9750-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9750-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b9750-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9750-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b9750-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9750-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9750-118"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9750-118"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9750-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9750-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9750-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b9750-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>



 

 
