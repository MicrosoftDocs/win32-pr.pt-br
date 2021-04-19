---
title: Atributo ShadowFilePath
description: O atributo ShadowFilePath é o caminho totalmente qualificado para um arquivo de sombra.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- Atributo ShadowFilePath Windows Media Player
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747714"
---
# <a name="shadowfilepath-attribute"></a><span data-ttu-id="76859-104">Atributo ShadowFilePath</span><span class="sxs-lookup"><span data-stu-id="76859-104">ShadowFilePath Attribute</span></span>

<span data-ttu-id="76859-105">O atributo **ShadowFilePath** é o caminho totalmente qualificado para um arquivo de sombra.</span><span class="sxs-lookup"><span data-stu-id="76859-105">The **ShadowFilePath** attribute is the fully qualified path to a shadow file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="76859-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="76859-106">Applies To</span></span>

-   [<span data-ttu-id="76859-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="76859-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="76859-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="76859-108">Remarks</span></span>

<span data-ttu-id="76859-109">Um *arquivo de sombra* é criado como parte de uma conversão de formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="76859-109">A *shadow file* is created as part of a file format conversion.</span></span> <span data-ttu-id="76859-110">É a cópia de um arquivo que o Player usa quando o usuário sincroniza o conteúdo do computador para um dispositivo que exige que o conteúdo esteja no formato de arquivo original.</span><span class="sxs-lookup"><span data-stu-id="76859-110">It is the copy of a file that the Player uses when the user syncs content from the computer to a device that requires the content to be in the original file format.</span></span> <span data-ttu-id="76859-111">Esse atributo é definido para o arquivo convertido a fim de apontar para o local do arquivo de sombra.</span><span class="sxs-lookup"><span data-stu-id="76859-111">This attribute is set for the converted file to point to the location of the shadow file.</span></span>

<span data-ttu-id="76859-112">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="76859-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="76859-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76859-113">Requirements</span></span>



| <span data-ttu-id="76859-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="76859-114">Requirement</span></span> | <span data-ttu-id="76859-115">Valor</span><span class="sxs-lookup"><span data-stu-id="76859-115">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="76859-116">Versão</span><span class="sxs-lookup"><span data-stu-id="76859-116">Version</span></span><br/> | <span data-ttu-id="76859-117">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="76859-117">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="76859-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="76859-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76859-119">**Sobre o processo de conversão**</span><span class="sxs-lookup"><span data-stu-id="76859-119">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="76859-120">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="76859-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





