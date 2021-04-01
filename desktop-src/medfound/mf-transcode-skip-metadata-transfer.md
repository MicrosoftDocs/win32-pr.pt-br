---
description: Especifica se os metadados são gravados no arquivo transcodificado.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: Atributo MF_TRANSCODE_SKIP_METADATA_TRANSFER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164756"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a><span data-ttu-id="01bfc-103">\_Atributo de \_ \_ transferência de metadados ignorar transcodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="01bfc-103">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute</span></span>

<span data-ttu-id="01bfc-104">Especifica se os metadados são gravados no arquivo transcodificado.</span><span class="sxs-lookup"><span data-stu-id="01bfc-104">Specifies whether metadata is written to the transcoded file.</span></span> <span data-ttu-id="01bfc-105">Esse atributo de contêiner é armazenado no perfil transcodificar.</span><span class="sxs-lookup"><span data-stu-id="01bfc-105">This container attribute is stored in the transcode profile.</span></span>

## <a name="data-type"></a><span data-ttu-id="01bfc-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="01bfc-106">Data type</span></span>

<span data-ttu-id="01bfc-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="01bfc-107">**UINT32**</span></span>

<span data-ttu-id="01bfc-108">Os valores possíveis para o \_ atributo de transferência de metadados MF de ignorar transcodificação \_ \_ \_ são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="01bfc-108">Possible values for the MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute are described in the following table.</span></span>



| <span data-ttu-id="01bfc-109">Valor</span><span class="sxs-lookup"><span data-stu-id="01bfc-109">Value</span></span>                                                                        | <span data-ttu-id="01bfc-110">Significado</span><span class="sxs-lookup"><span data-stu-id="01bfc-110">Meaning</span></span>                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01bfc-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="01bfc-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="01bfc-112">Transfere automaticamente os metadados em nível de arquivo do arquivo de origem para o arquivo transcodificado.</span><span class="sxs-lookup"><span data-stu-id="01bfc-112">Automatically transfers file-level metadata from the source file to the transcoded file.</span></span><br/> |
| <dl> <span data-ttu-id="01bfc-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="01bfc-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="01bfc-114">Os metadados do arquivo de origem não são gravados no arquivo transcodificado.</span><span class="sxs-lookup"><span data-stu-id="01bfc-114">The source file metadata is not written to the transcoded file.</span></span><br/>                          |



 

## <a name="getset"></a><span data-ttu-id="01bfc-115">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="01bfc-115">Get/set</span></span>

<span data-ttu-id="01bfc-116">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="01bfc-116">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="01bfc-117">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="01bfc-117">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="01bfc-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="01bfc-118">Remarks</span></span>

<span data-ttu-id="01bfc-119">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="01bfc-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="01bfc-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01bfc-120">Requirements</span></span>



| <span data-ttu-id="01bfc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="01bfc-121">Requirement</span></span> | <span data-ttu-id="01bfc-122">Valor</span><span class="sxs-lookup"><span data-stu-id="01bfc-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01bfc-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01bfc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="01bfc-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="01bfc-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="01bfc-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01bfc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="01bfc-126">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="01bfc-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="01bfc-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01bfc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="01bfc-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="01bfc-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01bfc-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="01bfc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01bfc-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01bfc-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="01bfc-131">**IMFTranscodeProfile:: getcontainerattributes**</span><span class="sxs-lookup"><span data-stu-id="01bfc-131">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="01bfc-132">**IMFTranscodeProfile:: setcontainerattributes**</span><span class="sxs-lookup"><span data-stu-id="01bfc-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




