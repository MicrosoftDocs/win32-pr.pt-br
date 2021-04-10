---
description: Especifica se o aplicativo requer suporte ao Microsoft Direct3D no leitor de origem ou no gravador de coletor.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: Atributo MF_READWRITE_D3D_OPTIONAL (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171727"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a><span data-ttu-id="fc709-103">\_ \_ Atributo opcional MF ReadWrite D3D \_</span><span class="sxs-lookup"><span data-stu-id="fc709-103">MF\_READWRITE\_D3D\_OPTIONAL attribute</span></span>

<span data-ttu-id="fc709-104">Especifica se o aplicativo requer suporte ao Microsoft Direct3D no [leitor de origem](source-reader.md) ou no [gravador de coletor](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="fc709-104">Specifies whether the application requires Microsoft Direct3D support in the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="fc709-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fc709-105">Data type</span></span>

<span data-ttu-id="fc709-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="fc709-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fc709-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc709-107">Remarks</span></span>

<span data-ttu-id="fc709-108">Esse atributo se aplicará somente se o aplicativo habilitar o suporte a Direct3D usando o atributo de [ \_ \_ \_ \_ Gerenciador](mf-sink-writer-d3d-manager.md) de D3D de [ \_ leitor de origem \_ \_ \_ MF](mf-source-reader-d3d-manager.md) ou do gravador de coletor MF.</span><span class="sxs-lookup"><span data-stu-id="fc709-108">This attribute applies only if the application enables Direct3D support using the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) or [MF\_SINK\_WRITER\_D3D\_MANAGER](mf-sink-writer-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="fc709-109">Se o aplicativo habilitar o suporte a Direct3D, o leitor de origem e o gravador de coletor tentarão alocar superfícies de Direct3D para vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc709-109">If the application enables Direct3D support, the Source Reader and Sink Writer will both try to allocate Direct3D surfaces for video.</span></span> <span data-ttu-id="fc709-110">Se isso falhar e o \_ \_ atributo opcional MF ReadWrite D3D \_ for **true**, o gravador de leitor/coletor de origem retornará para alocar superfícies de vídeo na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="fc709-110">If this fails, and the MF\_READWRITE\_D3D\_OPTIONAL attribute is **TRUE**, the Source Reader/Sink Writer will fall back to allocating video surfaces in system memory.</span></span> <span data-ttu-id="fc709-111">Caso contrário, se as superfícies do Direct3D não puderem ser alocadas e \_ o MF ReadWrite \_ D3D \_ opcional for **false**, ocorrerá um erro durante o processamento.</span><span class="sxs-lookup"><span data-stu-id="fc709-111">Otherwise, if Direct3D surfaces cannot be allocated and MF\_READWRITE\_D3D\_OPTIONAL is **FALSE**, an error occurs during processing.</span></span>

<span data-ttu-id="fc709-112">Se o aplicativo não habilitar o suporte a Direct3D, o gravador leitor/coletor de origem usará a memória do sistema e ignorará o valor do MF \_ ReadWrite \_ D3D \_ opcional.</span><span class="sxs-lookup"><span data-stu-id="fc709-112">If the application does not enable Direct3D support, the Source Reader/Sink Writer uses system memory, and ignores the value of MF\_READWRITE\_D3D\_OPTIONAL.</span></span>

<span data-ttu-id="fc709-113">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="fc709-113">This attribute is optional.</span></span> <span data-ttu-id="fc709-114">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="fc709-114">The default value is **FALSE**.</span></span> <span data-ttu-id="fc709-115">Defina o atributo ao criar o leitor de origem ou o gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="fc709-115">Set the attribute when you create the Source Reader or Sink Writer.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc709-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc709-116">Requirements</span></span>



| <span data-ttu-id="fc709-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc709-117">Requirement</span></span> | <span data-ttu-id="fc709-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fc709-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc709-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc709-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc709-120">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fc709-120">Windows 8 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fc709-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc709-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc709-122">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fc709-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fc709-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc709-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc709-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc709-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc709-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc709-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc709-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fc709-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fc709-127">Atributos do gravador de coletor</span><span class="sxs-lookup"><span data-stu-id="fc709-127">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="fc709-128">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="fc709-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




