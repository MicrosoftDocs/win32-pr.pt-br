---
description: Obtém estatísticas do coletor de mídia de rede de vida digital (DLNA).
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: Atributo MF_MP2DLNA_STATISTICS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502390"
---
# <a name="mf_mp2dlna_statistics-attribute"></a><span data-ttu-id="98c07-103">\_Atributo de \_ estatísticas MF MP2DLNA</span><span class="sxs-lookup"><span data-stu-id="98c07-103">MF\_MP2DLNA\_STATISTICS attribute</span></span>

<span data-ttu-id="98c07-104">Obtém estatísticas do coletor de mídia de rede de vida digital (DLNA).</span><span class="sxs-lookup"><span data-stu-id="98c07-104">Gets statistics from the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="98c07-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="98c07-105">Data type</span></span>

<span data-ttu-id="98c07-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** armazenado como **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="98c07-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="98c07-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="98c07-107">Get/set</span></span>

<span data-ttu-id="98c07-108">Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="98c07-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="98c07-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="98c07-109">Remarks</span></span>

<span data-ttu-id="98c07-110">Durante o streaming, o coletor de mídia DLNA atualiza esse atributo com estatísticas sobre a codificação e a multiplexação dos fluxos MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="98c07-110">During streaming, the DLNA media sink updates this attribute with statistics about the encoding and multiplexing of the MPEG-2 streams.</span></span> <span data-ttu-id="98c07-111">O aplicativo pode consultar esse atributo a qualquer momento para obter os valores mais recentes.</span><span class="sxs-lookup"><span data-stu-id="98c07-111">The application can query this attribute at any time to get the latest values.</span></span>

<span data-ttu-id="98c07-112">A definição desse atributo no coletor de mídia DLNA não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="98c07-112">Setting this attribute on the DLNA media sink has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="98c07-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98c07-113">Requirements</span></span>



| <span data-ttu-id="98c07-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c07-114">Requirement</span></span> | <span data-ttu-id="98c07-115">Valor</span><span class="sxs-lookup"><span data-stu-id="98c07-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98c07-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98c07-116">Minimum supported client</span></span><br/> | <span data-ttu-id="98c07-117">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="98c07-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="98c07-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98c07-118">Minimum supported server</span></span><br/> | <span data-ttu-id="98c07-119">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="98c07-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="98c07-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98c07-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="98c07-121"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="98c07-121"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98c07-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="98c07-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c07-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98c07-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




