---
description: Esses sinalizadores especificam o comportamento do localizador de mídia.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Sinalizadores de validação de nome de arquivo (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766312"
---
# <a name="file-name-validation-flags"></a><span data-ttu-id="54aa4-103">Sinalizadores de validação de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="54aa4-103">File Name Validation Flags</span></span>

<span data-ttu-id="54aa4-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="54aa4-104">\[Deprecated.</span></span> <span data-ttu-id="54aa4-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="54aa4-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="54aa4-106">Esses sinalizadores especificam o comportamento do localizador de mídia.</span><span class="sxs-lookup"><span data-stu-id="54aa4-106">These flags specify the behavior of the media locator.</span></span>



| <span data-ttu-id="54aa4-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="54aa4-107">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="54aa4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="54aa4-108">Description</span></span>                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <span data-ttu-id="54aa4-109"><dt>**SFN \_ \_Verificar VALIDATEF**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="54aa4-109"><dt>**SFN\_VALIDATEF\_CHECK**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="54aa4-110">Verifique a validade dos nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="54aa4-110">Check the validity of file names.</span></span> <span data-ttu-id="54aa4-111">Você deve definir esse sinalizador para validar nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="54aa4-111">You must set this flag to validate file names.</span></span> <span data-ttu-id="54aa4-112">Caso contrário, os outros sinalizadores não terão nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="54aa4-112">If not, the other flags have no effect.</span></span><br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <span data-ttu-id="54aa4-113"><dt>**SFN \_ VALIDATEF \_ Popup**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="54aa4-113"><dt>**SFN\_VALIDATEF\_POPUP**</dt> <dt>0x02</dt></span></span> </dl>                   | <span data-ttu-id="54aa4-114">Se um arquivo não estiver localizado, exiba uma caixa de diálogo abrir arquivo para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="54aa4-114">If a file is not located, display an Open File dialog box for the end user.</span></span><br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <span data-ttu-id="54aa4-115"><dt>**SFN \_ VALIDATEF \_ TELLME**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="54aa4-115"><dt>**SFN\_VALIDATEF\_TELLME**</dt> <dt>0x04</dt></span></span> </dl>                | <span data-ttu-id="54aa4-116">Se um arquivo ausente estiver localizado, exiba brevemente uma caixa de mensagem com o nome e o local do arquivo.</span><span class="sxs-lookup"><span data-stu-id="54aa4-116">If a missing file is located, briefly display a message box with the name and location of the file.</span></span> <span data-ttu-id="54aa4-117">Esse sinalizador é útil principalmente para fins de teste; a caixa de mensagem provavelmente não é adequada para um produto de varejo.</span><span class="sxs-lookup"><span data-stu-id="54aa4-117">This flag is mostly useful for testing purposes; the message box is probably not suitable for a retail product.</span></span><br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <span data-ttu-id="54aa4-118"><dt>**SFN \_ VALIDATEF \_ substituir**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="54aa4-118"><dt>**SFN\_VALIDATEF\_REPLACE**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="54aa4-119">Se um arquivo ausente estiver localizado, atualize o nome do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="54aa4-119">If a missing file is located, update the name of the source object.</span></span> <span data-ttu-id="54aa4-120">(Válido somente no método [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) .)</span><span class="sxs-lookup"><span data-stu-id="54aa4-120">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <span data-ttu-id="54aa4-121"><dt>**SFN \_ VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="54aa4-121"><dt>**SFN\_VALIDATEF\_USELOCAL**</dt> <dt>0x10</dt></span></span> </dl>          | <span data-ttu-id="54aa4-122">Sempre use um arquivo local, mesmo se houver uma versão do arquivo na rede.</span><span class="sxs-lookup"><span data-stu-id="54aa4-122">Always use a local file, even if a version of the file exists on the network.</span></span><br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <span data-ttu-id="54aa4-123"><dt>**SFN \_ VALIDATEF \_ NoFind**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="54aa4-123"><dt>**SFN\_VALIDATEF\_NOFIND**</dt> <dt>0x20</dt></span></span> </dl>                | <span data-ttu-id="54aa4-124">Não pesquise arquivos ausentes.</span><span class="sxs-lookup"><span data-stu-id="54aa4-124">Do not search for missing files.</span></span> <span data-ttu-id="54aa4-125">Os nomes de arquivo ainda serão validados se você definir o \_ sinalizador de verificação SFN VALIDATEF \_ .</span><span class="sxs-lookup"><span data-stu-id="54aa4-125">File names are still validated if you set the SFN\_VALIDATEF\_CHECK flag.</span></span><br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <span data-ttu-id="54aa4-126"><dt>**SFN \_ VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="54aa4-126"><dt>**SFN\_VALIDATEF\_IGNOREMUTED**</dt> <dt>0x40</dt></span></span> </dl> | <span data-ttu-id="54aa4-127">Ignorar objetos de origem sem som.</span><span class="sxs-lookup"><span data-stu-id="54aa4-127">Ignore muted source objects.</span></span> <span data-ttu-id="54aa4-128">(Válido somente no método [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) .)</span><span class="sxs-lookup"><span data-stu-id="54aa4-128">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                                                                |



## <a name="requirements"></a><span data-ttu-id="54aa4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54aa4-129">Requirements</span></span>



| <span data-ttu-id="54aa4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="54aa4-130">Requirement</span></span> | <span data-ttu-id="54aa4-131">Valor</span><span class="sxs-lookup"><span data-stu-id="54aa4-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54aa4-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54aa4-132">Header</span></span><br/> | <dl> <span data-ttu-id="54aa4-133"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="54aa4-133"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54aa4-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="54aa4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54aa4-135">**IMediaLocator::FindMediaFile**</span><span class="sxs-lookup"><span data-stu-id="54aa4-135">**IMediaLocator::FindMediaFile**</span></span>](imedialocator-findmediafile.md)
</dt> <dt>

[<span data-ttu-id="54aa4-136">**IRenderEngine::SetSourceNameValidation**</span><span class="sxs-lookup"><span data-stu-id="54aa4-136">**IRenderEngine::SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




