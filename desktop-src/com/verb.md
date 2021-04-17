---
title: Verbo
description: Especifica os verbos a serem registrados para um aplicativo.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Chave do registro de verbo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105787723"
---
# <a name="verb"></a><span data-ttu-id="4825a-104">Verbo</span><span class="sxs-lookup"><span data-stu-id="4825a-104">Verb</span></span>

<span data-ttu-id="4825a-105">Especifica os verbos a serem registrados para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4825a-105">Specifies the verbs to be registered for an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4825a-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="4825a-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a><span data-ttu-id="4825a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4825a-107">Remarks</span></span>

<span data-ttu-id="4825a-108">Cada verbo é um valor " **\_ reg** " do formato "*nome*, *\_ sinalizador de menu*, *\_ sinalizador de verbo*".</span><span class="sxs-lookup"><span data-stu-id="4825a-108">Each verb is a **REG\_SZ** value of the form "*name*, *menu\_flag*, *verb\_flag*".</span></span> <span data-ttu-id="4825a-109">Os verbos devem ser numerados consecutivamente.</span><span class="sxs-lookup"><span data-stu-id="4825a-109">Verbs must be numbered consecutively.</span></span>

<span data-ttu-id="4825a-110">O *nome* descreve como o verbo é acrescentado por uma chamada de função [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) .</span><span class="sxs-lookup"><span data-stu-id="4825a-110">The *name* describes how the verb is appended by an [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function call.</span></span> <span data-ttu-id="4825a-111">Por exemplo, "&Play".</span><span class="sxs-lookup"><span data-stu-id="4825a-111">For example, "&Play".</span></span>

<span data-ttu-id="4825a-112">O valor do *\_ sinalizador de menu* indica como o verbo deve aparecer no menu.</span><span class="sxs-lookup"><span data-stu-id="4825a-112">The *menu\_flag* value indicates how the verb should appear in the menu.</span></span> <span data-ttu-id="4825a-113">Todos os sinalizadores com suporte do [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) têm suporte, com exceção do \_ bitmap MF, MF \_ OWNERDRAW e \_ pop-up MF.</span><span class="sxs-lookup"><span data-stu-id="4825a-113">All flags supported by [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) are supported, except for MF\_BITMAP, MF\_OWNERDRAW, and MF\_POPUP.</span></span>

<span data-ttu-id="4825a-114">O valor do *\_ sinalizador de verbo* descreve os atributos dos verbos.</span><span class="sxs-lookup"><span data-stu-id="4825a-114">The *verb\_flag* value describes attributes of the verbs.</span></span> <span data-ttu-id="4825a-115">Use um dos valores de [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)ou 0.</span><span class="sxs-lookup"><span data-stu-id="4825a-115">Use one of the values from [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib), or 0.</span></span>

<span data-ttu-id="4825a-116">Para obter mais informações, consulte [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)e [**IOleObject:: EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span><span class="sxs-lookup"><span data-stu-id="4825a-116">For more information, see [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb), and [**IOleObject::EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4825a-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4825a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4825a-118">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="4825a-118">**AppendMenu**</span></span>](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="4825a-119">**OLEVERB**</span><span class="sxs-lookup"><span data-stu-id="4825a-119">**OLEVERB**</span></span>](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[<span data-ttu-id="4825a-120">**OLEVERBATTRIB**</span><span class="sxs-lookup"><span data-stu-id="4825a-120">**OLEVERBATTRIB**</span></span>](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 