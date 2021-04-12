---
title: Atributo src (VMLFrame) (VML)
description: Atributo src (VMLFrame) (VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294179"
---
# <a name="src-attribute-vmlframevml"></a><span data-ttu-id="1c737-103">Atributo src (VMLFrame) (VML)</span><span class="sxs-lookup"><span data-stu-id="1c737-103">Src Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="1c737-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1c737-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1c737-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="1c737-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1c737-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="1c737-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1c737-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="1c737-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1c737-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1c737-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1c737-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1c737-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1c737-110">Define a fonte de dados para o quadro.</span><span class="sxs-lookup"><span data-stu-id="1c737-110">Defines the source of data for the frame.</span></span> <span data-ttu-id="1c737-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1c737-111">Read/write.</span></span> <span data-ttu-id="1c737-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="1c737-112">**String**.</span></span>

<span data-ttu-id="1c737-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="1c737-113">**Applies To**</span></span>

[<span data-ttu-id="1c737-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="1c737-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="1c737-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="1c737-115">**Tag Syntax**</span></span>

<span data-ttu-id="1c737-116"><v: *Element* src = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="1c737-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="1c737-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="1c737-117">**Script Syntax**</span></span>

<span data-ttu-id="1c737-118">*Element* . src = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="1c737-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="1c737-119">*expressão* = de *elemento*. src</span><span class="sxs-lookup"><span data-stu-id="1c737-119">*expression*=*element*.src</span></span>

<span data-ttu-id="1c737-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="1c737-120">**Remarks**</span></span>

<span data-ttu-id="1c737-121">O atributo **src** pode envolver as seguintes sintaxes:</span><span class="sxs-lookup"><span data-stu-id="1c737-121">The **Src** attribute can involve the following syntaxes:</span></span>

-   <span data-ttu-id="1c737-122">URL para o arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="1c737-122">URL to external file.</span></span> <span data-ttu-id="1c737-123">O arquivo deve ser um arquivo XML com o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="1c737-123">The file must be an XML file with the following format:</span></span>
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   <span data-ttu-id="1c737-124">Dentro do arquivo, você deve ter uma ou mais formas de VML com IDs válidas que podem ser referenciadas usando essa sintaxe:</span><span class="sxs-lookup"><span data-stu-id="1c737-124">Inside the file you must have one or more VML shapes with valid IDs that can be referenced by using this syntax:</span></span>
    ```HTML
       filename#shapename
    ```

    

-   <span data-ttu-id="1c737-125">Na referência a seguir, os arquivos externos têm a extensão. VML, mas qualquer extensão pode ser usada:</span><span class="sxs-lookup"><span data-stu-id="1c737-125">In the following reference, external files have the .vml extension, but any extension can be used:</span></span>
    ```HTML
       external.vml#image01
    ```

    

-   <span data-ttu-id="1c737-126">Você pode fazer referência a uma forma dentro do mesmo arquivo usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="1c737-126">You can reference a shape within the same file by using the following syntax:</span></span>
    ```HTML
       #shapename
    ```

    

<span data-ttu-id="1c737-127">Se **clip** for **false**, a forma será dimensionada para caber no quadro.</span><span class="sxs-lookup"><span data-stu-id="1c737-127">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="1c737-128">Se **for true**, qualquer parte da forma que estiver fora do quadro não será exibida.</span><span class="sxs-lookup"><span data-stu-id="1c737-128">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="1c737-129">Observe que a [origem](origin-attribute--vmlframe--vml.md) e o [tamanho](size-attribute--vmlframe.md) não serão usados, a menos que o **clipe** seja **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="1c737-129">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="1c737-130">**Atributo padrão da VML**</span><span class="sxs-lookup"><span data-stu-id="1c737-130">**VML Standard Attribute**</span></span>

<span data-ttu-id="1c737-131">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="1c737-131">**Example**</span></span>

<span data-ttu-id="1c737-132">A imagem definida no arquivo externo será recortada.</span><span class="sxs-lookup"><span data-stu-id="1c737-132">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 