---
title: DRM_Rights
description: A \_ Propriedade direitos de DRM especifica os direitos que o aplicativo precisará na próxima tentativa de abrir um arquivo protegido.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007092"
---
# <a name="drm_rights"></a><span data-ttu-id="f1b2d-104">Direitos de DRM \_</span><span class="sxs-lookup"><span data-stu-id="f1b2d-104">DRM\_Rights</span></span>

<span data-ttu-id="f1b2d-105">A **propriedade \_ direitos de DRM** especifica os direitos que o aplicativo precisará na próxima tentativa de abrir um arquivo protegido.</span><span class="sxs-lookup"><span data-stu-id="f1b2d-105">The **DRM\_Rights** property specifies the rights that the application will require in the next attempt to open a protected file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f1b2d-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="f1b2d-106">Global Constant</span></span>

<span data-ttu-id="f1b2d-107">\_direitos g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="f1b2d-107">g\_wszWMDRM\_Rights</span></span>

## <a name="data-type"></a><span data-ttu-id="f1b2d-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f1b2d-108">Data Type</span></span>

<span data-ttu-id="f1b2d-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="f1b2d-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="f1b2d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1b2d-110">Remarks</span></span>

<span data-ttu-id="f1b2d-111">Essa é uma propriedade de leitura/gravação que é recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) e definida usando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) ou [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="f1b2d-111">This is a read-write property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) and set using either [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) or [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

<span data-ttu-id="f1b2d-112">A tabela a seguir lista os direitos com suporte.</span><span class="sxs-lookup"><span data-stu-id="f1b2d-112">The following table lists the supported rights.</span></span>



| <span data-ttu-id="f1b2d-113">Direita</span><span class="sxs-lookup"><span data-stu-id="f1b2d-113">Right</span></span>                                           | <span data-ttu-id="f1b2d-114">Cadeia de caracteres literal</span><span class="sxs-lookup"><span data-stu-id="f1b2d-114">String literal</span></span>      | <span data-ttu-id="f1b2d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1b2d-115">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b2d-116">\_ \_ backup do g wszWMDRM direito \_</span><span class="sxs-lookup"><span data-stu-id="f1b2d-116">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="f1b2d-117">Backup</span><span class="sxs-lookup"><span data-stu-id="f1b2d-117">"Backup"</span></span>            | <span data-ttu-id="f1b2d-118">Direito de fazer backup da licença.</span><span class="sxs-lookup"><span data-stu-id="f1b2d-118">Right to back up the license.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="f1b2d-119">g \_ wszWMDRM \_ de \_ colaboração à \_ direita</span><span class="sxs-lookup"><span data-stu-id="f1b2d-119">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="f1b2d-120">"CollaborativePlay"</span><span class="sxs-lookup"><span data-stu-id="f1b2d-120">"CollaborativePlay"</span></span> | <span data-ttu-id="f1b2d-121">Direito de reproduzir o arquivo como parte de uma lista de reprodução colaborativa.</span><span class="sxs-lookup"><span data-stu-id="f1b2d-121">Right to play the file as part of a collaborative playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="f1b2d-122">\_ \_ copiar à direita do g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="f1b2d-122">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="f1b2d-123">CopiarObjeto</span><span class="sxs-lookup"><span data-stu-id="f1b2d-123">"Copy"</span></span>              | <span data-ttu-id="f1b2d-124">Direito de copiar o arquivo para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1b2d-124">Right to copy the file to a device.</span></span> <span data-ttu-id="f1b2d-125">Esse direito substitui os direitos de cópia mais antigos (g \_ wszWMDRM \_ à direita \_ copiar \_ para \_ CD, g \_ wszWMDRM \_ à direita \_ copiar \_ para \_ \_ dispositivo não SDMI \_ e g \_ wszWMDRM \_ a cópia à direita \_ para o \_ \_ dispositivo SDMI \_ ).</span><span class="sxs-lookup"><span data-stu-id="f1b2d-125">This right supersedes the older copy rights (g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD, g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE, and g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE).</span></span> |
| <span data-ttu-id="f1b2d-126">\_ \_ \_ copiar \_ para o \_ CD do g wszWMDRM</span><span class="sxs-lookup"><span data-stu-id="f1b2d-126">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="f1b2d-127">"Print. Redbook"</span><span class="sxs-lookup"><span data-stu-id="f1b2d-127">"Print.redbook"</span></span>     | <span data-ttu-id="f1b2d-128">Direito de copiar o arquivo em um CD (formato de livro vermelho). No Windows Media DRM 10, esse direito é substituído pela \_ \_ cópia direita g wszWMDRM \_ .</span><span class="sxs-lookup"><span data-stu-id="f1b2d-128">Right to copy the file to a CD (Red Book format).In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                             |
| <span data-ttu-id="f1b2d-129">\_ \_ copiar à direita do g wszWMDRM \_ para um \_ \_ \_ dispositivo não SDMI \_</span><span class="sxs-lookup"><span data-stu-id="f1b2d-129">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="f1b2d-130">"Transfer. NONSDMI"</span><span class="sxs-lookup"><span data-stu-id="f1b2d-130">"Transfer.NONSDMI"</span></span>  | <span data-ttu-id="f1b2d-131">Direito de copiar o arquivo para um dispositivo não SDMI. No Windows Media DRM 10, esse direito é substituído pela \_ \_ cópia direita g wszWMDRM \_ .</span><span class="sxs-lookup"><span data-stu-id="f1b2d-131">Right to copy the file to a non-SDMI device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                                  |
| <span data-ttu-id="f1b2d-132">\_ \_ copiar à direita do g wszWMDRM \_ para o \_ \_ \_ dispositivo SDMI</span><span class="sxs-lookup"><span data-stu-id="f1b2d-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="f1b2d-133">"Transfer. SDMI"</span><span class="sxs-lookup"><span data-stu-id="f1b2d-133">"Transfer.SDMI"</span></span>     | <span data-ttu-id="f1b2d-134">Direito de copiar o arquivo para um dispositivo compatível com SDMI. No Windows Media DRM 10, esse direito é substituído pela \_ \_ cópia direita g wszWMDRM \_ .</span><span class="sxs-lookup"><span data-stu-id="f1b2d-134">Right to copy the file to an SDMI-compliant device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                           |
| <span data-ttu-id="f1b2d-135">\_ \_ reprodução à direita g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="f1b2d-135">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="f1b2d-136">Reproduzir</span><span class="sxs-lookup"><span data-stu-id="f1b2d-136">"Play"</span></span>              | <span data-ttu-id="f1b2d-137">Direito de reproduzir o arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f1b2d-137">Right to play the media file.</span></span>                                                                                                                                                                                        |



 

<span data-ttu-id="f1b2d-138">Essa propriedade contém uma cadeia de caracteres largos de um ou mais direitos separados por ponto-e-vírgula, por exemplo: L "reprodução; CopiarObjeto CollaborativePlay".</span><span class="sxs-lookup"><span data-stu-id="f1b2d-138">This property contains a wide-character string of one or more rights separated by semicolons, for example: L"Playback;Copy;CollaborativePlay".</span></span>

## <a name="see-also"></a><span data-ttu-id="f1b2d-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1b2d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b2d-140">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="f1b2d-140">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





