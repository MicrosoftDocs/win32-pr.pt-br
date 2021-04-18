---
description: A propriedade ProductLanguage especifica o idioma que o instalador deve usar para todas as cadeias de caracteres na interface do usuário que não são criadas no banco de dados.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Propriedade ProductLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792491"
---
# <a name="productlanguage-property"></a><span data-ttu-id="fa8f6-103">Propriedade ProductLanguage</span><span class="sxs-lookup"><span data-stu-id="fa8f6-103">ProductLanguage property</span></span>

<span data-ttu-id="fa8f6-104">A propriedade **ProductLanguage** especifica o idioma que o instalador deve usar para todas as cadeias de caracteres na interface do usuário que não são criadas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-104">The **ProductLanguage** property specifies the language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="fa8f6-105">Essa propriedade deve ser um identificador de idioma numérico (LANGid).</span><span class="sxs-lookup"><span data-stu-id="fa8f6-105">This property must be a numeric language identifier (LANGID).</span></span> <span data-ttu-id="fa8f6-106">Se uma transformação alterar o idioma da interface do usuário no banco de dados, ela também deverá alterar o valor dessa propriedade para refletir a nova linguagem.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-106">If a transform changes the language of the user interface in the database, then it should also change the value of this property to reflect the new language.</span></span>

<span data-ttu-id="fa8f6-107">Essa propriedade é necessária.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-107">This property is REQUIRED.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa8f6-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa8f6-108">Remarks</span></span>

<span data-ttu-id="fa8f6-109">O valor da propriedade **ProductLanguage** deve ser um dos idiomas listados na propriedade Summary do [**modelo**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="fa8f6-109">The value of the **ProductLanguage** property must be one of the languages listed in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="fa8f6-110">Ao criar um pacote como com neutralidade de idioma, defina a propriedade **ProductLanguage** como 0 e use a fonte MS Shell Dlg como o estilo de texto para todas as caixas de diálogo criadas.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-110">When authoring a package as language-neutral, set the **ProductLanguage** property to 0 and use the MS Shell Dlg font as the text style for all authored dialogs.</span></span> <span data-ttu-id="fa8f6-111">Como algumas fontes não dão suporte a todos os conjuntos de caracteres, usando essa fonte, você pode garantir que o texto seja exibido corretamente em todas as versões localizadas do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-111">Because some fonts do not support all the character sets, by using this font you can ensure that the text is correctly displayed on all localized versions of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa8f6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa8f6-112">Requirements</span></span>



| <span data-ttu-id="fa8f6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa8f6-113">Requirement</span></span> | <span data-ttu-id="fa8f6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="fa8f6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8f6-115">Versão</span><span class="sxs-lookup"><span data-stu-id="fa8f6-115">Version</span></span><br/> | <span data-ttu-id="fa8f6-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fa8f6-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fa8f6-118">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fa8f6-119">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa8f6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa8f6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa8f6-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa8f6-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




