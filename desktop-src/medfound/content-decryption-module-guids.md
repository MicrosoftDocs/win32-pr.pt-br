---
description: Os GUIDs a seguir dão suporte a implementações de CDM (módulo de descriptografia de conteúdo).
title: GUIDs do CDM (Módulo de Descriptografia de Conteúdo)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105808391"
---
# <a name="content-decryption-module-cdm-guids"></a><span data-ttu-id="a599b-103">GUIDs do CDM (Módulo de Descriptografia de Conteúdo)</span><span class="sxs-lookup"><span data-stu-id="a599b-103">Content Decryption Module (CDM) GUIDs</span></span>

<span data-ttu-id="a599b-104">Os GUIDs a seguir dão suporte a implementações de CDM (módulo de descriptografia de conteúdo).</span><span class="sxs-lookup"><span data-stu-id="a599b-104">The following GUIDs support Content Decryption Module (CDM) implementations.</span></span>

<span data-ttu-id="a599b-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span><span class="sxs-lookup"><span data-stu-id="a599b-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span></span>

<span data-ttu-id="a599b-106">GUID de serviço usado para obter interfaces de uma implementação de [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) , como a interface [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) do WinRT.</span><span class="sxs-lookup"><span data-stu-id="a599b-106">Service GUID used to obtain interfaces from an [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) implementation,such as the WinRT [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) interface.</span></span> <span data-ttu-id="a599b-107">Uma implementação de **IMFContentDecryptionModule** deve implementar o [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) e dar suporte a esse GUID de serviço.</span><span class="sxs-lookup"><span data-stu-id="a599b-107">An implementation of **IMFContentDecryptionModule** should implement [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) and support this service GUID.</span></span>


## <a name="requirements"></a><span data-ttu-id="a599b-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a599b-108">Requirements</span></span>



| <span data-ttu-id="a599b-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a599b-109">Requirement</span></span> | <span data-ttu-id="a599b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a599b-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a599b-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a599b-111">Header</span></span><br/> | <dl> <span data-ttu-id="a599b-112"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="a599b-112"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a599b-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="a599b-113">See also</span></span>



- [<span data-ttu-id="a599b-114">Media Foundation constantes</span><span class="sxs-lookup"><span data-stu-id="a599b-114">Media Foundation Constants</span></span>](media-foundation-constants.md)
- <span data-ttu-id="a599b-115">[IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span><span class="sxs-lookup"><span data-stu-id="a599b-115">[IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span></span>
- [<span data-ttu-id="a599b-116">IMediaProtectionPMPServer</span><span class="sxs-lookup"><span data-stu-id="a599b-116">IMediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [<span data-ttu-id="a599b-117">IMFGetService</span><span class="sxs-lookup"><span data-stu-id="a599b-117">IMFGetService</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




