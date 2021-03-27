---
description: Definindo atributos de tipo de arquivo no registro.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Como definir atributos de tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7844c65191d6513a06625a28c47accd3df5cc82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828295"
---
# <a name="how-to-define-file-type-attributes"></a><span data-ttu-id="132e8-103">Como definir atributos de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="132e8-103">How to Define File Type Attributes</span></span>

<span data-ttu-id="132e8-104">A atribuição de atributos de tipo de arquivo a um ProgID associado permite que você controle alguns aspectos do comportamento do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="132e8-104">Assigning file type attributes to an associated ProgID enables you to control some aspects of the file type's behavior.</span></span> <span data-ttu-id="132e8-105">Antes do Windows Vista, esses atributos poderiam permitir que você limite a extensão na qual o usuário poderia usar a guia de propriedades de **Opções de pasta** para modificar vários aspectos do tipo de arquivo, como seu ícone ou verbos.</span><span class="sxs-lookup"><span data-stu-id="132e8-105">Prior to Windows Vista, these attributes could enable you to limit the extent to which the user could use the **Folder Options** property tab to modify various aspects of the file type, such as its icon or verbs.</span></span>

<span data-ttu-id="132e8-106">Os atributos de tipo de arquivo são sinalizadores binários especificados como valores **reg \_ DWORD** ou **reg \_ Binary** na subchave ProgID associada do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="132e8-106">File type attributes are binary flags specified as **REG\_DWORD** or **REG\_BINARY** values in the file type's associated ProgID subkey.</span></span>

<span data-ttu-id="132e8-107">Para atribuir atributos a um tipo de arquivo, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="132e8-107">To assign attributes for a file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="132e8-108">Instruções</span><span class="sxs-lookup"><span data-stu-id="132e8-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="132e8-109">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="132e8-109">Step 1:</span></span>

<span data-ttu-id="132e8-110">Adicione uma entrada EditFlags à subchave ProgID associada do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="132e8-110">Add an EditFlags entry to the file type's associated ProgID subkey.</span></span>

### <a name="step-2"></a><span data-ttu-id="132e8-111">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="132e8-111">Step 2:</span></span>

<span data-ttu-id="132e8-112">Defina a entrada para o valor de atributo apropriado.</span><span class="sxs-lookup"><span data-stu-id="132e8-112">Set the entry to the appropriate attribute value.</span></span>

<span data-ttu-id="132e8-113">O exemplo a seguir mostra os \_ atributos FTAs NoRemove (0x00000010) e FTAs \_ NoNewVerb (0x00000020) definidos para o tipo de arquivo. MYP.</span><span class="sxs-lookup"><span data-stu-id="132e8-113">The following example shows the FTA\_NoRemove (0x00000010) and FTA\_NoNewVerb (0x00000020) attributes set for the .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a><span data-ttu-id="132e8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="132e8-114">Remarks</span></span>

<span data-ttu-id="132e8-115">Os sinalizadores podem ser combinados com um OR lógico para formar o valor de atributo único.</span><span class="sxs-lookup"><span data-stu-id="132e8-115">The flags can be combined with a logical OR to form the single attribute value.</span></span>

<span data-ttu-id="132e8-116">Para obter uma lista de possíveis atributos de tipo de arquivo e seus valores hexadecimais e mais detalhes sobre como recuperar e definir esses valores programaticamente, consulte [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span><span class="sxs-lookup"><span data-stu-id="132e8-116">For a list of possible file type attributes and their hexadecimal values, and more details on programmatically retrieving and setting these values, see [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span></span>

 

 



