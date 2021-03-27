---
description: Os valores de sinalizador SFGAO dos atributos de Shell de um item podem ser testados para determinar se o verbo deve ser habilitado ou desabilitado.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Como usar atributos de item
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828286"
---
# <a name="how-to-use-item-attributes"></a><span data-ttu-id="d9dc4-103">Como usar atributos de item</span><span class="sxs-lookup"><span data-stu-id="d9dc4-103">How to Use Item Attributes</span></span>

<span data-ttu-id="d9dc4-104">Os valores de sinalizador [**SFGAO**](sfgao.md) dos atributos de Shell de um item podem ser testados para determinar se o verbo deve ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d9dc4-104">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="d9dc4-105">Para usar esse recurso de atributo, adicione os seguintes valores de **reg \_ DWORD** no verbo:</span><span class="sxs-lookup"><span data-stu-id="d9dc4-105">To use this attribute feature, add the following **REG\_DWORD** values under the verb:</span></span>

## <a name="instructions"></a><span data-ttu-id="d9dc4-106">Instruções</span><span class="sxs-lookup"><span data-stu-id="d9dc4-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="d9dc4-107">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="d9dc4-107">Step 1:</span></span>

<span data-ttu-id="d9dc4-108">O valor AttributeMask especifica o valor de [**SFGAO**](sfgao.md) dos valores de bits da máscara com a qual testar.</span><span class="sxs-lookup"><span data-stu-id="d9dc4-108">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>

### <a name="step-2"></a><span data-ttu-id="d9dc4-109">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="d9dc4-109">Step 2:</span></span>

<span data-ttu-id="d9dc4-110">O valor AttributeValue especifica o valor [**SFGAO**](sfgao.md) dos bits que são testados.</span><span class="sxs-lookup"><span data-stu-id="d9dc4-110">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="d9dc4-111">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="d9dc4-111">Step 3:</span></span>

<span data-ttu-id="d9dc4-112">O ImpliedSelectionModel Especifica zero para verbos de item ou zero para verbos no menu de atalho de segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d9dc4-112">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9dc4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9dc4-113">Remarks</span></span>

<span data-ttu-id="d9dc4-114">Na entrada de registro de exemplo a seguir, o AttributeMask é definido como [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="d9dc4-114">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



