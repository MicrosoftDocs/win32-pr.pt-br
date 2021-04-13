---
title: Recurso de BITMAP
description: Define um bitmap que um aplicativo usa na tela de exibição ou como um item em um menu ou controle.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Menus de recursos de BITMAP e outros recursos
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5bed33fb66d9deb85e1f25165f3f7a0f664961
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365908"
---
# <a name="bitmap-resource"></a><span data-ttu-id="84781-104">Recurso de BITMAP</span><span class="sxs-lookup"><span data-stu-id="84781-104">BITMAP resource</span></span>

<span data-ttu-id="84781-105">Define um bitmap que um aplicativo usa na tela de exibição ou como um item em um menu ou controle.</span><span class="sxs-lookup"><span data-stu-id="84781-105">Defines a bitmap that an application uses in its screen display or as an item in a menu or control.</span></span>

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a><span data-ttu-id="84781-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84781-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84781-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="84781-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="84781-108">Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="84781-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="84781-109"><span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="84781-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="84781-110">Nome do arquivo que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="84781-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="84781-111">O nome deve ser um nome de arquivo válido; Ele deve ser um caminho completo se o arquivo não estiver no diretório de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="84781-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="84781-112">O caminho deve ser uma cadeia de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="84781-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="84781-113">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="84781-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="84781-114">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="84781-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="84781-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="84781-115">Examples</span></span>

<span data-ttu-id="84781-116">O exemplo a seguir define dois recursos de bitmap:</span><span class="sxs-lookup"><span data-stu-id="84781-116">The following example defines two bitmap resources:</span></span>

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a><span data-ttu-id="84781-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="84781-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84781-118">Usando bitmaps</span><span class="sxs-lookup"><span data-stu-id="84781-118">Using Bitmaps</span></span>](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[<span data-ttu-id="84781-119">**LoadBitmap**</span><span class="sxs-lookup"><span data-stu-id="84781-119">**LoadBitmap**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[<span data-ttu-id="84781-120">**LoadImage**</span><span class="sxs-lookup"><span data-stu-id="84781-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 