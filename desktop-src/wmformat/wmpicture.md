---
title: WM/imagem
description: O atributo WM/Picture contém uma imagem relacionada ao conteúdo.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- Formato de mídia do WM/Picture Windows
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916750"
---
# <a name="wmpicture"></a><span data-ttu-id="99145-104">WM/imagem</span><span class="sxs-lookup"><span data-stu-id="99145-104">WM/Picture</span></span>

<span data-ttu-id="99145-105">O atributo **WM/Picture** contém uma imagem relacionada ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="99145-105">The **WM/Picture** attribute contains a picture related to the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="99145-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="99145-106">Global Constant</span></span>

<span data-ttu-id="99145-107">g \_ wszWMPicture</span><span class="sxs-lookup"><span data-stu-id="99145-107">g\_wszWMPicture</span></span>

## <a name="data-type"></a><span data-ttu-id="99145-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="99145-108">Data Type</span></span>

<span data-ttu-id="99145-109">[**WM \_ PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**\_ tipo \_ binário WMT**)</span><span class="sxs-lookup"><span data-stu-id="99145-109">[**WM\_PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="99145-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="99145-110">Remarks</span></span>

<span data-ttu-id="99145-111">Esse atributo é compatível com o quadro ID3, APIC.</span><span class="sxs-lookup"><span data-stu-id="99145-111">This attribute is compatible with the ID3 frame, APIC.</span></span> <span data-ttu-id="99145-112">A especificação ID3 para o quadro APIC determina que, embora possa haver qualquer número de quadros APIC associados a um arquivo, apenas um pode ser do tipo 1 e apenas um pode ser do tipo 2.</span><span class="sxs-lookup"><span data-stu-id="99145-112">The ID3 specification for the APIC frame stipulates that, while there may be any number of APIC frames associated with a file, only one may be of type 1 and only one may be of type 2.</span></span> <span data-ttu-id="99145-113">A especificação também indica que a descrição da imagem não pode ter mais de 64 caracteres, mas pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="99145-113">The specification also states that the description of the picture can be no longer than 64 characters, but can be empty.</span></span>

<span data-ttu-id="99145-114">Os atributos do WM/Picture adicionados com os objetos do Windows Media Format SDK não são validados automaticamente para obedecer às especificações ID3.</span><span class="sxs-lookup"><span data-stu-id="99145-114">WM/Picture attributes added with the objects of the Windows Media Format SDK are not automatically validated to conform to ID3 specifications.</span></span> <span data-ttu-id="99145-115">Você deve adicionar código em seu aplicativo para executar validações se desejar manter a compatibilidade completa com ID3.</span><span class="sxs-lookup"><span data-stu-id="99145-115">You must add code in your application to perform validations if you want to maintain complete compatibility with ID3.</span></span>

## <a name="see-also"></a><span data-ttu-id="99145-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="99145-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99145-117">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="99145-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="99145-118">**imagem do WM \_**</span><span class="sxs-lookup"><span data-stu-id="99145-118">**WM\_PICTURE**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




