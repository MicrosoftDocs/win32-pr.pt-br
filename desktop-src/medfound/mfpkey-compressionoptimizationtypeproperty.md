---
description: Especifica as configurações de qualidade visual ideais a serem usadas para o codificador de perfil avançado do Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: Propriedade MFPKEY_COMPRESSIONOPTIMIZATIONTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781380"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a><span data-ttu-id="f4928-103">\_Propriedade MFPKEY COMPRESSIONOPTIMIZATIONTYPE</span><span class="sxs-lookup"><span data-stu-id="f4928-103">MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE Property</span></span>

<span data-ttu-id="f4928-104">Especifica as configurações de qualidade visual ideais a serem usadas para o codificador de perfil avançado do Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="f4928-104">Specifies the optimal visual quality settings to use for the Windows Media Video 9 Advanced Profile encoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f4928-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f4928-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f4928-106">g \_ wszWMVCCompressionOptimizationType</span><span class="sxs-lookup"><span data-stu-id="f4928-106">g\_wszWMVCCompressionOptimizationType</span></span>

## <a name="data-type"></a><span data-ttu-id="f4928-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f4928-107">Data Type</span></span>

<span data-ttu-id="f4928-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="f4928-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f4928-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="f4928-109">Default Value</span></span>

<span data-ttu-id="f4928-110">0</span><span class="sxs-lookup"><span data-stu-id="f4928-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="f4928-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4928-111">Remarks</span></span>

<span data-ttu-id="f4928-112">Essa propriedade fornece uma maneira rápida de configurar várias opções de codificação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f4928-112">This property provides a quick way to configure a number of video encoding options.</span></span> <span data-ttu-id="f4928-113">Pode ser definido como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4928-113">It may be set to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f4928-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f4928-114">Value</span></span></th>
<th><span data-ttu-id="f4928-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4928-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f4928-116">0</span><span class="sxs-lookup"><span data-stu-id="f4928-116">0</span></span></td>
<td><span data-ttu-id="f4928-117">O codec não forçará a otimização e usará quaisquer recursos especificados por outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="f4928-117">The codec will not force optimization and will use whatever features are specified by other properties.</span></span> <span data-ttu-id="f4928-118">Em muitos casos, o codec usará lógica interna para determinar as configurações se elas não forem especificadas.</span><span class="sxs-lookup"><span data-stu-id="f4928-118">In many cases, the codec will use internal logic to determine settings if they are not specified.</span></span> <span data-ttu-id="f4928-119">Este é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="f4928-119">This is the default value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4928-120">1</span><span class="sxs-lookup"><span data-stu-id="f4928-120">1</span></span></td>
<td><span data-ttu-id="f4928-121">Habilita os recursos que produzirão a melhor qualidade visual. O uso desse valor configura o codec como se você tivesse definido as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="f4928-121">Enables the features that will produce the best visual quality.Using this value configures the codec as if you had set the following properties:</span></span><br/>
<ul>
<li><span data-ttu-id="f4928-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span><span class="sxs-lookup"><span data-stu-id="f4928-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span></span></li>
<li><span data-ttu-id="f4928-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span><span class="sxs-lookup"><span data-stu-id="f4928-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span></span></li>
<li><span data-ttu-id="f4928-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span><span class="sxs-lookup"><span data-stu-id="f4928-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span></span></li>
<li><span data-ttu-id="f4928-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</span><span class="sxs-lookup"><span data-stu-id="f4928-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</span></span></li>
<li><span data-ttu-id="f4928-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span><span class="sxs-lookup"><span data-stu-id="f4928-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span></span></li>
<li><span data-ttu-id="f4928-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</span><span class="sxs-lookup"><span data-stu-id="f4928-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</span></span></li>
<li><span data-ttu-id="f4928-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span><span class="sxs-lookup"><span data-stu-id="f4928-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span></span></li>
</ul>
<span data-ttu-id="f4928-129">Se você definir qualquer uma das propriedades na lista anterior, o valor definido substituirá os valores associados a essa configuração, exceto por <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span><span class="sxs-lookup"><span data-stu-id="f4928-129">If you set any of the properties in the previous list, the value you set overrides the values associated with this setting, except for <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f4928-130">Definir o valor da propriedade MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE como 1 também tem o efeito de definir a configuração de registro de opção Dquant como 2 e a configuração do registro de método de custo de vetor de movimento como 1.</span><span class="sxs-lookup"><span data-stu-id="f4928-130">Setting the value of the MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE property to 1 also has the effect of setting the Dquant Option registry setting to 2, and the Motion Vector Cost Method registry setting to 1.</span></span> <span data-ttu-id="f4928-131">Para obter mais informações, consulte o artigo da Web [usando as configurações avançadas do codec de perfil avançado do Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span><span class="sxs-lookup"><span data-stu-id="f4928-131">For more information, see the web article [Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4928-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4928-132">Requirements</span></span>



| <span data-ttu-id="f4928-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4928-133">Requirement</span></span> | <span data-ttu-id="f4928-134">Valor</span><span class="sxs-lookup"><span data-stu-id="f4928-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4928-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4928-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f4928-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f4928-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f4928-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4928-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f4928-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f4928-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f4928-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4928-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4928-140"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4928-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4928-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4928-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4928-142">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4928-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




